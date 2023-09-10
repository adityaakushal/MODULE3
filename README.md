# AK47 token

The solidity code in the project explains the ERC20 contract functionalities.

## Description

In our solidity code , ERC20 smart contract is created using openzeppelin library where it makes it easier for us to create any token standard contracts. The token I created is called AK47 with symbol AK which is able to perform many functions (ERC20). Only the owner is able to mint tokens (we have added a modifier to mint function)

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., AK47.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/token/ERC20/extensions/ERC20Burnable.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract AK47 is ERC20, ERC20Burnable, Ownable {
    constructor() ERC20("AK47", "AK") {
        _mint(msg.sender, 1 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile AK47.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "AK47" contract from the dropdown menu, and then click on the "Deploy" button.


## Authors

Aditya K

@adityaaakushal@gmail.com

## License

This project is licensed under the MIT License
