---
title: Making API requests with Python
date: 2020-10-20T01:27:01.202Z
description: Learn how to make simple API requests using Python's request module.
---

## Requirements

- Python 2.7, 3.5+
- Code editor of your choice (I use VSCode)

## Overview

Many times as a developer, you will be required to get data from an API.

> According to Oxford Languages an API is a set of functions and procedures allowing the creation of applications that access the features or data of an operating system, application, or other service.

## API

Lets say for example, you want to fetch some data about cat facts because everybody loves cats, right? [Here](https://alexwohlbruck.github.io/cat-facts/docs/) is the website for the API we will be using. Before we get to coding, lets take a look at the documentation and see how we can use this API.

At the top, is tells us that the base endpoint for the API requests is `https://cat-fact.herokuapp.com`. Awesome, now it tells us that the endpoint we want to use to fetch the facts is `/facts`. Now lets visit that link all put together which is [https://cat-fact.herokuapp.com/facts](https://cat-fact.herokuapp.com/facts). When you visit the site you should see a long list of JSON objects (cat facts!).

> Json.org tells us that JSON is: a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate. You will often see JSON responses in not only API requests, but also in several instances along your web-developer journey. JSON makes it easy for developers to read and write data across multiple programming languages.

## Coding

Lets get to coding!

Get started by opening your editor of choice and creating a new python file. Make sure the file is saved as `<NAME-OF-FILE>.py` (It is important to save it with the .py extension) where NAME-OF-FILE is the name of the file that you want.

Lets start by adding the file imports at the top.

```
import requests
```

We need the python requests module to fetch api requests.

Now, lets create a variable to store the URL in which we want to fetch data from.

```
import requests

# URL we are fetching data from
url = 'https://cat-fact.herokuapp.com/facts'
```

Now lets set a variable to store the response from the request get requests

```
import requests

# URL we are fetching data from
url = 'https://cat-fact.herokuapp.com/facts'

# Response from requests
response = requests.get(url)
```

Cool, now lets add a simple print statement to print the response to see the data!

```
import requests

# URL we are fetching data from
url = 'https://cat-fact.herokuapp.com/facts'

# Response from requests
response = requests.get(url)

# Print the output
print(response)
```

Now run the file.

Wait, why don't I see any data? I only see a `<Response [200]>`?

It's ok! A 200 response means that the request is OK and has succeeded. Remember that the data response is in JSON, so we will need to format the response to JSON to see the actual data.

> According to Mozilla 'The HTTP 200 OK success status response code indicates that the request has succeeded'.

Now, lets format the data to JSON so we can actually see our cat facts. Don't worry this part is easy because Python has a built in JSON library which allows us to easily convert the response to json.

To your print statement, add `.json()`. Your print statement should now look like the following:

```
print(response.json())
```

Ta-Da you should now see a long list of cat facts in JSON format!

To make it a little easier, lets just grab the first cat fact and display it. Notice in the JSON response the first `key` is 'all'. We should grab the 'all' key and then the first cat item's text.

Here is the code to do this:

```
print(response.json()['all'][0]['text'])
```

This line of code may look a little bit complicated but lets break it down.

JSON has what is known as Key-Value pairs to format its data. A typical JSON response contains JSON objects which can have nested JSON objects. Here we have the first key `all` so we used `['all']` to grab and display all keys in the all key section. Next we use `[0]` to grab the first index of the all object (the first cat fact object). 

If we print that first cat object with the following code we get the following:

```
print(response.json()['all'][0])

# Output
# {
        '_id': '591d9b2f227c1a0020d26823',  
        'text': 'Every year, nearly four million cats are eaten in China as a delicacy.', 
        'type': 'cat', 
        'user': {'_id': # '5a9ac18c7478810ea6c06381', 'name': {'first': 'Alex', 'last': 'Wohlbruck'}}, 
        'upvotes': 7, 
        'userUpvoted': None
    }
#
```

Now we can see the entire JSON object for the first cat JSON object which includes the fact ID, text, type, user, upvotes, and userUpvoted. We are interested in the fact itself, so that's where the ['text'] key comes in. If we add in that key to the end, it will display only the cat fact.

```
print(response.json()['all'][0]['text'])

# Output
# Every year, nearly four million cats are eaten in China as a delicacy.
```

You may see a different cat fact, that's fine it just means the list was updated so the first cat fact changed. 

## Conclusion

There you have it, that is the basics of using the python request module to fetch data from an API. You can use this method to fetch data from any JSON based API. 

## Additional Reading 

- A list of open APIs to use: [Medium](https://medium.com/better-programming/a-curated-list-of-100-cool-and-fun-public-apis-to-inspire-your-next-project-7600ce3e9b3)
- Python Requests module documentation: [Docs](https://requests.readthedocs.io/en/master/)
- Mozilla 200 response code: [Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/200)
- Additional JSON information: [JSON.org](https://www.json.org/json-en.html)

        