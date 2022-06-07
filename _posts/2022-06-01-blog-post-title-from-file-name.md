### Quick look at Trunk-based development

One day, bring the code you are working on to production will be as easy as pressing a button on your IDE. Meanwhile, development methodologies have the solution:
Trunk-based methodology. Also identifeid as TBD, a way of working whose main objective is to reduce time. As for example,
the time between your commit and the user feedback. To that end, TBD proposes  us to always work in the main development branch; or what is the same: Trunk.
So, here are some of the properties.

#### Trunk
Changes are uploaded once a day and always ready to version and deployment. If there is something we do not want to show, we must follow strategies like: features flags or branch by abstraction.

#### Git hooks
A tool that allows us to test before a git action. Inside ./git/hooks there are the files you can prepare. Example: if you would like to do tests automatically before a commit, you shall incate it in pre-commit file (exec youTestCommand)

#### Version by commit date
For this, it is necesary two components:
- Git Commit Plugin: it generates a file of properties when compiles with the information of the commit.
- "Your framework" Acurator. For example, Spring Boot acurator alows to sort by endpoints.

#### CI
TBD must implements Continuous Integration. CI server is executed every time we change the Trunk. If something goes wrong, it notifies immediately. Then 
you act in some predefined way by the team: rollback or automatic CI action.


And many more to tell. There are some related links:

#### Links
- [Feature-flags](https://thysniu.medium.com/coding-with-feature-flags-how-to-guide-and-best-practices-3f9637f51265)
- [Habits](https://trunkbaseddevelopment.com/observed-habits/)
- [If we do not TBD](https://trunkbaseddevelopment.com/youre-doing-it-wrong/)