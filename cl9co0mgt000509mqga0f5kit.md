# Earning.farm Platform exploited for almost  $1 million!

Earning.farm is a simple yield machine for holders of Ethereum (ETH), Wrapped Bitcoin (WBTC), and USD Coin (USDC). It was exploited for around 750 ETH on October 14, 2022, at 12:27:11 PM +UTC.
The attacker with the address, "0xdf31F4C8dC9548eb4c416Af26dC396A25FDE4D5F", managed to withdraw all ethers (ETH) stored in the Earning.farm EFLeverVault contract that was designed to act as collateral, using a flash loan attack.

>The attack happened because the contract did not verify that flashloan callbacks were actually initiated by the protocol, allowing the attacker to tell the protocol to withdraw large amounts of funds. -Daniel Von Fange.

The contract was attacked twice, and the first attack was blocked and frontrun by an MEV bot "0xa57", which got 480 ETH and is known to have returned the funds, and the second attack was completed successfully with a profit of 268 ETH for the attacker.

The EFLeverVault handles withdrawal by making a flash loan to itself for that amount, when it receives the flash loan, it withdraws that amount of funds and leaves it in ETH on the contract. After the flash loan is over, the contract sends all ETH on the contract to the user. 
The attacker exploited this by making a tiny deposit, then a huge outside flashloan, causing the protocol to make a large withdrawal of ETH to itself. The attacker then withdrew their small amount of ETH, and the protocol sent both the small and the large amount it had to the attacker.


These attacks happened on Friday 14th October 2022, with the transaction details below.
> - [First attack transaction details](https://etherscan.io/tx/0x1f1aba5bef04b7026ae3cb1cb77987071a8aff9592e785dd99860566ccad83d1)
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666020958688/uI26E4kpW.png align="left")

- [Second attack transaction details](https://etherscan.io/tx/0x160c5950a01b88953648ba90ec0a29b0c5383e055d35a7835d905c53a3dda01e) 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666021041268/LWfU92kd6.png align="left")


More information about the hack.

%[https://twitter.com/Supremacy_CA/status/1581012823701786624]

%[https://twitter.com/danielvf/status/1580936010556661761]