# Smart-Contract-Vulnerabilities---Security-
## Reentrancy Attack 
    Check how to do reentrancy attack with reentrancy_vulnarable_contract . 
    reentrancy_vulnarable_contract is not work compiler 0.8.7 . Its work 0.6.10 compiler.
    reentrancy_corrected - After fixed reentracny vulnerability. 
    

## Preventive methods of reentrancy attack
    1. Use openzappling nonReentrant modifier.
    2. Update the state balance variable before sending the transaction.
    3. Or else you custom modifier as given in reentrancey_corrected.sol file.
    

## Arithmatic Overflow & Underflow
    uint256 x  maximum number is 2**256-1 . if add 1 to x its become 0 . if add 2 to x , x = 1 and so on.  This is overflow.
    
    uint256 y minimum number is 0 . but if y = 2-3 = -1 . But it eventually becomes 2**256 -1 . This is underflow
    
    likewise unit128 , uint64 , uint32 , uint16, uint8 can be overflow and underflow
    
   

