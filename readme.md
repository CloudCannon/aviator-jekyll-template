# Magic: The Gathering API Documentation

Welcome to the API documentation! Please feel free to make pull requests if you see something is out of date, or you wish to provide additional docs for an SDK or the API itself.

## Setup

To get started with the documentation locally, you will need to have Ruby installed. Once ruby is installed, run the following from the root directory:

`bundle install`

## Running Local Server

`bundle exec jekyll serve`

## Updating Documentation

The main files you will be working with are in the directories `_documentation` and `_api_v1`.

To add a code section for an SDK, check the examples in the files of the `_api_v1` folder. Here is a brief example:

```
~~~ python
from mtgsdk import Card

card = Card.find(386616)
~~~
{: title="python" }
```