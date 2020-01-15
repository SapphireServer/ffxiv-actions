# FFXIV Actions
This repo contains mostly complete action data for all regular combat actions - meaning PvP is excluded (for now). Some data may be incorrect or missing, contributions are more than welcome.

Originally based on the work of [Ravahn](https://github.com/ravahn/) for his ACT plugin.

## Folder Structure
All files exist in the `actions` directory. Said actions belong in a json file that represents what _class_ or _job_ they belong to.

For example, the action `Fast Blade` is shared by both Gladiator and Paladin, but the origin class is Gladiator so it goes in the `gladiator` json, not anywhere else.

## Format Structure
Everything should be mostly self explanatory. The `examples` directory has working examples of parsing all of the actions into a usable structure.

```json
{
  "id": 7482,
  "name": "Kasha",
  "positionalDirection": 1,
  "potency": {
    "base": 100,
    "combo": 480,
    "positional": 0,
    "positionalCombo": 0,
    "heal": 0,
    "selfHeal": 0,
    "mpGainPercentage": 0
  },
  "statuses": []
}
```

### PositionalDirection

Has the following values:
 * 0 - None
 * 1 - Flank
 * 2 - Rear
 * 3 - Front

### Statuses

```json
"statuses": [
  {
    "id": 50,
    "name": "Sprint",
    "duration": 10000,
    "param": 0,
    "flags": {
      "ApplyToSelf": true
    }
  }
]
```

#### Flags

* `ApplyToSelf` - always should apply to the caster and never to someone else