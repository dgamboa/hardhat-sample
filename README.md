# Basic Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, a sample script that deploys that contract, and an example of a task implementation, which simply lists the available accounts.

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

# Documented Issues

* I ran into a chainId issue when trying to send ETH from one hardhat account to another on the Hardhat Network. I solved it using [this page](https://hardhat.org/metamask-issue.html) from Hardhat documenting the MetaMask issue. Effectively, I had to add an explicit chainId to the `hardhat.config` as follows:

```
networks: {
  hardhat: {
    chainId: 1337
  },
}
```
