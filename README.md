# ETH Module 3

This Solidity program is a "Minting and Burning" program that shows how to Mint and Burn the Token that you created.

## Description

This only for my Final Assessment on Module 3 in metacrafters. It shows the MINTING and BURNING the Token.


### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at remix.ethereum.org/
* When you reach the site of remix.ethereum.org, create a new file then the last thing that you pur there should be .sol (e.g MyNFT.sol). Copy this code on your remix.
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyNFTToken {

    
    string public tokenName = "Justine Donn Angsantos";
    string public tokenAbbrv = "JDA";
    uint public totalSupply;

    
    mapping (address => uint) public Balances;

    
    function mint (address Address, uint value) public{
        totalSupply += value;
        Balances[Address] += value; 

    }
    function burn (address Address, uint value) public {
        if (Balances[Address] >= value){
        totalSupply -= value;
        Balances[Address] -= value;}
        else{


    }
    }
}
```

## Help

To run this code, you can click the "Solidity Compiler" tab in the left side bar. Make sure that your compiler is set to "0.8.18" and you can click the Compile on the lower left side bar in Advanced Configuration (Compile myNFT.sol).

Once you compile this code you can go to "Deploy & run transactions" in the left side bar then select in contract the "myNFTToken" because this is the name of my contract in my code. Then click the "Deploy" button.

Once you deploy the contract, you can go down then you can see the "Deployed Contracts" then click the left arrow then you can BURN, MINT and you can see your Balances.

You can run it properly, first copy the address in the next to "MYNFTTOKEN". Once you copy the address, first thing will you do is to MINT. Copy the address and put the value that you want (e.g Address: 0x0fC5025C764cE34df352757e82f7B5c4Df39A836 value: 100) then click transact. Once you done in MINTING, you can BURN your token by doing it again on the first thing you do in MINTING, if the value that you chose is higher in the value the you put in MINTING nothing will change on the value that you put because it's more than the value that you put in. To see your Total Balances go to the below of the "MINT" and copy the address and then click the "CALL"
```
command to run if program contains helper info
```

## Author

Justine Donn B. Angsantos

8215200@ntc.edu.ph


## License

This project is licensed under the [MIT] License.
