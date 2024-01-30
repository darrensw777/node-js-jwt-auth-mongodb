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

## STEP 2: Install Git and clone repository:

### To install Git, run the commands below:

```
sudo apt-get update -y OR sudo yum update -y
apt-get install git -y OR yum install git -y
```

### Just to verify Git has installed correctly:

```
git --version
```

## Now we will clone our repo onto the instance

```
git clone https://github.com/darrensw777/node-js-jwt-auth-mongodb.git
cd node-js-jwt-auth-mongodb
npm install
```

### Now let's start the server:

```
nodemon server.js
```
