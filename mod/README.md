# Overview

Have you ever wondered what other Clone Army leaders might be able to do, when not leading a fleet?  Or maybe wondered why their (thematically-appropriate) generals don't have any special bonuses?  Well wonder no more!  With this mod, your Origin: Clone Army empires will have a full suite of special traits, including your rules.  As you might expect, these bonuses are largely related to naval and army bonuses.

# Changes

Adds twelve new traits for leaders from Clone Soldier species, one for each non-Admiral leader class for regular, Ascendant, and Descendant clone soldiers.  These traits follow roughly the same scaling as the built-in Clone Army Admiral traits: the Ascendant trait is about twice as powerful, while the Descendant trait is about half as powerful.  In order to ensure all Clone Soldier leaders have their traits applied when completing one of the mutually-exclusive Clone Army special project choices, this mode needs to preempts three events related to adjusting Clone Soldier leader traits.

## Compatibility

Preempts three of the built-in Origin: Clone Army events: `clones.22`, `clones.23`, and `clones.24`.  These events need to be replaced so that Clone Soldier traits can be up-/down-graded when completing the relevant special projects, therefor this mod will not work with other mods that also replace these events.

Built for Stellaris version 3.8 "Gemini."  Not compatible with achievements.

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/sharedfiles/filedetails/?id=2522974089) because it is a considerable buff to leaders for empires with Origin: Clone Army.  It is otherwise fully compatible.

## Known Issues

Preempting an event causes the game to log an error, so expect to see three error.log entries similar to these:

```
[00:15:19][eventmanager.cpp:368]: an event with id [clones.22] already exists!  file: events/clone_army_events.txt line: 441
[00:15:19][eventmanager.cpp:368]: an event with id [clones.23] already exists!  file: events/clone_army_events.txt line: 555
[00:15:19][eventmanager.cpp:368]: an event with id [clones.24] already exists!  file: events/clone_army_events.txt line: 622
```

## Changelog

* 1.0.0 Initial version
* 2.0.0 Update for Stellaris version 3.4 "Cepheus" - use memory optimization feature for effects
* 2.1.0 Mark as compatible with Stellaris version 3.6 "Orion" - no script changes
* 3.0.0 Add a compatibility trigger for other mods to check whether this one is active, remove old compatibility global flag
* 3.0.1 Fix several events referring to the incorrect namespace
* 3.1.0 Mark as compatible with Stellaris version 3.7 "Canis Minor" - no script changes
* 4.0.0 Update for Stellaris version 3.8 "Gemini"
    * Combine each level of Clone Soldier leader class traits into one trigger-based trait per level, similar to the structure of `leader_trait_brainslug`
    * Update effect code to use condensed traits
* 4.0.1 Do not notify when Clone Soldier traits are gained
* 4.0.2 Remove an unnecessary ownership check (plus the leader is exiled and has no owner when combined with Leader Traits: All Eligible Species Traits)

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/leader_traits_more_clone_soldiers)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.