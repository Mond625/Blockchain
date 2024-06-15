# Sol1_assessment_Villacorta

This Solidity program is a project assessment for getting started with Solidity

## Description

This program is a simple contract that creates tokens written in Solidity, 
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.



```javascript
//SPDX-License-Identifier:MIT
pragma solidity 0.8.18;

contract MyToken{

    //Public Variables
    string public Tokenname = "Ducats";
    string public tokenAbbrv = "DUC";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;
 
    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
}
    // burn function
    function burn(address _address, uint _value) public {
    if(balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
 }
    
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile " button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the contract below then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by inputting the address in the mint and setting initial values. Check the changes of totalSupply and balances. not set the address and value to burn also then check the changes again in totalSupply.
