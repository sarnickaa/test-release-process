# test-release-process

## development workflow:
### pre-requisite: 
before starting the development workflow, a Github Issue must be opened.
The issue must be in BDD format and must be accepted. 

### development:
1. fork repository
2. clone forked repository to local machine
3. create your feature branch locally
4. check in their code
5. create pull request back to the original repository to main branch

## RELEASE:
1. Pull request (PR) to main should enforce the conventional commit format (as expected by sematic-release)
2. PR should pass unit tests and code coverage, code quality, and outstanding comment checks with the approval of at least one required reviewer.
3. merge and squash will be performed (potentially automated)
4. on merge to main, a github action will be initiated to run semantic-release
    - automatically generate a changelog entry
    - version file updates
    - generates tag
    - checks in all above release changes
    - updates github Releases
    - optionally: can update and publish a packaged version of the project
5. decision point: when should the release be executed?:
 - option 1: feature -> main via PR will initiate the semantic-release process
 - option 2 (MANUAL):       feature -> develop/release
                            develop/release -> main via PR will initiate the semantic-release process
 - option 3: option 2 executed on a cron schedule (monthly, bi-monthly, milestones)

### Adding something 

- New list
- merge linked test
- manual release test
- yet another release test
- so many changes
- many chnage. much joy.
