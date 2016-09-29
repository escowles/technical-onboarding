# Code Review

See https://github.com/projecthydra/hydra/blob/master/CONTRIBUTING.md#merging-changes

* Code review elements
* Responding to comments
* Squashing/rebasing
* Norms for merging pull requests

## Code review elements

Pull requests are evaluated in many different ways; fortunately, we have tools to help us with code review so that human review can focus on overall code quality and maintainability. For instance, we use:

* TravisCI, to ensure the test suite is passing
* Rubocop, to be consistent w/ a baseline of Ruby style conventions
* Coveralls, to ensure code changes are covered by test changes
* Hound, to be consistent w/ Javascript and CSS style conventions
* CodeClimate, to flag obvious code smells early for remediation
