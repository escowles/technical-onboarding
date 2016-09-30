# Code Guidelines

See https://github.com/projecthydra/hydra/blob/master/CONTRIBUTING.md#making-changes
and following.

* Github workflow, forking and branching
* Organizing your code
* Testing and test coverage
* Style guidelines
* Creating a pull request

## GitHub workflow, forking and branching

To start working on a Hydra codebase, you may wish to fork it to your own organization and then clone it locally. This will allow you to push your work up for review and for pull requests. The advantage of forking existing codebases is that you can do so without asking anyone and get started quickly. The disadvantage is that there's a risk of writing code that only lives in your fork, which -- if you wind up running this in production, or pointing other production code at your fork -- is a surefire way to make your work difficult to upgrade. You will probably want to request access to push your work directly to Hydra codebases (see [formalities](formalities.md)).

## Testing and test coverage

Many developers in the Hydra community practice [test-driven development](https://en.wikipedia.org/wiki/Test-driven_development), and you will notice as you begin submitting pull requests that the common code review process requires that you cover all code changes with tests; this is equally true of bugfixes, features, and refactoring. We tend to use RSpec as our testing tool of choice, with Capybara for feature tests, and our tests tend to conform to [community-driven testing guidelines](http://betterspecs.org/). All of our codebases on GitHub integrate with the Travis continuous integration service, which allows reviewers to see if changes made in pull requests have a passing test suite. We also tend to use Coveralls to determine whether the proposed changes have increased or decreased overall code coverage.

## Style guidelines

The Hydra community uses a somewhat modified version of the default Ruby style conventions provided by the Rubocop tool. If your pull request contains style violations, continuous integration builds will fail quickly and your work will be in an unmergeable state. Fortunately, it's very easy (and fast) to check this in your development environment. Run the `rubocop` command to see if your changes pass muster. If they do not, Rubocop also supports an auto-fix flag for some violations. To do this, run `rubocop -a` -- but we recommend committing your changes first, because though this seldom happens, Rubocop can sometimes "fix" your code into a state that causes tests to fail. Don't worry about having to commit earlier, or more, than you intended; you can always squash your commits later.

## Additional resources

The [Hydra Camp Resources List](https://docs.google.com/document/d/1wnpJBS-Q9Yswp7r2fGfzvOzjjz0C971INU3pDfgZd8k/edit#heading=h.avateqba3goc)
has links to lots of good resources on general Ruby information, IDEs, data models, example Hydra
heads, etc.
