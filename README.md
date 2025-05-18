# ProxycontractImplementation

UUPS (Universal Upgradeable Proxy Standard)

WHAT PROXY SMART CONTRACT IS.
We all khow that the blockchain on its own is immutable, anything it holds already cannot be changed. This property of blockchain has a tremendous advantage, but it becomes so problematic when ever we want to upgrade our already existiing contract or maybe fix bugs on them. This issue brought about the proxy smart contract. It is simply a way to fix bugs, upgrade our codes and also make changes to them on the blockchain. There has been stansards to achieving this, but i will be disscusing UUPS standards.

UUPS standards
This is one of the universal way of implementing proxy. its main difference to other standards is that the function that upgrades the implementaion contract is writing withing the implementation contract itself, and not in the proxy contract. Below is a comprehensive explanation of how this works.
This has two smart contracts, one is called proxy smart contract, while the second one is called the implementation smart contract. The implementation smart contract holds all the fuction and logics to be implemented, including the function that changes the implementation address. And then, the proxy stores the impplementation smart contract address, with just small logics that is enough to delegate call the implementation smart contract, so that its codes and logic could be visible to users.   
The implementation smart contract is deployed, then its contract address is  used to deploy the proxy smart contract which is delegating call to it. When the logic is to be upgraded, we then deploy another implementation smart contract, and pass its contract address to the fuction that allows upgradability in the first implementation smart contract.
