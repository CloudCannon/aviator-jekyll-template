---
title: /subtypes
position: 1.6
type: get
description: Get All Sub Types
right_code: |
  ~~~ json
  {  
    "subtypes":[  
      "Advisor",
      "Ajani",
      "Alara",
      "Ally",
      "Angel",
      "Antelope",
      "Ape",
      "Arcane"
    ]
  }
  ~~~
  {: title="Response" }
---

~~~ ruby
require 'mtg_sdk'

subtypes = MTG::Subtype.all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Subtype

subtypes = Subtype.all()
~~~
{: title="python" }

~~~ bash
curl "https://api.magicthegathering.io/v1/subtypes"
~~~
{: title="bash" }



