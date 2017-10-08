---
title: /supertypes
position: 5.0
type: get
description: Get All Super Types
right_code: |
  ~~~ json
  {  
    "supertypes":[  
      "Basic",
      "Legendary",
      "Ongoing",
      "Snow",
      "World"
    ]
  }
  ~~~
  {: title="Response" }
---

~~~ ruby
require 'mtg_sdk'

supertypes = MTG::Supertype.all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Supertype

supertypes = Supertype.all()
~~~
{: title="python" }

~~~ bash
curl "https://api.magicthegathering.io/v1/supertypes"
~~~
{: title="bash" }



