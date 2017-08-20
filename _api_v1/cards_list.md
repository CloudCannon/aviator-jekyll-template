---
title: /cards
position: 1.0
type: get
description: Get All Cards
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
        "colors":[  
            "White"
        ],
        "colorIdentity":[
            "W"
        ],
        "type":"Legendary Creature — Angel",
        "supertypes":[  
            "Legendary"
        ],
        "types":[  
            "Creature"
        ],
        "subtypes":[  
            "Angel"
        ],
        "rarity":"Mythic Rare",
        "set":"SOI",
        "text":"Flash\nFlying, vigilance\nWhen Archangel Avacyn enters the battlefield, creatures you control gain indestructible until end of turn.\nWhen a non-Angel creature you control dies, transform Archangel Avacyn at the beginning of the next upkeep.",
        "artist":"James Ryman",
        "number":"5a",
        "power":"4",
        "toughness":"4",
        "layout":"double-faced",
        "multiverseid":409741,
        "imageUrl":"http://gatherer.wizards.com/Handlers/Image.ashx?multiverseid=409741&type=card",
        "rulings":[  
            {  
            "date":"2016-04-08",
            "text":"Archangel Avacyn’s delayed triggered ability triggers at the beginning of the next upkeep regardless of whose turn it is."
            },
            {  
            "date":"2016-04-08",
            "text":"Archangel Avacyn’s delayed triggered ability won’t cause it to transform back into Archangel Avacyn if it has already transformed into Avacyn, the Purifier, perhaps because several creatures died in one turn."
            },
            {  
            "date":"2016-04-08",
            "text":"For more information on double-faced cards, see the Shadows over Innistrad mechanics article (http://magic.wizards.com/en/articles/archive/feature/shadows-over-innistrad-mechanics)."
            }
        ],
        "foreignNames":[  
            {  
            "name":"大天使艾维欣",
            "language":"Chinese Simplified",
            "multiverseid":410071
            },
            {  
            "name":"大天使艾維欣",
            "language":"Chinese Traditional",
            "multiverseid":410401
            },
            {  
            "name":"Archange Avacyn",
            "language":"French",
            "multiverseid":411061
            },
            {  
            "name":"Erzengel Avacyn",
            "language":"German",
            "multiverseid":410731
            },
            {  
            "name":"Arcangelo Avacyn",
            "language":"Italian",
            "multiverseid":411391
            },
            {  
            "name":"大天使アヴァシン",
            "language":"Japanese",
            "multiverseid":411721
            },
            {  
            "name":"대천사 아바신",
            "language":"Korean",
            "multiverseid":412051
            },
            {  
            "name":"Arcanjo Avacyn",
            "language":"Portuguese (Brazil)",
            "multiverseid":412381
            },
            {  
            "name":"Архангел Авацина",
            "language":"Russian",
            "multiverseid":412711
            },
            {  
            "name":"Arcángel Avacyn",
            "language":"Spanish",
            "multiverseid":413041
            }
        ],
        "printings":[  
            "SOI"
        ],
        "originalText":"Flash\nFlying, vigilance\nWhen Archangel Avacyn enters the battlefield, creatures you control gain indestructible until end of turn.\nWhen a non-Angel creature you control dies, transform Archangel Avacyn at the beginning of the next upkeep.",
        "originalType":"Legendary Creature — Angel",
        "id":"02ea5ddc89d7847abc77a0fbcbf2bc74e6456559"
        },
        { ... },
        { ... }
    ]
    }
  ~~~
  {: title="Response" }
---
This call will return a maximum of 100 cards
{: .info }

Paginate the response using the `page` parameter.

Each field below can be used as a query parameter. By default, fields that have a singular value such as rarity, set, and name will always use a logical “or” operator when querying with a list of values. Fields that can have multiple values such as colors, supertypes, and subtypes can use a logical "and" or a logical "or" operator.


The accepted delimiters when querying fields are the pipe character or a comma character. The pipe represents a logical “or”, and a comma represents a logical “and”. The comma can only be used with fields that accept multiple values (like colors).

Example:`name=nissa, worldwaker|jace|ajani, caller`
More examples: `colors=red,white,blue` versus `colors=red|white|blue`

name
: The card name. For split, double-faced and flip cards, just the name of one side of the card. Basically each ‘sub-card’ has its own record.

layout
: The card layout. Possible values: normal, split, flip, double-faced, token, plane, scheme, phenomenon, leveler, vanguard

cmc
: Converted mana cost. Always a number

colors
: The card colors. Usually this is derived from the casting cost, but some cards are special (like the back of dual sided cards and Ghostfire).

colorIdentity
: The card colors by color code. [“Red”, “Blue”] becomes [“R”, “U”]

type
: The card type. This is the type you would see on the card if printed today. Note: The dash is a UTF8 'long dash’ as per the MTG rules

supertypes
: The supertypes of the card. These appear to the far left of the card type. Example values: Basic, Legendary, Snow, World, Ongoing

types
: The types of the card. These appear to the left of the dash in a card type. Example values: Instant, Sorcery, Artifact, Creature, Enchantment, Land, Planeswalker

subtypes
: The subtypes of the card. These appear to the right of the dash in a card type. Usually each word is its own subtype. Example values: Trap, Arcane, Equipment, Aura, Human, Rat, Squirrel, etc.

rarity
: The rarity of the card. Examples: Common, Uncommon, Rare, Mythic Rare, Special, Basic Land

set
: The set the card belongs to (set code).

setName
: The set the card belongs to.

text
: The oracle text of the card. May contain mana symbols and other symbols.

flavor
: The flavor text of the card.

artist
: The artist of the card. This may not match what is on the card as MTGJSON corrects many card misprints.

number
: The card number. This is printed at the bottom-center of the card in small text. This is a string, not an integer, because some cards have letters in their numbers.

power
: The power of the card. This is only present for creatures. This is a string, not an integer, because some cards have powers like: “1+*”

toughness
: The toughness of the card. This is only present for creatures. This is a string, not an integer, because some cards have toughness like: “1+*”

loyalty
: The loyalty of the card. This is only present for planeswalkers.

foreignName
: The name of a card in a foreign language it was printed in

language
: The language the card is printed in. Use this parameter when searching by foreignName

gameFormat
: The game format, such as Commander, Standard, Legacy, etc. (when used, legality defaults to Legal unless supplied)

legality
: The legality of the card for a given format, such as Legal, Banned or Restricted.

page
: The page of data to request

pageSize
: The amount of data to return in a single request. The default (and max) is 100.

orderBy
: The field to order by in the response results

random
: Fetch any number of cards (controlled by pageSize) randomly

contains
: Filter cards based on whether or not they have a specific field available (like imageUrl)

id
: A unique id for this card. It is made up by doing an SHA1 hash of setCode + cardName + cardImageName

multiverseid
: The multiverseid of the card on Wizard’s Gatherer web page. Cards from sets that do not exist on Gatherer will NOT have a multiverseid. Sets not on Gatherer are: ATH, ITP, DKM, RQS, DPA and all sets with a 4 letter code that starts with a lowercase 'p’.

#### Other Fields in Response

The fields below are also part of the response (if not null), but cannot currently be used as query parameters

names
: Only used for split, flip and dual cards. Will contain all the names on this card, front or back

manaCost
: The mana cost of this card. Consists of one or more mana symbols. (use cmc and colors to query)

variations
: If a card has alternate art (for example, 4 different Forests, or the 2 Brothers Yamazaki) then each other variation’s multiverseid will be listed here, NOT including the current card’s multiverseid.

imageUrl
: The image url for a card. Only exists if the card has a multiverse id.

watermark
: The watermark on the card. Note: Split cards don’t currently have this field set, despite having a watermark on each side of the split card.

border
: If the border for this specific card is DIFFERENT than the border specified in the top level set JSON, then it will be specified here. (Example: Unglued has silver borders, except for the lands which are black bordered)

timeshifted
: If this card was a timeshifted card in the set.

hand
: Maximum hand size modifier. Only exists for Vanguard cards.

life
: Starting life total modifier. Only exists for Vanguard cards.

reserved
: Set to true if this card is reserved by Wizards Official Reprint Policy

releaseDate
: The date this card was released. This is only set for promo cards. The date may not be accurate to an exact day and month, thus only a partial date may be set (YYYY-MM-DD or YYYY-MM or YYYY). Some promo cards do not have a known release date.

starter
: Set to true if this card was only released as part of a core box set. These are technically part of the core sets and are tournament legal despite not being available in boosters

rulings
: The rulings for the card. An array of objects, each object having 'date’ and 'text’ keys.

foreignNames
: Foreign language names for the card, if this card in this set was printed in another language. An array of objects, each object having 'language’, 'name’ and 'multiverseid’ keys. Not available for all sets.

printings
: The sets that this card was printed in, expressed as an array of set codes.

originalText
: The original text on the card at the time it was printed. This field is not available for promo cards.

originalType
: The original type on the card at the time it was printed. This field is not available for promo cards.

legalities
: Which formats this card is legal, restricted or banned in. An array of objects, each object having 'format’ and 'legality’.

source
: For promo cards, this is where this card was originally obtained. For box sets that are theme decks, this is which theme deck the card is from.

~~~ ruby
require 'mtg_sdk'

# Get all Cards
cards = MTG::Card.all

# Filter Cards
# You can chain 'where' clauses together. The key of the hash
# should be the URL parameter you are trying to filter on
cards = MTG::Card.where(supertypes: 'legendary')
                 .where(types: 'creature')
                 .where(colors: 'red,white')
                 .all

# Get cards on a specific page / pageSize
cards = MTG::Card.where(page: 50).where(pageSize: 50).all
~~~
{: title="ruby" }

~~~ python
from mtgsdk import Card

# Get all cards
cards = Card.all()

# Filter Cards
# You can chain 'where' clauses together. The key of the hash
# should be the URL parameter you are trying to filter on
cards = Card.where(supertypes='legendary') \
            .where(types='creature') \
            .where(colors='red,white') \
            .all()

# Get cards on a specific page / pageSize
cards = Card.where(page=50).where(pageSize=50).all()
~~~
{: title="python" }

~~~ javascript
const mtg = require('mtgsdk')

// Get all cards
mtg.card.all()
.on('data', function (card) {
  console.log(card.name)
});

// Filter Cards
mtg.card.all({ supertypes: 'legendary', types: 'creature', colors: 'red,white' })
.on('data', function (card) {
    console.log(card.name)
});

// Get cards on a specific page / pageSize
mtg.card.where({ page: 50, pageSize: 50})
.then(cards => {
    console.log(cards[0].name)
})
~~~
{: title="javascript" }

~~~ bash
# Get all cards
curl "https://api.magicthegathering.io/v1/cards"

# Filter cards
curl "https://api.magicthegathering.io/v1/cards?supertypes=legendary&types=creature&colors=red,white"

# Get specific page of data
curl "https://api.magicthegathering.io/v1/cards?page=50&pageSize=50"
~~~
{: title="bash" }
