# Smart-Contract-Vulnerabilities---Security-
## 1. Reentrancy Attack 
    Check how to do reentrancy attack with reentrancy_vulnarable_contract . 
    reentrancy_vulnarable_contract is not work compiler 0.8.0 and above. Its work 0.6.10 compiler.
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

    if you get address(this).balance , it might be a vulnerability with selfdestruct . 
    
    
 ### Preventive methods of selfdestruct attack
    
    If you want to get the balance then its better to declare a uint varibale balance and set it to balance += msg.value . 
 
 
 ## 4. Block Timestamp Manipulation
 
    Miners are able to manipulate the block.timestamp under these 2 constraints. 
       1.The next timestamp is after the last block timestamp
       2.The timestamp can not be too far into the future
        
       Average blocktime is about 13 seconds. Here we use 15 seconds rule of block.timestamp. Thats mean if your program not affecting varying 
       the 15 seconds then its ok to use block.timestamp.
       
## 5. tx.origin phishing attack
       If code exists tx.origin then it might be vulnerable to attack. So better to use msg.sender instead of tx.origin
    
## 6. Hiding smart contracts
       Functions or costructor set the address that having smart contracts. Make sure those address exists the same code 
       published on etherscan or relevant blockchain scanner.
   
## 7. Hiding code - Another example
      Created a reentrancy vulnerability intentionally but no one is able withraw money from it.
 
## 8. Front running 
      hijacking the data from mem pools and do the same transaction with high gas . 
      You can see some flash loans are attacked by frontrunners. You can avoid this using flashbots.
      
## 9. Hack isContract
      There is a assembly code which can be used to if there is contract on etherium address. 
      Here you can bypass it calling it when deploying the contract. 
      
## 10. Random number hacking 
       There is no good source of random number in solidity. In this example blockhash with previous block 
       and blocktime is used to generate random number. But its can be computed with another contract. 
 
## 11. Smart contract not having fallback 
       If smart contract which not have fallback function in order to get ethers it might couse some errors . 
       if call funcition not success then rest of the code which are under the call not performed. 
       It may cause unexpected errors. Please check given example. 

## 12. Oracle price manupulation

## 13. Taking flash loan and pool manupulation


     
    
    
    
   

