---
title: /sets
position: 1.3
type: get
description: Get All Sets
right_code: |
  ~~~ json
    {  
    "sets":[  
        {  
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
        },
        { ... }.
        { ... }
    ]
    }
  ~~~
  {: title="Response" }
---

Currently, only the name and block fields can be used as query parameters. To query on multiple names or blocks at a time, use a pipe separated list (ex. `sets?name=khans|origins`).

name
: The name of the set

block
: The block the set is in

#### Other Fields In Reponse

The fields below are also part of the response (if not null), but cannot be used as query parameters.

code
: The code name of the set

gathererCode
: The code that Gatherer uses for the set. Only present if different than ‘code’

oldCode
: An old style code used by some Magic software. Only present if different than 'gathererCode’ and 'code’

magicCardsInfoCode
: The code that magiccards.info uses for the set. Only present if magiccards.info has this set

releaseDate
: When the set was released (YYYY-MM-DD). For promo sets, the date the first card was released

border
: The type of border on the cards, either “white”, “black” or “silver”

expansion
: Type of set. One of: “core”, “expansion”, “reprint”, “box”, “un”, “from the vault”, “premium deck”, “duel deck”, “starter”, “commander”, “planechase”, “archenemy”, “promo”, “vanguard”, “masters”

onlineOnly
: Present and set to true if the set was only released online

booster
: Booster contents for this set

~~~ ruby
require 'mtg_sdk'

# Get all Sets
sets = MTG::Set.all

# Filter Sets
sets = MTG::Set.where(name: 'khans').all

# Get sets on a specific page / pageSize
sets = MTG::Set.where(page: 2).where(pageSize: 10).all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Set

# Get all Sets
sets = Set.all()

# Filter Sets
sets = Set.where(name='khans').all()

# Get sets on a specific page / pageSize
sets = Set.where(page=2).where(pageSize=10).all()
~~~
{: title="python" }

~~~ bash
# Get all sets
curl "https://api.magicthegathering.io/v1/sets"

# Filter cards
curl "https://api.magicthegathering.io/v1/sets?name=khans"

# Get specific page of data
curl "https://api.magicthegathering.io/v1/sets?page=2&pageSize=10"
~~~
{: title="bash" }



