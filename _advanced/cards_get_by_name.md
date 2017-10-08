---
title: Find by name
position: 1.1
type: get
description: Get Cards by Name
right_code: |
  ~~~ json
  {  
    "cards":[  
        {  
        "name":"Archangel Avacyn",
        "names":[  
            "Archangel Avacyn",
            "Avacyn, the Purifier"
        ],
        "manaCost":"{3}{W}{W}",
        "cmc":5,
        ...
    ]
    }
  ~~~
  {: title="Response" }
---

Returns cards by name

~~~ ruby
require 'mtg_sdk'

# partial name match
cards = MTG::Card.where(name: 'avacyn').all

# exact name mtch
cards = MTG::Card.where(name: '"Archangel Avacyn"').all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Card

# partial name match
cards = Card.where(name='avacyn').all()

# exact name match
cards = Card.where(name='"Archangel Avacyn"').all()
~~~
{: title="python" }

~~~ javascript
const mtg = require('mtgsdk')

// partial name match
mtg.card.where({name: '"Archangel Avacyn"'})
.then(results => {
    console.log(results)
})

// exact name match
mtg.card.where({name: '"Archangel Avacyn"'})
.then(results => {
    console.log(results)
})
~~~
{: title="javascript" }

~~~ bash
# partial name match
curl "https://api.magicthegathering.io/v1/cards?name=avacyn"

# exact name match
curl 'https://api.magicthegathering.io/v1/cards?name="Archangel Avacyn"'
~~~
{: title="bash" }



