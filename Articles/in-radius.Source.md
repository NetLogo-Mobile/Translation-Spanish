﻿`in-radius` is used when you want to select all agents within a certain radius of the current agent. For example, a turtle might like to know how many other turtles are within two units of itself, or a patch might like to know how many turtles are within three units of itself. You can think of `in-radius` as a filter that takes some large agentset and filters out all those agents too far away, leaving only those within a given radius.



For example, say you wanted to model air pollution. In the model below, all the patches within a certain radius of a factory are polluted, represented by darkening those patches. By varying the given radius, we can simulate different levels of pollution.