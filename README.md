## Cross-Chain Bridge: Moving ERC20 Tokens from Goerli to Mumbai via fxPortal

# Welcome to the ERC20 Goerli to Mumbai Bridge project, showcasing the utilization of fxPortal contracts for seamless ERC20 token transfers between the Goerli and Mumbai networks.

# Bridging Process:

* Begin by running npm i to conveniently install the required dependencies.
* Safeguard your private key in the .env.examples file, subsequently renaming it to .env once the insertion is complete.
* Employ the command npx hardhat run scripts/deploy.js --network goerli to initiate the deployment of the ERC20 contract.
* Capture the newly deployed contract address and insert it into the tokenAddress variable in the other scripts.
* Don't forget to provide your public key.
* Execute npx hardhat run scripts/mint.js --network goerli to generate tokens into your wallet.
* Run npx hardhat run scripts/approveDeposit.js --network goerli to grant approval and transfer your tokens to the Polygon network.
* Allow a window of 20-30 minutes for the tokens to be visible in your Polygon account.
* Employ polyscan.com to monitor your account for the token arrival. Once confirmed, access the transaction to obtain the Polygon contract address.
* Incorporate this Polygon contract address into your getBalance script's tokenAddress.
* Finally, run npx hardhat run scripts/getBalance.js --network mumbai to view your new Polygon balance.