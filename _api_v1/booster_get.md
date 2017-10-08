---
title: /sets/:id/booster
position: 2.2
type: get
description: Generate Booster Pack
right_code: |
  ~~~ json
  {
    "cards": [
        {
        "name": "Meandering Towershell",
        "manaCost": "{3}{G}{G}",
        "cmc": 5,
        "colors": [
            "Green"
        ],
        "type": "Creature — Turtle",
        "types": [
            "Creature"
        ],
        "subtypes": [
            "Turtle"
        ],
        ...
        }
    ]
  }
  ~~~
  {: title="Response" }
---

Returns a list of cards for a specific set representing a booster pack for the set.
The number of commons, uncommons, rares, etc. are determined by the `booster` field in a set response.

~~~ ruby
require 'mtg_sdk'

card = MTG::Set.generate_booster('ktk')
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Set
from mtgsdk import Card

card = Set.generate_booster('ktk')
~~~
{: title="python" }

~~~ bash
curl "https://api.magicthegathering.io/v1/sets/ktk/booster"
~~~
{: title="bash" }



