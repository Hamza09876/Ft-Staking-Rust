Token creation 
First of All we have to create a token that can be staked to contract and can be given as reward.
1) spl-token create-token --decimals
2) spl-token create-account <token>
3) spl-token mint <token>
Need to change variable value in contract:
In Admin add your keypair Pubkey as it will be controller of your vault generation.
In reward mint add token which will contract hold and give in reward
Deploy Contract by compiling
1) cargo build-bpf
2) solana program deploy /ft_staking/ft_stake_contract/target/deploy/staking.so
Client side:
Edit and compile client side
1)need to change program_id
2)need to change reward_mint
Will run commands for Vault generation by using Admin keypair
1)staking-tokens-client generate_vault_address -e dev -s <keypair.json> --min_lock_period <seconds>
With some other wallet that have same tokens in it.
2)staking-tokens-client stake -s <keypair.json> -e dev -a <token-amount> -l 2
3)staking-tokens-client unstake -s <keypair.json> -e dev