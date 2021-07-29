<a name="module_src/index"></a>

## src/index
Module providing GitHub API calls.


* [src/index](#module_src/index)
    * [~authenticate(gitHubOAuthToken)](#module_src/index..authenticate) ⇒ <code>Promise</code>
    * [~getDetailsForAuthenticatedUser()](#module_src/index..getDetailsForAuthenticatedUser) ⇒ <code>Promise</code>
    * [~getDetailsForUser(username)](#module_src/index..getDetailsForUser) ⇒ <code>Promise</code>
    * [~getReposForAuthenticatedUser(affiliation, page, per_page)](#module_src/index..getReposForAuthenticatedUser) ⇒ <code>Promise</code>
    * [~getReposForUser(username, page, per_page)](#module_src/index..getReposForUser) ⇒ <code>Promise</code>
    * [~getDetailsForOrg(org)](#module_src/index..getDetailsForOrg) ⇒ <code>Promise</code>
    * [~getMembershipForUser(org, username)](#module_src/index..getMembershipForUser) ⇒ <code>Promise</code>
    * [~getPermissionsForUser()](#module_src/index..getPermissionsForUser) ⇒ <code>Promise</code>
    * [~getTemplates(owner, repo, ref, path)](#module_src/index..getTemplates) ⇒ <code>Promise</code>
    * [~getDoc(owner, repo, ref, path)](#module_src/index..getDoc) ⇒ <code>Promise</code>
    * [~createRepo(repo, description, isPrivate)](#module_src/index..createRepo) ⇒ <code>Promise</code>
    * [~renameRepo(repo, description, isPrivate)](#module_src/index..renameRepo) ⇒ <code>Promise</code>
    * [~createOrgRepo(org, repo, description, isPrivate)](#module_src/index..createOrgRepo) ⇒ <code>Promise</code>
    * [~saveDoc(owner, repo, path, content, branch, message, [sha])](#module_src/index..saveDoc) ⇒ <code>Promise</code>
    * [~saveAsPullRequest(owner, repo, path, content, branch, message, title, [sha])](#module_src/index..saveAsPullRequest) ⇒ <code>Promise</code>
    * [~createFork(owner, repo, [organization])](#module_src/index..createFork) ⇒ <code>Promise</code>
    * [~searchCode(query, page, per_page)](#module_src/index..searchCode) ⇒ <code>Promise</code>
    * [~searchRepos(query, page, per_page)](#module_src/index..searchRepos) ⇒ <code>Promise</code>
    * [~getRepoContents(owner, repo)](#module_src/index..getRepoContents) ⇒ <code>Promise</code>
    * [~getRepoContentsByDrillDown(owner, repo)](#module_src/index..getRepoContentsByDrillDown) ⇒ <code>Promise</code>

<a name="module_src/index..authenticate"></a>

### src/index~authenticate(gitHubOAuthToken) ⇒ <code>Promise</code>
Authenticate the user for making calls to GitHub, using their OAuth token.
See [https://developer.github.com/v3/#authentication](https://developer.github.com/v3/#authentication)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| gitHubOAuthToken | <code>String</code> | The OAuth token from GitHub |

<a name="module_src/index..getDetailsForAuthenticatedUser"></a>

### src/index~getDetailsForAuthenticatedUser() ⇒ <code>Promise</code>
Get the details associated with the currently authenticated user.
See [https://developer.github.com/v3/users/#get-the-authenticated-user](https://developer.github.com/v3/users/#get-the-authenticated-user)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  
<a name="module_src/index..getDetailsForUser"></a>

### src/index~getDetailsForUser(username) ⇒ <code>Promise</code>
Get the details for a specific user.
See [https://developer.github.com/v3/users/#get-a-single-user](https://developer.github.com/v3/users/#get-a-single-user)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type |
| --- | --- |
| username | <code>String</code> | 

<a name="module_src/index..getReposForAuthenticatedUser"></a>

### src/index~getReposForAuthenticatedUser(affiliation, page, per_page) ⇒ <code>Promise</code>
Get the repos the user has explicit permission to access.
See [https://developer.github.com/v3/repos/#list-your-repositories](https://developer.github.com/v3/repos/#list-your-repositories)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| affiliation | <code>String</code> | User's relation to the repo |
| page | <code>Integer</code> | The page number |
| per_page | <code>Integer</code> | Repos per page |

<a name="module_src/index..getReposForUser"></a>

### src/index~getReposForUser(username, page, per_page) ⇒ <code>Promise</code>
Get the repos for a specific user.
See [https://developer.github.com/v3/repos/#list-user-repositories](https://developer.github.com/v3/repos/#list-user-repositories)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| username | <code>String</code> | The username |
| page | <code>Integer</code> | The page number |
| per_page | <code>Integer</code> | Repos per page |

<a name="module_src/index..getDetailsForOrg"></a>

### src/index~getDetailsForOrg(org) ⇒ <code>Promise</code>
Get the repos for a specific org.
See [https://developer.github.com/v3/repos/#list-organization-repositories](https://developer.github.com/v3/repos/#list-organization-repositories)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| org | <code>String</code> | The org name |

<a name="module_src/index..getMembershipForUser"></a>

### src/index~getMembershipForUser(org, username) ⇒ <code>Promise</code>
Get organization membership for a user
See [https://docs.github.com/en/rest/reference/orgs#set-organization-membership-for-a-user](https://docs.github.com/en/rest/reference/orgs#set-organization-membership-for-a-user)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| org | <code>String</code> | The org name |
| username | <code>String</code> | The user name |

<a name="module_src/index..getPermissionsForUser"></a>

### src/index~getPermissionsForUser() ⇒ <code>Promise</code>
Get the permissions for a specific user and repo.
See [https://developer.github.com/v3/repos/collaborators/#review-a-users-permission-level](https://developer.github.com/v3/repos/collaborators/#review-a-users-permission-level)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| req.owner | <code>String</code> | The repo owner |
| req.repo | <code>String</code> | The repo |
| req.username | <code>String</code> | The username |

<a name="module_src/index..getTemplates"></a>

### src/index~getTemplates(owner, repo, ref, path) ⇒ <code>Promise</code>
Get the CWRC Writer templates.
Default location is [https://github.com/cwrc/CWRC-Writer-Templates/tree/master/templates](https://github.com/cwrc/CWRC-Writer-Templates/tree/master/templates)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |
| ref | <code>String</code> | The branch/tag |
| path | <code>String</code> | The path |

<a name="module_src/index..getDoc"></a>

### src/index~getDoc(owner, repo, ref, path) ⇒ <code>Promise</code>
Get a document from GitHub.
See [https://developer.github.com/v3/repos/contents/#get-contents](https://developer.github.com/v3/repos/contents/#get-contents)
See [https://octokit.github.io/rest.js/#octokit-routes-repos-get-contents](https://octokit.github.io/rest.js/#octokit-routes-repos-get-contents)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |
| ref | <code>String</code> | The branch/tag |
| path | <code>String</code> | The path |

<a name="module_src/index..createRepo"></a>

### src/index~createRepo(repo, description, isPrivate) ⇒ <code>Promise</code>
Create a new repo for the authenticated user.
See [https://developer.github.com/v3/repos/#create](https://developer.github.com/v3/repos/#create)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| repo | <code>String</code> | The repo |
| description | <code>String</code> | The repo description |
| isPrivate | <code>String</code> \| <code>Boolean</code> | Is the repo private |

<a name="module_src/index..renameRepo"></a>

### src/index~renameRepo(repo, description, isPrivate) ⇒ <code>Promise</code>
Create a new repo for the authenticated user.
See [https://developer.github.com/v3/repos/#create](https://developer.github.com/v3/repos/#create)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| repo | <code>String</code> | The repo |
| description | <code>String</code> | The repo description |
| isPrivate | <code>String</code> \| <code>Boolean</code> | Is the repo private |

<a name="module_src/index..createOrgRepo"></a>

### src/index~createOrgRepo(org, repo, description, isPrivate) ⇒ <code>Promise</code>
Create a new repo for a specific org.
See [https://developer.github.com/v3/repos/#create](https://developer.github.com/v3/repos/#create)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| org | <code>String</code> | The org |
| repo | <code>String</code> | The repo |
| description | <code>String</code> | The description |
| isPrivate | <code>String</code> \| <code>Boolean</code> | Is the repo private |

<a name="module_src/index..saveDoc"></a>

### src/index~saveDoc(owner, repo, path, content, branch, message, [sha]) ⇒ <code>Promise</code>
Save (i.e. create or update) a document.
See [https://developer.github.com/v3/repos/contents/#create-or-update-a-file](https://developer.github.com/v3/repos/contents/#create-or-update-a-file)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |
| path | <code>String</code> | The path |
| content | <code>String</code> | The content |
| branch | <code>String</code> | The branch |
| message | <code>String</code> | The commit message |
| [sha] | <code>String</code> | The SHA |

<a name="module_src/index..saveAsPullRequest"></a>

### src/index~saveAsPullRequest(owner, repo, path, content, branch, message, title, [sha]) ⇒ <code>Promise</code>
Save (i.e. create) a document as a pull request.
See [https://developer.github.com/v3/pulls/#create-a-pull-request](https://developer.github.com/v3/pulls/#create-a-pull-request)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |
| path | <code>String</code> | The path |
| content | <code>String</code> | The content |
| branch | <code>String</code> | The branch |
| message | <code>String</code> | The commit message |
| title | <code>String</code> | The title of the pull request |
| [sha] | <code>String</code> | The SHA |

<a name="module_src/index..createFork"></a>

### src/index~createFork(owner, repo, [organization]) ⇒ <code>Promise</code>
Create a fork for the authenticated user.
See [https://octokit.github.io/rest.js/v18#repos-create-fork](https://octokit.github.io/rest.js/v18#repos-create-fork)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |
| [organization] | <code>String</code> | The organization |

<a name="module_src/index..searchCode"></a>

### src/index~searchCode(query, page, per_page) ⇒ <code>Promise</code>
Search for files based on a specific query.
See [https://developer.github.com/v3/search/#search-code](https://developer.github.com/v3/search/#search-code)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>String</code> | The query |
| page | <code>String</code> | The page number |
| per_page | <code>String</code> | Results per page |

<a name="module_src/index..searchRepos"></a>

### src/index~searchRepos(query, page, per_page) ⇒ <code>Promise</code>
Search for repos based on a specific query.
See [https://developer.github.com/v3/search/#search-repositories](https://developer.github.com/v3/search/#search-repositories)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| query | <code>String</code> | The query |
| page | <code>String</code> | The page number |
| per_page | <code>String</code> | Results per page |

<a name="module_src/index..getRepoContents"></a>

### src/index~getRepoContents(owner, repo) ⇒ <code>Promise</code>
Gets the contents (i.e. file structure) of a repo using the GitHub recursive tree method.
See [https://developer.github.com/v3/git/trees/#get-a-tree-recursively](https://developer.github.com/v3/git/trees/#get-a-tree-recursively)

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |

<a name="module_src/index..getRepoContentsByDrillDown"></a>

### src/index~getRepoContentsByDrillDown(owner, repo) ⇒ <code>Promise</code>
Gets the contents (i.e. file structure) of a repo by manually recursing.
Intended to be used if the github recursive option didn't work because the repository is too big.

**Kind**: inner method of [<code>src/index</code>](#module_src/index)  

| Param | Type | Description |
| --- | --- | --- |
| owner | <code>String</code> | The owner |
| repo | <code>String</code> | The repo |

