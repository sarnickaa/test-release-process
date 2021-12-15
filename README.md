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
3. merge and squash will be performed
4. A Github Action running Release Please (https://github.com/googleapis/release-please#release-please) will create a 'release-type' PR on each push to main. This PR will:
    - automatically generate a changelog entry for all relevant 'feat/bugfix/hotfix' type commits to main made since the last tagged release. 
    - update version files in semver format
5. When reviewed and mereged, this 'release-type' PR will:
    - generate a tag for the release
    - checks in all above release changes
    - updates Github Release Notes

### Adding something 

- New list
- merge linked test
- manual release test
- yet another release test
- so many changes
- many change. much joy.
