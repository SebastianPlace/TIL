# Cohesion

Cohesion is a measure of how well parts of a module belong together.

A highly cohesive module could be a module which encapsulates arithmetic functions for instance.

Low cohesion implies that a module encapsulates logic which does not belong together. For instance a module which has some arithmetic functions and some functions responsible for rendering results.

## Advantages of highly cohesive code

- Maintainability - Changing logic within a highly cohesive module requires fewer changes in other modules.
- Module reusability - Devs are more likely to use small simple modules over monolithic hauls of shit.
- Module simplicity - Single responsibility.
