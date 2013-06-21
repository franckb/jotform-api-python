jotform-api-python 
===============
JotForm API - Python Client


### Installation

Install via git clone:

        $ git clone git://github.com/jotform/jotform-api-python.git
        $ cd jotform-api-python
        
or

Install via Composer package manager (http://getcomposer.org/)
        
_composer.json_
```json
    {
        "require": {
            "jotform/jotform-api-php": "dev-master"
        }
    }
```

        $ php composer.phar install

### Documentation

You can find the docs for the API of this client at [http://api.jotform.com/docs/](http://api.jotform.com/docs)

### Authentication

JotForm API requires API key for all user related calls. You can create your API Keys at  [API section](http://www.jotform.com/myaccount/api) of My Account page.

### Examples

Print all forms of the user

from jotform import *


def main():

    jotformAPIClient = JotformAPIClient('YOUR API KEY')


    forms = jotformAPIClient.get_forms()

    for form in forms:
    	print form["title"]

if __name__ == "__main__":
    main()

   

Get latest submissions of the user
    
