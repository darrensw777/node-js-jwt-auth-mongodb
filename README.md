# Node.js MongoDB – User Authentication & Authorization example with JWT & Mongoose

## Project setup

## STEP 1: Install node version manage (nvm) using the following commands:

```
sudo su -
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

### Activate nvm and run the following to use it now:

```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

### Use nvm to install NodeJS (this is correct, not npm):

```
nvm install node
```

### Test that Node and npm are installed correctly:

```
node -v
npm -v
```

### Now install npm and pm2 globally

```
npm inmstall npm -g
npm install pm2 -g
```

### To install Git, run the commands below:

```
sudo apt-get update -y OR sudo yum update -y
apt-get install git -y OR yum install git -y
```

### Just to verify Git has installed correctly:

```
git --version
```

## STEP 2: Install Git and clone repository:

## Now we will clone our repo onto the instance

### IMPORTANT

We now need to go back to being a user, type:

```
exit
```

Your cursor will be ubutu@ip-\***\*\*\*\*\*\***

```
git clone https://github.com/darrensw777/node-js-jwt-auth-mongodb.git
cd node-js-jwt-auth-mongodb
npm install
```

### Now let's start the server:

```
pm2 start server.js
```

## Configure AWS endpoint

### Set a security group and edit INBOUND rules to add:

| Type       | Protocol | Port range | Source        |
| ---------- | -------- | ---------- | ------------- |
| SSH        | TCP      | 22         | Anywhere-IPv4 |
| Custom TCP | TCP      | 8000-9000  | Anywhere-IPv4 |
| HTTP       | TCP      | 22         | Anywhere-IPv4 |
| HTTPS      | TCP      | 22         | Anywhere-IPv4 |

### Set a security group and edit OUTBOUND rules to add:

| Type        | Protocol | Port range | Source        |
| ----------- | -------- | ---------- | ------------- |
| All traffic | All      | All        | Anywhere-IPv4 |

### Now get the endpoint:

Look at your instance list and click the Instance ID
link which will take you to an overview.

On that page, look for: Public IPv4 address, combine that
with the port the app runs on to derive your url.

e.g.

http://34.244.202.78:8080

**NB HTTP, NOT HTTPS**
