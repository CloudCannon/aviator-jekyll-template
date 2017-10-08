---
title: /types
position: 3.0
type: get
description: Get All Types
right_code: |
  ~~~ json
  {  
    "types":[  
      "Artifact",
      "Conspiracy",
      "Creature",
      "Enchantment",
      "Instant",
      "Land",
      "Phenomenon",
      "Plane",
      "Planeswalker",
      "Scheme",
      "Sorcery",
      "Tribal",
      "Vanguard"
    ]
  }
  ~~~
  {: title="Response" }
---

~~~ ruby
require 'mtg_sdk'

types = MTG::Type.all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Type

types = Type.all()
~~~
{: title="python" }

~~~ bash
curl "https://api.magicthegathering.io/v1/types"
~~~
{: title="bash" }



