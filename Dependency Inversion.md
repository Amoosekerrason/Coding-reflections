# Dependency Inversion

Imagine a person hunting various targets like cows, sheep, chickens, elephants, etc.
Each type of prey requires a different hunting method, and encountering a new target necessitates researching an effective approach from scratch.
Now, instead of dealing with each target individually, we abstract them into a general category,animals,and categorize the hunting methods into abstract strategies such as bleeding, burning, exhaustion, or trapping.
Each specific animal then determines how these abstract hunting strategies apply to its nature.
This way, all animals can be systematically hunted without requiring hunters to rework their approach for each individual species.
This transforms the dependency: instead of directly relying on concrete targets, the hunter now depends on the abstract animal layer, and each target also relies on this layer.
By introducing this additional abstraction, we create Dependency Inversion.
Even if the hunter encounters the Alien(aka Xenomorph XX121) , as long as it falls under the broader definition of an "animal," the existing strategies like bleeding or burning remain applicable.
The hunter only needs to determine how to execute these methods effectively to guarantee success.

If the above example still isn’t clear enough, then imagine you have Sherry, Mary, Coco, and Isabella—so many people that your bad memory causes you to mix up their names, leading to catastrophic consequences. So, you abstract a layer called ‘baby’. You depend on ‘baby’, and they also depend on ‘baby’. That way, you can call all of them ‘baby’, and they know they are your baby. This is what dependency inversion means.