### System Design and Programming

## Services and Interfaces
* When designing an object or component, have a clear vision for the service and interface it will provide.
    * Otherwise, you'll lack sense of direction, you won't know the ins and outs of this object, and you'll end up with a mess.
* Not doing things that aren't your job, is just as important as doing your job.
    * Potentially use Event Based Programming to avoid doing other objects' jobs. Instead send them a message saying the job needs to be done. Its their responsibility to register with you.
* Use Access Modifiers to enforce your interface.
* In general, think carefully about who should act upon a piece of data changing.
* Behavior Design
    * What should this object pay attention to?
    * What should this object not care about?

## Data Model Design
* If possible, only have members that define **fundamental** data.
    * Superfluous data members makes it hard to know the single source of truth.
    * Consider the memory vs computation trade off.
* Picture yourself as being the object - What do you have? What do you know? These are your members.
* Use has-a and is-a extensively.
    * X has-a Y implies Y is a member variable belonging to X.
    * X is-a Y implies X inherits from Y.
* In general, think carefully about who should own a piece of persistent data.

## General
* User Getter/Setters
    * Gives you more flexibility in how fundamental data is interpreted.
    * Allows for easy behavioral changes in derived classes.
    * The object can know (and potentially do actions) when people are reading / writing its data.
    * Fundamental data can **appear** to be modified by the state of the object.
* Don't Repeat Yourself (DRY)
    * If several lines of code look the same, you may want to do more programming to get a more general algorithm.
    * Helps you write less code. Helps you write maintainable code.
* When solving a problem, generate at least a few potential solutions. The first one you think of will probably not be the best.
    * Search for the **best** way to solve the problem, not just **a** way. Program, don't hack.
    * Yet another reason to avoid being under time pressure. If you are, its more tempting to blaze through with the first (potentially poor) solution.
* **Invest** time learning the best way to use the tools and APIs provided to you.
    * Tools are likely more powerful when you use them as designers intended.
