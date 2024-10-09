# COMP2160 Prac Week 12 - Refactoring

## Today's Task
Today's prac is focused on putting your game development skills in action, rather than learning a new area of development. This practical involves refactoring an older practical from the unit. You can pick any practical you already have a full mark for. If you only have half marks for practicals, speak to your demonstrator about which practical task is best for you to pick.

## Refactoring
This task involves refactoring a previous practical task you have completed. Refactoring is the process of re-writing code to improve its operations without changing functionality. The topic was previously covered in live lectures by both Cameron and Malcolm. You can also read Vasileios Karavasilis' [Game Developer article on Refactoring](https://www.gamedeveloper.com/programming/refactoring-the-way-to-perfection-) for more context.

## Step 1 - Pick a Prac (10 min)
Pick a practical task you have already completed (or you have approval from your demonstrator to work on despite only having half a mark for it). Make sure it is committed and pushed to Github, as you will need to show your version history to your demonstrator to receive your mark.

## Step 2 - Plan your refector (30 min)

### Finding a smell
When refactoring, we are looking to not change the functionality of the code, but instead to improve its **performance** or **architecture**, making it easier to **use and modify**. Often, when we first write code, we take a few shortcuts to get things done. These little shortcuts add up! The problems that emerge later due to poorly written code is often called **technical debt**, and we can identify technical debt through **code smell**. Code smell comes in many shapes and forms. According to [Matt Eland](https://multisearch.mq.edu.au/permalink/61MACQUARIE_INST/467l3g/cdi_safari_books_v2_9781835089989), a few key characteristics that suggest a piece of code is smelly are:

* It’s difficult to understand what it does or why it does it.
* You or people on your team avoid working with it.
* It’s slower to modify than other areas or tends to break when modified.
* It’s hard to test or debug.

Spend a little bit of time reading over the code used in the practical you have chosen, and see if you can identify any bits of code where this is true. Are solutions convoluted and break when changed? Are magic numbers, strings, or other hard-coded elements getting in the way of changes or re-use? Is code difficult to understand or follow? Are there dependencies bewteen objects that make things difficult to isolate and debug?

You might even find these problems in the template code, not just your own. Some common refactor projects for this class to get you started:
* Adding an FSM to replace nested if statements.
* Replacing polling with event-driven code where suitable.
* Better architecture through seperating game, UI, or other logic so less objects know need to know about each other.
* Placing repeating code into a function that is called, or breaking up Update() and FixedUpdate() code into additional methods
* Anything else you can think of that applies more suitable techniques to older pracs. As we say, you can even edit the template code, just as long as you can explain what you are doing ;).

### Writing a plan
Once you've identified a problem (or a few problems), make a note of them. Something succinct, such as "This mechanic is difficult to modifiy, because its code is repeated throughout a number of scripts". Think about how you are going to solve the problem.

Now, start making a plan for your refactor. We will leave the exact documentation up to you, but you essentially want to create notes and diagrams that will help keep you on task and guide your refactor. Some examples include:
* Comments in the initial code.
* ERDs
* FSMs

As you create these documents, you'll likely find that you are refining your plan.

## Checkpoint! Save, Commit and Push your work now

## To receive half-marks, show your demonstrator:
* Which practical you've chosen, and the smells/technical debt you've identified.
* Your planning documents for refactoring.

## Step 3 - Refactor! (40 min)
Now, do your refactoring. Following your plan (but not being afraid to make changes), make the modifications to the code to implement your refactor. Make sure you are pushing things to Github, as your demonstrator will need to see evidence of your changes.

Note: If functionality is improved as a result of your refactoring, that is absolutely fine. You can even improve accessibility. However, the emphasis should be on refactoring.

Get ready to tell your demonstrator about your refactor. You will only have a couple of minutes to explain it to them, so make sure you are ready before calling them over.

## To receive full marks for this prac, show your demonstrator:
* Your refactored project.
* Evidence of your refactor (such as git history).
* Why you made the changes and how it improved performance and/or architecture.

## Further reading
* [Gorbachenko, P. (2024). Code Refactoring: Why, When and How Explained. Enkonix](https://enkonix.com/blog/code-refactoring/)
* [Eland, M. (2023). Refactoring with C#. Packt Publishing](https://multisearch.mq.edu.au/permalink/61MACQUARIE_INST/467l3g/cdi_safari_books_v2_9781835089989)
