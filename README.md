# blockchain-developer-bootcamp-final-project

This project demonstrates a basic Hardhat use case. It comes with a custom .sol contract, no tests :/ oyo w that, a custom script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

I buidled a website called the 🩸SARDAUKAR BOOTCAMP🩸 --- it'll be a place where anyone on the internet can chant to the maker and have that data saved on the blockchain through an Ethereum smart contract.

Try running some of the following tasks:

```shell
npx hardhat accounts
npx hardhat compile
npx hardhat clean
npx hardhat test
npx hardhat node
node scripts/sample-script.js
npx hardhat help
```
1. Using Hardhat (assuming NODE/NPM is already on sys)
mkdir my-wave-portal
cd my-wave-portal
npm init -y
npm install --save-dev hardhat
2. Run:
npx hardhat
3. Choose the option to create a sample project. Say yes to everything.
The sample project will ask you to install hardhat-waffle and hardhat-ethers. These are other goodies we'll use later :).
Go ahead and install these other dependencies just in case it didn't do it automatically.
npm install --save-dev @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers
- DO NOT FORGET THIS INSTRUCTION FROM HARDHAT!!!
-- You need to install these dependencies to run the sample project:
  npm install --save-dev "hardhat@^2.6.8" "@nomiclabs/hardhat-waffle@^2.0.0" "ethereum-waffle@^3.0.0" "chai@^4.2.0" "@nomiclabs/hardhat-ethers@^2.0.0" "ethers@^5.0.0"
4. Finally, run npx hardhat accounts 
- and this should print out a bunch of strings that look like this:
0xBLAHBLAHRANDOMaDDRESS9720
5. To make sure everything is working, run:
 npx hardhat compile
Then run:
npx hardhat test
6. Open the code for the project now in your favorite code editor
7. Delete the file sample-test.js under test.  Also, delete sample-script.js under scripts. Then, delete Greeter.sol under contracts. Don't delete the actual folders!
---
Writing Contract
1. Create a file named sardaukar.sol under the contracts directory in your code editor

Init Blockchain env to Test
1. Go into the scripts directory and make a file named run.js
2. Run: npx hardhat run scripts/run.js
**Run this any time code is altered to ensure its functionality
---
Running Local Node
1. In new terminal cd into proj then run: npx hardhat node
2. Now the command we're going to run to deploy locally is:
npx hardhat run scripts/deploy.js --network localhost
---
- Create a replit profile
-- you can fork this proj here: https://replit.com/@adilanchian/waveportal-starter-project
- create an Alchemy account & create a DEVELOPMENT app using the RINKEBY testnet under the ETH Network
- add your PRIVATE Metamask Key + DEVELOPMENT Alchemy key to your hardhat.config,js file
- Run: npx hardhat run scripts/deploy.js --network rinkeby to deploy to the Rinkeby testnet
RECORD WHAT IS OUTPUT TO YOUR TERMINAL
WavePortal address:  0xBLAHBLAHBLAH50763
-- working in REPLIT going forward
