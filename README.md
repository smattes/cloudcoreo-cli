# CloudCoreo CLI
======================================================================
## Install CloudCoreo CLI tool

Installation is simple and managed via NPM. For a global install (reccomended) run:

```
npm install -g cloudcoreo-cli
```
# Configuration

To configure cloudcoreo-cli you must have a CloudCoreo account. If you do not, please sign up for one

[!https://www.cloudcoreo.com/](You can sign up here)

After completing the registration, you can 'login' with the CloudCoreo cli.

```
coreo login --username <my_cloudcoreo_username>
```

This will prompt you for your password.

Assuming your credentials entered are accurate, a `config` file will be create in `$HOME/.cloudcoreo/`

Each login will invalidate all other cli instantiations forcing you re-login on eaech machine you run from.
## Commands

The following is a list of commands that can be run with the CLI tool. This is auto-generated.
### Command: **coreo**

#### Options

```
-h, --help output usage information
-V, --version output the version number
```

### SubCommands

#### SubCommand: init

 work pertaining to creating a new AppStack init
#### Options

```
-h, --help output usage information
-V, --version output the version number
-D, --directory <fully-qualified-path> the working directory
```
#### Actions

##### Action: new-stack

  new description

###### Options:

```
-h, --help output usage information
-s, --stack-type <stack type> What will this stack be? (server | stack)
```
###### Examples:

```
$ new-stack -s server
$ new-stack --stack-type stack
```
#### SubCommand: stack

 work on existing AppStacks stack
#### Options

```
-h, --help output usage information
-V, --version output the version number
-D, --directory <fully-qualified-path> the working directory
```
#### Actions

##### Action: add

  Add a sibling stack

###### Options:

```
-h, --help output usage information
-s, --stack-type <stack type> What will this stack be? (server | stack)
-n, --stack-name <stack name> The name you would like to give to the sibling stack
-g, --from-git <git ssh url> The git ssh url from which this stack will be extended.
```
###### Examples:

```
Add a VPN server
$ coreo -D "/tmp/mystack" stack add -s "server" -g "git@github.com:CloudCoreo/servers-vpn.git" -n "vpn"
$ coreo -D "/tmp/mystack" stack add --stack-type "server" --from-git "git@github.com:CloudCoreo/servers-vpn.git" -stack-name "vpn"
```
##### Action: extend

  Extend a stack

###### Options:

```
-h, --help output usage information
-g, --from-git <git ssh url> The git ssh url from which this stack will be extended.
```
###### Examples:

```
Extend the CloudCoreo VPC
$ coreo -D "/tmp/mystack" stack extend -g git@github.com:cloudcoreo/cloudcoreo-vpc
```
