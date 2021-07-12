# eAI Sample Mission

Instructions to combine with your own mission folder:

1. Copy the directory `eAI` into your own mission folder
2. In your `init.c`, add the `#include` line from this mission’s `init.c`
3. IMPORTANT: In your `main()` function, add the line `InitDynamicPatrols();` at the end.
4. Replace the mission name in the `#include` line with your mission name. It should look like:

```
#include "$CurrentDir:mpmissions/<MISSION>.<MAPNAME>/eAI/AI_init.c"
```

# AI Settings:

AI Spawn Amount:

1. Navigate to the directory `eAI` in your own mission folder and open up the `AI_init.c` file
2. Scroll down till you find the `patrol_aiAmmount` array

```
ref array<int> patrol_aiAmmount = {MIN_NUMBER_PER_PATROL, RandomAIAmmount(), RandomAIAmmount(10, 20)};
```

3. For each patrol entry in your `patrol_list` array you must add an entry to the `patrol_aiAmmount` array
You can choose from `MIN_NUMBER_PER_PATROL`, `RandomAIAmmount()` or `RandomAIAmmount(10, 20)`

`MIN_NUMBER_PER_PATROL` Will use the minimum you set
`RandomAIAmmount()` Will use a value between `MIN_NUMBER_PER_PATROL` and `MAX_NUMBER_PER_PATROL`
`RandomAIAmmount(10, 20)` Will override the `MIN_NUMBER_PER_PATROL` and `MAX_NUMBER_PER_PATROL` incase you wish to supply a custom min and max for a patrol
