# GitHub API QA test

Please create the three integration tests for the [GitHub GraphQL API](https://developer.github.com/v4/) that are specified below.

You may find it helpful to explore the API using Github's public [GraphQL explorer](https://developer.github.com/v4/explorer/) before writing the tests.

## Instructions
 - Please approach your code architecture as if this will be the beginning of a large QA project.
 - Tests should include multiple assertions where appropriate.
 - The tests can be written in any language you like and with any GraphQL client.
 - Please use a test framework, you may use any that you like e.g. [jest](https://jestjs.io/).
 - You can clone [this Github repository](https://github.com/sol-x/github-qa-test.git) as a starting point or create your own git repository using `git init` if preferred.
 - Please provide a script so we can run the tests using one or two commands e.g. `yarn install && yarn test`.
 - You may assume that a GitHub graphql token is available in the environment variable `GITHUB_GRAPHQL_TOKEN`. You will need to [generate your own GraphQL token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line) and set it at this environment variable before running the tests e.g.

        export GITHUB_GRAPHQL_TOKEN=mytokengoeshere

## Tests to implement

### Test 1, verify list of stargazers
 - Please get a list of the users that have starred this repository: [sol-x/github-qa-test](https://github.com/sol-x/github-qa-test).
 - Please verify that this list includes *at least* the github logins, `insidewhy` and `sxwei123`, but note that it may contain more stargazers.

### Test 2, verify list of stargazers locations
 - Please verify that all of the users who starred the repository above live in a different location to each other.

### Test 3, verify information about issues assigned to project
 - Please verify that all of the issues belonging to the repository [sol-x/github-qa-test](https://github.com/sol-x/github-qa-test):
   - Are not closed.
   - Are assigned to exactly one github user, and each assigned to the *same* github user as every other issue.
   - That there are at least two issues.

## Submitting your solution

Please zip/tar the entire test directory and email your solution back to us. Please do not fork the project on git or submit a pull request with your solution as we it to remain private.

We would like it if you would submit your solution as multiple git commits with descriptive commit messages.
