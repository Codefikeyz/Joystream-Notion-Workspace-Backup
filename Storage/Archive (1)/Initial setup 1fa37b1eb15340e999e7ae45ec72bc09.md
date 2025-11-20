# Initial setup

For a future analysis, here are the commands I've used for the initial setup:

```jsx
# global settings

# Set "global" storage limits to 10000 GB and 200000 files:
yarn storage-node leader:update-voucher-limits -s 10000000000000 -o 20000 -k /root/.local/share/joystream-cli/accounts/SPLeader.json 

# Update/set the dynamic bag policy:
yarn storage-node leader:update-dynamic-bag-policy -t Channel -n 4 -k /root/.local/share/joystream-cli/accounts/SPLeader.json
 
# Update the bag limit:
yarn storage-node leader:update-bag-limit -l 5 -k /root/.local/share/joystream-cli/accounts/SPLeader.json 

```