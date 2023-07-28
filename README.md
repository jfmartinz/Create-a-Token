# Metacrafters: Solidity Assessment
> Project: Create a Token 

 ## ASSESSMENT REQUIREMENTS:

1. Your contract will have public variables that store the details about your coin (`Token Name`, `Token Abbrv.`, `Total Supply`)<br>
   
2. Your contract will have a mapping of addresses to balances (`address => uint`)<br>

3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the `“sender”` address by that amount<br>

4. Your contract will have a burn function, which works the opposite    of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the `“sender”`.<br>

5. Lastly, your burn function should have conditionals to make sure the balance of `"sender"` is greater than or equal 
       to the amount that is supposed to be burned.

## Excuting the program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the [Remix](https://remix.ethereum.org/) website.

---

*here is a basic contract file to get you started:*

```js
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
        // code here

    // mapping variable here
        // code here

    // mint function
        // code here

    // burn function
        // code here
}
```

You can find the solution [here](https://youtu.be/yfuMcRf1Ml4).



<details>
<summary>My Solution</summary>

```js
contract Token {
    string public tokenName = "jfmartinz";           
    string public tokenAbbreviation = "jmz";  
    uint public totalSupply = 0;       

    mapping(address => uint) public balances;  

  

    function mint(address account, uint value) public {
        totalSupply += value;          
        balances[account] += value;    
    }
    
    function burn(address account, uint value) public {
      if(balances[account] >= value){
        totalSupply -= value;          
        balances[account] -= value;    
      }  

    }

}
```

</details>

I recommend you to check this [repo](https://github.com/jfmartinz/web3Notes) before attempting this assessment.

**Author:**
Twitter: [@jfmartinz](https://twitter.com/jfmartinz)<br>
Github: [@jfmartinz](https://github.com/jfmartinz)<br>
Linkedin: [@jfmartinz](https://www.linkedin.com/in/jfmartinz/)

