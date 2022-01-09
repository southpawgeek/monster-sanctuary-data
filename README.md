# Monster Sanctuary Data
## Game version: `1.3.0.18`

### What is this?
This is extracted data from the game [Monster Sanctuary](https://monster-sanctuary.com/). You should buy the game if you haven't already.

### Where did the data come from?
uTinyRipper was used to extract `.prefab` and `.prefab.meta` files.

### How did you parse the data?
Several custom YAML parsers, written in Perl.

### Are you releasing the parsers?
Not at this time.

### What else to expect?
Check the [Issues](https://github.com/southpawgeek/monster-sanctuary-data/issues) before adding new ones.
* Structures may not be final
* Skills may be missing
* Attributes and/or values may be missing

### Will the data be updated for future patches?
Current plan is to keep it up-to-date. 


### Data structure (partial)
```json
{
    "monsters": {
        "<id>": {
            "name": "<string>",
            "bio": "<string>",
            "skills": [ // array of arrays...
                [ // each array represents a skill tree
                    // and will contain 5 tiers
                    // each tier contains an array of skill IDs
                    {"tier1": [<id>, ...]},
                    {"tier2": [<id>, ...]}
                // and so on
                ]
            ]
        }
    },
    "skills": {
        "<id>": {
            "name": "<string>",
            "element": "<string>",
            "icon": "<string>"
        }
    }
}
```

### Credit
* [lmmfranco](https://github.com/lmmfranco/monster-sanctuary-exported-data) for pointing me in the right direction.
* [mafaca](https://github.com/mafaca/UtinyRipper) for the uTinyRipper tool.