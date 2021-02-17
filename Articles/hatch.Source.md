﻿`Hatch` is used to create new turtles by an existing turtle. It takes the form of:



```hatch number-of-new-turtles [ optional-commands ]```



The new turtles inherit all the same characteristics as the parent turtle (for example size, color, location, etc.). After being created, the new turtles will run the commands independently. (Note: because adding commands are optional, they are used if you want to change a variable from the parent or have the new turtle do something specific.) `Hatch` is a primitive that can only be used by turtles, that is, within an `ask turtles [ … ] `; only turtles can hatch turtles. To create turtles from patches, see `sprout`.
