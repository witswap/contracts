# Contracts

This repository contains the two contracts used for the WitSwap project.

# The eWIT contract: eWIT.sol

eWIT.sol is the contract launched on the Ethereum network and built on the standard ERC-20 standard with additional minting and pausing capabilities by identities whome are assigned the minter or pauser role.

The eWIT contract has been audited by Red4Sec (see eWit_Security Audit Report_Final_Mainnet.pdf) and is deployed at 0x56EE175FE37CD461486cE3c3166e0CaFCcd9843f. 

# The liquidity rewards contract: Farm.sol

Farm.sol is a contract modified from https://github.com/ltonetwork/uniswap-farming/blob/master/contracts/Farm.sol

Modifications:  
  1. Removed usage of SafeMath which is obsolete from Solidity ^0.8.0  
  2. Added a defund function usuable by the contract owner only  
  3. Added a variable that can be used to close deposits after a certain block has passed  
  4. Added a variable to lock the LP deposits in the contract until a specified block number has passed  
  5. Added an event for funding and defunding  
