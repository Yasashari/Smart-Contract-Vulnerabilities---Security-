# Smart-Contract-Vulnerabilities---Security-
## Reentrancy Attack 
    Check how to do reentrancy attack with reentrancy_vulnarable_contract . 
    reentrancy_vulnarable_contract is not work compiler 0.8.7 . Its work 0.6.10 compiler.
    reentrancy_corrected - After fixed reentracny vulnerability. 
    

## Preventive methods of reentrancy attack
    1. Use openzappling nonReentrant modifier.
    2. Update the state balance variable before sending the transaction.
    3. Or else you custom modifier as given in reentrancey_corrected.sol file.
