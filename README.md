# Smart-Contract-Vulnerabilities---Security-
## 1. Reentrancy Attack 
    Check how to do reentrancy attack with reentrancy_vulnarable_contract . 
    reentrancy_vulnarable_contract is not work compiler 0.8.7 . Its work 0.6.10 compiler.
    reentrancy_corrected - After fixed reentracny vulnerability. 
    

### Preventive methods of reentrancy attack
    1. Use openzappling nonReentrant modifier.
    2. Update the state balance variable before sending the transaction.
    3. Or else you custom modifier as given in reentrancey_corrected.sol file.
    

## 2. Arithmatic Overflow & Underflow
    uint256 x  maximum number is 2**256-1 . if add 1 to x its become 0 . if add 2 to x , x = 1 and so on.  This is overflow.
    
    uint256 y minimum number is 0 . but if y = 2-3 = -1 . But it eventually becomes 2**256 -1 . This is underflow
    
    likewise unit128 , uint64 , uint32 , uint16, uint8 can be overflow and underflow
 
 ### Preventive Methods of Arithmatic Overflow & Underflow
    Use SafeMath openzappling library for arithmatic operations.
  
 ## 3. Selfdestruct attack

    if your contract have address address(this).balance solidity command this might be a vulnerability.
    
    
 ### Preventive methods of selfdestruct attack
    
    If you want to get the balance then its better to declare a uint varibale balance and set it to balance += msg.value . 
 
 
 ## 4. Block Timestamp Manipulation
 
    Miners are able to manipulate the block.timestamp under these 2 constraints. 
       1.The next timestamp is after the last block timestamp
       2.The timestamp can not be too far into the future
        
       Average blocktime is about 13 seconds. Here we use 15 seconds rule of block.timestamp. Thats mean if your program not affecting varying 
       the 15 seconds then its ok to use block.timestamp.
       
## tx.origin phishing attack
       If code exists tx.origin then it might be vulnerable to attack. So better to use msg.sender instead of tx.origin
    
    
    
    
    
   

