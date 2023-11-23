# Deploy on Fly.io

## Install flyctl

To deploy in on [fly.io](https://fly.io/), you'll need to install the [flyctl](https://fly.io/docs/hands-on/install-flyctl/) on your machine.

If you are on Github Codespaces: 

```bash
curl -L https://fly.io/install.sh | sh && export FLYCTL_INSTALL="/home/codespace/.fly" && export PATH="$FLYCTL_INSTALL/bin:$PATH"
```

Note that you will need to exec this *every time* you open a new codespace.

## Login

Next you need to auth on fly with your command line (You will need an account in fy.io):

```bash
flyctl auth login
```

If you are on Github Codespaces:

```bash
 flyctl auth login -t FLY_IO_AUTH_TOKEN
 ```

Where **FLY_IO_AUTH_TOKEN** is generated on [fly.io specific page](https://fly.io/user/personal_access_tokens). Note that for this repository is stored in a secret.

This command will tell you something like 

> failed opening browser. Copy the url (https://fly.io/app/auth/cli/URL) into a browser and continue

Click on the provided link to finish login.


## Build & Deploy 

to build fly app: 

```bash
 flyctl launch
 ```

 this command will gather all the information needed


 ```bash
 fly deploy 
 ```

 to deploy on Fly