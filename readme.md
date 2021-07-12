# eAI Sample Mission

Instructions to combine with your own mission folder:

1. Copy the directory `eAI` into your own mission folder
2. In your `init.c`, add the `#include` line from this mission’s `init.c`
3. IMPORTANT: In your `main()` function, add the line `InitDynamicPatrols();` at the end.
4. Replace the mission name in the `#include` line with your mission name. It should look like:

```
#include "$CurrentDir:mpmissions/<MISSION>.<MAPNAME>/eAI/AI_init.c"
```

