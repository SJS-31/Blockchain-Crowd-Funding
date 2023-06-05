## Getting Started

Create a project using this example:

```bash
npx thirdweb create --contract --template hardhat-javascript-starter
```

You can start editing the page by modifying `contracts/Contract.sol`.

To add functionality to your contracts, you can use the `@thirdweb-dev/contracts` package which provides base contracts and extensions to inherit. The package is already installed with this project. Head to our [Contracts Extensions Docs](https://portal.thirdweb.com/contractkit) to learn more.

## Building the project

After any changes to the contract, run:

```bash
npm run build
# or
yarn build
```

to compile your contracts. This will also detect the [Contracts Extensions Docs](https://portal.thirdweb.com/contractkit) detected on your contract.

## Deploying Contracts

When you're ready to deploy your contracts, just run one of the following command to deploy you're contracts:

```bash
npm run deploy
# or
yarn deploy
```

## Releasing Contracts

If you want to release a version of your contracts publicly, you can use one of the followings command:

```bash
npm run release
# or
yarn release
```

## Join our Discord!

For any questions, suggestions, join our discord at [https://discord.gg/thirdweb](https://discord.gg/thirdweb).

## Terminal Cmd
WEB3
npx thirdweb@latest create --contract
npm install dotenv

Client
npx thirdweb create --app

## CrowdFunding.sol

createCampaign:

    mapping(uint256 => Campaign): campaign[0] to access the campaign
    _owner: _ is used to make sure taht this parameter is only for this func
    string memory _title: used to declare a string variable that is stored in memory (temperorily) rather than in storage.
    public returns (uint256): In solidity we need to specify if the function is to be used by frontend or just internally, here we declare it as public and return the id of the campaign

donateToCampaign:
    uint256 _id: Id of the campaign for which you want to donate
    payable: Keyword that determines that there will be transaction of crypto in this func

getDonators:(Who donated to a specific campaign)
    view: Keyword used just to view
    uint256 _id: Id of the specific campaign
    We pass these as parameter address[] donators; uint256[] donations;

getCampaigns: 
    Campaign[]: Takes array of campaigns
    Campaign[] memory allCampaigns = new Campaign[](numberOfCampaigns): Created a new variable allcampaigns which is a array of multiple campaign structure, here we are creating empty array with as many empty elements as there are actual campaigns numberofcampaigns.
    
