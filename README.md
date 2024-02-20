### smart contracts that have been deployed : https://mumbai.polygonscan.com/address/0xA9dc375a9d4Ea1a397Cd6e17a7653FA6B9Bf49F8#readContract

##### Create a new folder named as constants and inside that add a new file named index.js. Add these lines to the index.js file: 
```
const { ethers } = require("hardhat");

const LINK_TOKEN = "0x326C977E6efc84E512bB9C30f76E30c160eD06FB";
const VRF_COORDINATOR = "0x8C7382F9D8f56b33781fE506E897a4F1e2d17255";
const KEY_HASH =
  "0x6e75b569a01ef56d18cab6a8e71e6600d6ce853834d4a5748b720d06f878b3a4";
const FEE = ethers.parseEther("0.0001");
module.exports = { LINK_TOKEN, VRF_COORDINATOR, KEY_HASH, FEE };

```

#### The values we got for this are from here and are already provided to us by Chainlink.

#### Compile the contract, open up a terminal pointing at hardhat-tutorial directory and execute this command:

```
npx hardhat compile
```

#### To deploy, open up a terminal pointing at hardhat-tutorial directory and execute this command: 

```
npx hardhat run scripts/deploy.js --network mumbai
```
