# Free FlashLoan Starknet

Based on the sample implementation of flashloans in cairo I will implement a version without fees and a reentry basic protection based on the (balancer vault contract)[https://etherscan.io/address/0xba12222222228d8ba445958a75a0704d566bf2c8#code] on ethereum.

In this contract anyone can deposit any ERC20 token in a pool and flash borrowers can borrow as long as they return the borrowed amount + fee by the end of the transaction.

## Spec
Original repo was Based on: https://eips.ethereum.org/EIPS/eip-3156 New version based on https://etherscan.io/address/0xba12222222228d8ba445958a75a0704d566bf2c8#code

---

## Deploy

```
nile compile
nile deploy FlashLoanBorrower --alias <alias> --network <network>
nile deploy FlashLoanLender --alias <alias> --network <network>
```
---

## Test
```
pytest tests/test_flash_loan.py -s
```
---

## Deployment Addresses


## Credits

This repo is based on standard cairo contract library by [@OpenZeppelin](https://github.com/OpenZeppelin) : [Repo](https://github.com/OpenZeppelin/cairo-contracts)
