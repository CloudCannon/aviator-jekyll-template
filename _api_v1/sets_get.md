---
title: /sets/:id
position: 1.4
type: get
description: Get Set
right_code: |
  ~~~ json
  {  
    "set":{  
        "code":"KTK",
        "name":"Khans of Tarkir",
        "type":"expansion",
        "border":"black",
        "mkm_id":1495,
        "booster":[  
        [  
            "rare",
            "mythic rare"
        ],
        "uncommon",
        "uncommon",
        "uncommon",
        "common",
        "common",
        "common",
        "common",
        "common",
        "common",
        "common",
        "common",
        "common",
        "common",
        "land",
        "marketing"
        ],
        "mkm_name":"Khans of Tarkir",
        "releaseDate":"2014-09-26",
        "magicCardsInfoCode":"ktk",
        "block":"Khans of Tarkir"
    }
  }
  ~~~
  {: title="Response" }
---

Returns a specific set by the set code

~~~ ruby
require 'mtg_sdk'

card = MTG::Set.find('ktk')
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Set

card = Set.find('ktk')
~~~
{: title="python" }

~~~ bash
curl "https://api.magicthegathering.io/v1/sets/ktk"
~~~
{: title="bash" }



