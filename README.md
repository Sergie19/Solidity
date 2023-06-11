# ETH PROOF: Beginner EVM Course

This code represents a simple Ethereum smart contract for a token called "MyToken" Here's a breakdown of its functionality

## Description

It's important to note that this code is a minimal implementation and does not include crucial features such as access control, security checks. In a real-world scenario, you would need to consider additional functionality and best practices to ensure the contract's security and usability.

## Getting Started

### Installing

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., SergTokens.sol). Copy and paste the following code into the file:


### Executing program

contract MyToken {

// public variables here
string public mixName = "SERGIE";
string public mixAbbry = "SRE";
uint public TotalTokens = 0;

// mapping variable here
mapping(address => uint) public balances;

// mint function
function mint (address addrss, uint value) public {
    TotalTokens += value;
    balances[addrss] += value;
}

// burn function
function burn (address addrss, uint value) public {
    if (balances[addrss] >= value){
        TotalTokens -= value;
        balances[addrss] -= value;
    }
}
} 

* Step-by-step bullets


•First to compile the code you need to go in "Solidity Compiler" and click AUTO COMPILE in the left and click compile (in my case (SergTokens.sol).sol) button.

•Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left. Copy the "Account" contract from the dropdown menu, and then click on the "Deploy" button contract from(MyToken-SergTokens.sol).

•After the deploy in the lower left it will show the the "Deployed Contracts" and you need to inpute the account in BURN, MINT, BALANCES. (Put anything or whatever digit you want in Mint and click "TotalTokens") it will show the amount and if you want to remove it you need to put the digit in Burn it's always show in TotalTokens.



## Authors

Contributors names and contact info

Sergie Alvarez
61901325@ntc.edu.ph


## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
