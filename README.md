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
•State Variables (mixName, mixAbbry, TotalTokens) name is represent the token, the next is abbreviation of token, and the last is total tokens
•Mapping variable:balances (mapping): Maps addresses to their respective token balances. Each address can have an associated balance of tokens. 
The mapping allows you to look up the balance of an address quickly.
•Mint function: The mint function allows for the creation of new tokens. It takes two parameters: addrss (the address to which the tokens will be minted) and value (the number of tokens to mint).
•Burn function:The burn function allows for the destruction of tokens. It takes two parameters: addrss (the address from which tokens will be burned) and value (the number of tokens to burn).
