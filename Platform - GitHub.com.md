 

# GitHub CLI

`gh` is GitHub on the command line. It brings pull requests, issues, and other GitHub concepts to the terminal next to where you are already working with `git` and your code.

![screenshot of gh pr status](https://user-images.githubusercontent.com/98482/84171218-327e7a80-aa40-11ea-8cd1-5177fc2d0e72.png)

GitHub CLI is available for repositories hosted on GitHub.com and GitHub Enterprise Server 2.20+, and to install on macOS, Windows, and Linux.

## Documentation

[See the manual](https://cli.github.com/manual/) for setup and usage instructions.

## Installation

### macOS

`gh` is available via [Homebrew][], [MacPorts][], [Conda][], [Spack][], and as a downloadable binary from the [releases page][].

#### Homebrew

| Install:          | Upgrade:          |
| ----------------- | ----------------- |
| `brew install gh` | `brew upgrade gh` |

#### MacPorts

| Install:               | Upgrade:                                       |
| ---------------------- | ---------------------------------------------- |
| `sudo port install gh` | `sudo port selfupdate && sudo port upgrade gh` |


## Configuration
Run gh auth login to authenticate with your GitHub account. Alternatively, gh will respect the GITHUB_TOKEN environment variable.

To set your preferred editor, use gh config set editor <editor>. Read more about gh config and environment variables.

Declare your aliases for often-used commands with gh alias set.

### GitHub Enterprise
GitHub CLI supports GitHub Enterprise Server 2.20 and above. To authenticate with a GitHub instance, run:

gh auth login --hostname <hostname>
To define this host as a default for all GitHub CLI commands, set the GH_HOST environment variable:

`export GH_HOST=<hostname>`
Finally, to authenticate commands in scripting mode or automation, set the GH_ENTERPRISE_TOKEN:

`export GH_ENTERPRISE_TOKEN=<access-token>`
 
    
    
## Tools:
- https://github.com/yusukebe/gh-markdown-preview

    

## gh

Work seamlessly with GitHub from the command line.

### Core commands

*   [gh auth](https://cli.github.com/manual/gh_auth) | 

*   [gh browse](https://cli.github.com/manual/gh_browse) | 

*   [gh codespace](https://cli.github.com/manual/gh_codespace) | 

*   [gh gist](https://cli.github.com/manual/gh_gist) | 

*   [gh issue](https://cli.github.com/manual/gh_issue) | 
*   [gh pr](https://cli.github.com/manual/gh_pr) | 

*   [gh release](https://cli.github.com/manual/gh_release) | 

*   [gh repo](https://cli.github.com/manual/gh_repo) | 


### Actions commands

*   [gh run](https://cli.github.com/manual/gh_run) | 

*   [gh workflow](https://cli.github.com/manual/gh_workflow) | 


### Additional commands

*   [gh alias](https://cli.github.com/manual/gh_alias) | 

*   [gh api](https://cli.github.com/manual/gh_api) | 

*   [gh completion](https://cli.github.com/manual/gh_completion) | 

*   [gh config](https://cli.github.com/manual/gh_config) | 

*   [gh extension](https://cli.github.com/manual/gh_extension) | 

*   [gh gpg-key](https://cli.github.com/manual/gh_gpg-key) | 

*   [gh label](https://cli.github.com/manual/gh_label) | 

*   [gh search](https://cli.github.com/manual/gh_search) | 

*   [gh secret](https://cli.github.com/manual/gh_secret) | 

*   [gh ssh-key](https://cli.github.com/manual/gh_ssh-key) | 

*   [gh status](https://cli.github.com/manual/gh_status) | 


### Options

<dl class="flags">

<dt>`--version`</dt>

<dd>Show gh version</dd>

</dl>

### Examples

<figure class="highlight">

    $ gh issue create
    $ gh repo clone cli/cli
    $ gh pr checkout 321

</figure>

</div>

</div>

[alias](https://cli.github.com/manual/gh_alias) | 


[delete](https://cli.github.com/manual/gh_alias_delete) | 


[list](https://cli.github.com/manual/gh_alias_list) | 


[set](https://cli.github.com/manual/gh_alias_set) | 


##### [api](https://cli.github.com/manual/gh_api) | 


##### [auth](https://cli.github.com/manual/gh_auth) | 


[login](https://cli.github.com/manual/gh_auth_login) | 


[logout](https://cli.github.com/manual/gh_auth_logout) | 


[refresh](https://cli.github.com/manual/gh_auth_refresh) | 


[setup-git](https://cli.github.com/manual/gh_auth_setup-git) | 


[status](https://cli.github.com/manual/gh_auth_status) | 


##### [browse](https://cli.github.com/manual/gh_browse) | 


##### [codespace](https://cli.github.com/manual/gh_codespace) | 


[code](https://cli.github.com/manual/gh_codespace_code) | 


[cp](https://cli.github.com/manual/gh_codespace_cp) | 


[create](https://cli.github.com/manual/gh_codespace_create) | 


[delete](https://cli.github.com/manual/gh_codespace_delete) | 


[edit](https://cli.github.com/manual/gh_codespace_edit) | 


[jupyter](https://cli.github.com/manual/gh_codespace_jupyter) | 


[list](https://cli.github.com/manual/gh_codespace_list) | 


[logs](https://cli.github.com/manual/gh_codespace_logs) | 


[ports](https://cli.github.com/manual/gh_codespace_ports) | 


[ports forward](https://cli.github.com/manual/gh_codespace_ports_forward) | 


[ports visibility](https://cli.github.com/manual/gh_codespace_ports_visibility) | 


[ssh](https://cli.github.com/manual/gh_codespace_ssh) | 


[stop](https://cli.github.com/manual/gh_codespace_stop) | 


##### [completion](https://cli.github.com/manual/gh_completion) | 


##### [config](https://cli.github.com/manual/gh_config) | 


[get](https://cli.github.com/manual/gh_config_get) | 


[list](https://cli.github.com/manual/gh_config_list) | 


[set](https://cli.github.com/manual/gh_config_set) | 


##### [extension](https://cli.github.com/manual/gh_extension) | 


[create](https://cli.github.com/manual/gh_extension_create) | 


[exec](https://cli.github.com/manual/gh_extension_exec) | 


[install](https://cli.github.com/manual/gh_extension_install) | 


[list](https://cli.github.com/manual/gh_extension_list) | 


[remove](https://cli.github.com/manual/gh_extension_remove) | 


[upgrade](https://cli.github.com/manual/gh_extension_upgrade) | 


##### [gist](https://cli.github.com/manual/gh_gist) | 


[clone](https://cli.github.com/manual/gh_gist_clone) | 


[create](https://cli.github.com/manual/gh_gist_create) | 


[delete](https://cli.github.com/manual/gh_gist_delete) | 


[edit](https://cli.github.com/manual/gh_gist_edit) | 


[list](https://cli.github.com/manual/gh_gist_list) | 


[view](https://cli.github.com/manual/gh_gist_view) | 


##### [gpg-key](https://cli.github.com/manual/gh_gpg-key) | 


[add](https://cli.github.com/manual/gh_gpg-key_add) | 


[list](https://cli.github.com/manual/gh_gpg-key_list) | 


##### [help](https://cli.github.com/manual/gh_help) | 


[environment](https://cli.github.com/manual/gh_help_environment) | 


[formatting](https://cli.github.com/manual/gh_help_formatting) | 


[mintty](https://cli.github.com/manual/gh_help_mintty) | 


[reference](https://cli.github.com/manual/gh_help_reference) | 


##### [issue](https://cli.github.com/manual/gh_issue) | 


[close](https://cli.github.com/manual/gh_issue_close) | 


[comment](https://cli.github.com/manual/gh_issue_comment) | 


[create](https://cli.github.com/manual/gh_issue_create) | 


[delete](https://cli.github.com/manual/gh_issue_delete) | 


[edit](https://cli.github.com/manual/gh_issue_edit) | 


[list](https://cli.github.com/manual/gh_issue_list) | 


[reopen](https://cli.github.com/manual/gh_issue_reopen) | 


[status](https://cli.github.com/manual/gh_issue_status) | 


[transfer](https://cli.github.com/manual/gh_issue_transfer) | 


[view](https://cli.github.com/manual/gh_issue_view) | 


##### [label](https://cli.github.com/manual/gh_label) | 


[clone](https://cli.github.com/manual/gh_label_clone) | 


[create](https://cli.github.com/manual/gh_label_create) | 


[delete](https://cli.github.com/manual/gh_label_delete) | 


[edit](https://cli.github.com/manual/gh_label_edit) | 


[list](https://cli.github.com/manual/gh_label_list) | 


##### [pr](https://cli.github.com/manual/gh_pr) | 


[checkout](https://cli.github.com/manual/gh_pr_checkout) | 


[checks](https://cli.github.com/manual/gh_pr_checks) | 


[close](https://cli.github.com/manual/gh_pr_close) | 


[comment](https://cli.github.com/manual/gh_pr_comment) | 


[create](https://cli.github.com/manual/gh_pr_create) | 


[diff](https://cli.github.com/manual/gh_pr_diff) | 


[edit](https://cli.github.com/manual/gh_pr_edit) | 


[list](https://cli.github.com/manual/gh_pr_list) | 


[merge](https://cli.github.com/manual/gh_pr_merge) | 


[ready](https://cli.github.com/manual/gh_pr_ready) | 


[reopen](https://cli.github.com/manual/gh_pr_reopen) | 


[review](https://cli.github.com/manual/gh_pr_review) | 


[status](https://cli.github.com/manual/gh_pr_status) | 


[view](https://cli.github.com/manual/gh_pr_view) | 


##### [release](https://cli.github.com/manual/gh_release) | 


[create](https://cli.github.com/manual/gh_release_create) | 


[delete-asset](https://cli.github.com/manual/gh_release_delete-asset) | 


[delete](https://cli.github.com/manual/gh_release_delete) | 


[download](https://cli.github.com/manual/gh_release_download) | 


[edit](https://cli.github.com/manual/gh_release_edit) | 


[list](https://cli.github.com/manual/gh_release_list) | 


[upload](https://cli.github.com/manual/gh_release_upload) | 


[view](https://cli.github.com/manual/gh_release_view) | 


##### [repo](https://cli.github.com/manual/gh_repo) | 


[archive](https://cli.github.com/manual/gh_repo_archive) | 


[clone](https://cli.github.com/manual/gh_repo_clone) | 


[create](https://cli.github.com/manual/gh_repo_create) | 


[delete](https://cli.github.com/manual/gh_repo_delete) | 


[deploy-key](https://cli.github.com/manual/gh_repo_deploy-key) | 


[deploy-key add](https://cli.github.com/manual/gh_repo_deploy-key_add) | 


[deploy-key delete](https://cli.github.com/manual/gh_repo_deploy-key_delete) | 


[deploy-key list](https://cli.github.com/manual/gh_repo_deploy-key_list) | 


[edit](https://cli.github.com/manual/gh_repo_edit) | 


[fork](https://cli.github.com/manual/gh_repo_fork) | 


[list](https://cli.github.com/manual/gh_repo_list) | 


[rename](https://cli.github.com/manual/gh_repo_rename) | 


[sync](https://cli.github.com/manual/gh_repo_sync) | 


[view](https://cli.github.com/manual/gh_repo_view) | 


##### [run](https://cli.github.com/manual/gh_run) | 


[cancel](https://cli.github.com/manual/gh_run_cancel) | 


[download](https://cli.github.com/manual/gh_run_download) | 


[list](https://cli.github.com/manual/gh_run_list) | 


[rerun](https://cli.github.com/manual/gh_run_rerun) | 


[view](https://cli.github.com/manual/gh_run_view) | 


[watch](https://cli.github.com/manual/gh_run_watch) | 


##### [search](https://cli.github.com/manual/gh_search) | 


[issues](https://cli.github.com/manual/gh_search_issues) | 


[prs](https://cli.github.com/manual/gh_search_prs) | 


[repos](https://cli.github.com/manual/gh_search_repos) | 


##### [secret](https://cli.github.com/manual/gh_secret) | 


[delete](https://cli.github.com/manual/gh_secret_delete) | 


[list](https://cli.github.com/manual/gh_secret_list) | 


[set](https://cli.github.com/manual/gh_secret_set) | 


##### [ssh-key](https://cli.github.com/manual/gh_ssh-key) | 


[add](https://cli.github.com/manual/gh_ssh-key_add) | 


[list](https://cli.github.com/manual/gh_ssh-key_list) | 


##### [status](https://cli.github.com/manual/gh_status) | 


##### [workflow](https://cli.github.com/manual/gh_workflow) | 


[disable](https://cli.github.com/manual/gh_workflow_disable) | 


[enable](https://cli.github.com/manual/gh_workflow_enable) | 


[list](https://cli.github.com/manual/gh_workflow_list) | 


[run](https://cli.github.com/manual/gh_workflow_run) | 


[view](https://cli.github.com/manual/gh_workflow_view) | 


