# git subcommand for semver 

### Install
~~~
go get -u github.com/liangzuobin/git-semver
~~~

### Usage

A `-m` or `--message` is optional to specify a git tag message.

Current semver, acutally it finds the max(semver) and returns `v0.0.0` if no semver found.
~~~
➜  git-semver master ✗ git semver current
current semver v2.0.0
~~~

Patch, find current(max) semver and add its patch +1.
~~~
➜  git-semver master ✗ git semver patch
current version: v2.0.1, message: v2.0.1
~~~

Minor
~~~
➜  git-semver master ✗ git semver minor
current version: v2.1.0, message: v2.1.0
~~~

Major
~~~
➜  git-semver master ✗ git semver major
current version: v3.0.0, message: v3.0.0
~~~

BTW, rm all your local tags
~~~
git tag -d $(git tag -l)
~~~
