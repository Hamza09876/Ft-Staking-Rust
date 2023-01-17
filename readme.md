Token creation 
First of All we have to create a token that can be staked to contract and can be given as reward.
1) spl-token create-token --decimals
2) spl-token create-account <token>
3) spl-token mint <token>
Need to change variable value in contract
In Admin add your keypair Pubkey as it will be controller of your vault generation.