---
title: /cards/:id
position: 1.1
type: get
description: Get Card
right_code: |
  ~~~ json
  {  
    "card":{  
      "name":"Narset, Enlightened Master",
      "manaCost":"{3}{U}{R}{W}",
      "cmc":6,
      "colors":[  
        "White",
        "Blue",
        "Red"
      ],
      "type":"Legendary Creature — Human Monk",
      ...
    }
  }
  ~~~
  {: title="Response" }
---

Returns a specific card by id or multiverseid

~~~ ruby
require 'mtg_sdk'

card = MTG::Card.find(386616)
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Card

card = Card.find(386616)
~~~
{: title="python" }

~~~ javascript
const mtg = require('mtgsdk')

mtg.card.find(386616)
.then(result => {
    console.log(result.card.name)
})
~~~
{: title="javascript" }

~~~ bash
curl "https://api.magicthegathering.io/v1/cards/386616"
~~~
{: title="bash" }



