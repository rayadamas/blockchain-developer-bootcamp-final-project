# blockchain-developer-bootcamp-final-project

This project demonstrates a basic Hardhat use case. It comes with a custom .sol contract, a custom script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

I buidled a website called the 🩸SARDAUKAR BOOTCAMP🩸 --- it'll be a place where anyone on the internet can chant to the maker and have that data saved on the blockchain through an Ethereum smart contract.

SETTING UP LOCAL ETH ENVIRONMENT
-This is the area where you will be able to compile & test your smart contract code.
(Note)
node/npm is REQUIRED to implement this project, Click [here](https://hardhat.org/tutorial/setting-up-the-environment.html) to install.

WORKING FROM LOCAL TERMINAL

1. Using Hardhat (assuming NODE/NPM is already on sys)
`mkdir mySampleProj`
`cd mySampleProj`
`npm init -y`
`npm install --save-dev hardhat`
2. Run created sample project:
`npx hardhat`
(Note)
Carefully read what is output and run commands accordingly.

3. Choose the option to create a sample project. Say yes to everything.
The sample project will ask you to install `hardhat-waffle` and `hardhat-ethers`
- DO NOT FORGET THIS INSTRUCTION FROM HARDHAT!!!
- You need to install these dependencies to run the sample project:
  `npm install --save-dev "hardhat@^2.6.8" "@nomiclabs/hardhat-waffle@^2.0.0" "ethereum-waffle@^3.0.0" "chai@^4.2.0" "@nomiclabs/hardhat-ethers@^2.0.0" "ethers@^5.0.0"`

4. Finally, run `npx hardhat accounts` 
- and this should print out a bunch of strings that look like this:
0xBLAHBLAHRANDOMaDDRESS9720

5. To make sure everything is working we  assure we can compile our contracts by running:
 `npx hardhat compile`
Next run:
`npx hardhat test`

Output should display the contents of the .sol contract code.

6. Open the code for the project now in your favorite code editor
7. Delete the file `sample-test.js` under test.  Also, delete `sample-script.js` under `scripts`. Then, delete `Greeter.sol` under contracts. Do NOT delete the actual folders!

---
**Writing Contract**
1. Create a file named `sardaukar.sol` under the contracts directory in your code editor

Initialize Local Blockchain Environment to Test
1. Go into the `scripts` directory and make a file named `run.js`
2. Run: `npx hardhat run scripts/run.js`
*Run this any time code is altered to ensure its functionality*

---
**Running Local Node**
1. In terminal window separate to your current workspace, cd into your proj then run: `npx hardhat node`
This will create a local Ethereum network that stays alive as long as the terminal window remains open.
2. Now the command we're going to run to deploy locally is:
`npx hardhat run scripts/deploy.js --network localhost`

(Note)
This is run from your `mySampleProj` directory in a terminal window _separate_ from the window hosting our local blockchain environment.

---
Working with REPLIT, METAMASK, & ALCHEMY going forward
1. Create a replit profile
- you can fork this project [here](https://replit.com/@rayadamas/sardaukarchantProj#.replit)

2. Metamask can be found [here](https://metamask.io/download.html)
- [test-ETH faucet](https://faucet.rinkeby.io/)
3. Create an Alchemy account & create a DEVELOPMENT app using the RINKEBY testnet under the ETH Network [here](https://alchemy.com/?r=b93d1f12b8828a57)
4. Add your PRIVATE Metamask Key + DEVELOPMENT Alchemy key to your `hardhat.config,js` file
- Reference final `hardhat.config.js` file for updated code where PRIVATE KEY values will be utilized
- Run: `npx hardhat run scripts/deploy.js --network rinkeby` to deploy to the Rinkeby testnet
_RECORD WHAT IS OUTPUT TO YOUR TERMINAL_
(Note)
Any changes to LOCAL contracts' code will need to be re-tested, then re-deployed. 
1. Deploy your scrpt again
2. Update the contract address on your Replit frontend
- Once re-deployed you must take the NEW contract address output to your terminal & add it to your `app.js` code via Replit under `const contractAddress`
- `yourSampleProj address:  0xBLAHBLAHBLAH50763`
3. Update the ABI file on our Replit frontend
- Locate the ABI code in your LOCAL code env via this path: `artifacts/contracts/yourSampleProj.sol/yourSampleProj.json`, then copy said code and paste said code under such path on Replit under this path: `./src/utils/yourSampleProj.json` 


*DO NOT COMMIT BARE PRIVATE KEYS TO GITHUB OR ANYWHERE*
`dotenv` is used in this example.

1. Withing your project directory run: `npm install --save dotenv`
2. Refer to `hardhat.config.js` for code skeleton
3. Create a `.env` file withing the projects directory.
Format is as follows:

STAGING_ALCHEMY_KEY=;
PROD_ALCHEMY_KEY=;
PRIVATE_KEY=;

4. Ensure `.env` is withing your `.gitignore` file
