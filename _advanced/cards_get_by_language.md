---
title: Find by foreign name
position: 1.1
type: get
description: Get Cards by Foriegn Name
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

cards = MTG::Card.where(name: 'Arcángel Avacyn')
                 .where(language: 'spanish')
                 .all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Card

cards = Card.where(name='Arcángel Avacyn')
            .where(language='spanish')
            .all()
~~~
{: title="python" }

~~~ javascript
const mtg = require('mtgsdk')

mtg.card.where({name: 'Arcángel Avacyn', language: 'spanish'})
.then(results => {
    console.log(results)
})
~~~
{: title="javascript" }

~~~ bash
curl "https://api.magicthegathering.io/v1/cards?name=Arcángel Avacyn&language=spanish"
~~~
{: title="bash" }



