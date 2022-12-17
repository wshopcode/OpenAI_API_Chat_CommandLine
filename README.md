# OpenAI_API_Chat_CommandLine
A python program that takes user input, and the program will respond with an intelligent response. Using the OpenAI API

We're going to write a program that takes user input, and the program will respond with an intelligent response. Pretty much any kind of input works. You can

    ask it questions,
    ask it to give you ideas,
    ask it to help you with a writing task,

and much more.

**STEP 1:**
You'll need to sign up to use the OpenAI API. At the time of writing this, a free tier is available and no credit card is required to use the API.

**STEP 2:**
Once you've signed up, you'll want to find your API key and export it as an environment variable. It should look something like this:

```export OPENAPI_API_KEY='PUT_API_KEY_HERE'```

OR
you can include the API KEY as an absolute path in the script in step 3 below(this is not recommended for security reasons). It should look something like this:
```openai.api_key = 'PUT_API_KEY_HERE'```

**STEP 3:**
install Open AI via terminal
```py -m pip install openai```
OR
```py pip install openai```

**STEP 4:**
create a python file and include the code below
```
import os
import openai

**openai.api_key = 'PUT_API_KEY_HERE'

**while True:
    prompt = input("Ask OpenAI Anything: ")
    completions = openai.Completion.create(prompt=prompt,
                                           engine="text-davinci-003",
                                           max_tokens=100)
    completion = completions.choices[0].text
    print(completion)
```
    
**STEP 5:**
Save the python script and run it from the command line!





