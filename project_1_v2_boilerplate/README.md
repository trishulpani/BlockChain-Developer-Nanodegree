# Private Blockchain Application

This is the submission for 'Create Private Blockchain' project.

## Issues faced during development

* Non-base58 character issue

    This happened due to using wallet of sigwit seed type. If using Electrum, choose to restore/recreate the wallet using the initial list of pass phrases and click 'Options' button to select 'bip32'. Wallet details should show as follows to avoid this error:
    
    ![Wallet type](screenshots/wallet_type.png)

* Several issues with resolving Javascript promises and filters. Had to go over several stackoverflow and google examples to get them right.

* Get URL for Genesis Block is not correct in the boiler plate code. Check the BlockChainController for the correct path.

## Final Screenshots from working app in local

1. Run your application using the command `node app.js`
You should see in your terminal a message indicating that the server is listening in port 8000:
> Server Listening for port: 8000

![Running Locally](screenshots/Running_locally.png)

2. POSTMAN to request the Genesis block:
    ![Request: http://localhost:8000/block/0 ](screenshots/GetGenesisBlock.png)
3. Request ownership validation to own wallet address:
    ![Request: http://localhost:8000/requestValidation ](screenshots/RequestValidation.png)
4. Sign the message with your Wallet:
    ![Use the Wallet to sign a message](screenshots/ElectrumValidSignature.png)
5. Submit Star
     ![Request: http://localhost:8000/submitstar](screenshots/SubmitStar.png)
6. Retrieve Stars owned by me
    ![Request: http://localhost:8000/blocks/<WALLET_ADDRESS>](screenshots/GetStarsByOwner.png)
7. Validate Blockchain
    ![Request: http://localhost:8000/validateChain](screenshots/ValidateBlockChain.png)



