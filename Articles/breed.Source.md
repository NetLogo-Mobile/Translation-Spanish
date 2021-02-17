﻿`breed` is a special primitive that can only be placed in the top of a netlogo code tab. Using `breed`, you can define custom kinds or *breeds* of turtles. It is most useful when you have different groups of turtles that each need to have their own behavior and you want to have an easy way to reference each group within your code.  



To create a new type of turtles, you use the `breed` primitive followed by an opening square bracket `[`, the plural version of the breed, a space, the singular version of the breed, and a closing square bracket `]` . For example, `breed [dogs dog]`, `breed [buildings building]`, and `breed [cars car]`. 



NetLogo requires both the plural and singular versions of a breed because: 

* Different spoken languages may have different conventions for plural and singular words
* Some things may have non-conventional forms for plural and singular such as `breed [cacti cactus]`, `breed [mice mouse]`, or `breed [leaves leaf]`.



`breed` is also special in that it creates other related commands that can be used later on in your code. For example, if you create a **dogs** breed, you can use primitives such as `create-dogs`, `dogs-here`, `hatch-dogs`, `sprout-dogs` and so on. 



You can create as many breeds as you wish in your model. You can also use the `link-breed` primitive to create different groups of links.