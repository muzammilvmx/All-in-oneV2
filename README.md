[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=ALL+in+one+V2+By+Cipher_Airdrop)](https://git.io/typing-svg)


[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=This+Script+credit+goes+to;someone+else)](https://git.io/typing-svg)

<h1>Social Links</h1>
Follow us here: [Cipher_Airdrop](https://linktr.ee/cadrop)

Twitter(X): [Cipher_Airdrop](https://x.com/cipher_airdrop)

Telegram: [Cipher_Airdrop](https://t.me/Cipher_Airdrop)


<h1>Readme</h1>
An ideal V2 script for farm management. Having mastered it, you can (there is a listing of modules) :

1. web3_checker: very quickly watches the balance of the coin in any evm network.
2. debank_checker: about quickly looks at all tokens, nft and protocols in all evm networks (which are available on the most [debank](https://debank.com/)).
3. exchange_withdraw: coin withdrawal from exchanges: binance, mexc, kucoin, bybit, huobi, bitget.
4. okx_withdraw: withdrawal from the exchange okx + as a gift withdrawal from the sub. separate module due to the function of withdrawal from sub-accounts.
5. transfer: withdrawal of coins from wallets in evm networks.
6. 0x_swap: agragator, good 1inch replacement.
7. [orbiter](https://www.orbiter.finance/) : bridge eth in all networks, including zksync era and starknet. to bridge to starknet, you need to add the addresses of the starknet wallets to the file `starknet_address.txt`
8. [woofi](https://fi.woo.org/) : bridge. the bridge passes through stargate (layerzero). universal, all the coins and networks that are there are available.
9. [woofi](https://fi.woo.org/) : swap. universal, all coins and networks that are there are available.
10. sushiswap: universal, all major networks are available except optimism (so far).
11. bungee_refuel: cheap bridge of the pressure between the networks.
12. tx_checker: looks nonce in all (almost) evm networks.
13. 1inch_swap: aggregator.
14. merkly_refuel: sending gas from one network to another via layerzero.
15. nft_checker: very quickly (asynka) watches the balance of a specific nft.

Additional information :

1. All results are recorded not only in the terminal, but also in tg-bot.
2. web3_checker and nft_checker use multicall = > tracking is very fast.
3. Ability to include proxies in web3. It works like this: takes all your wallets and takes proxy from the file one by one `proxies.txt`. That is, the distribution on the proxy will be equal. Number of wallets and proxy may vary. For example, if there are 10 wallets and 3 proxies, then the distribution will be as follows: proxy_1 = 4 wallets, proxy_2 = 3 wallets, proxy_3 = 3 wallets.
4. Added the maximum gas charge to $ for each network. if the gas in the trance is higher than the specified number, the script will sleep until the gas drops (`setting.py => MAX_GAS_CHARGE`)
5. If the transaction hangs in the pending > of a given time (`config.py => max_time_check_tx_status`), it is considered fulfilled. I did this because of bsc, tk with 1 gwei some trunks hang in pending for hours, and the script, respectively, too.
6. You can run 1 or more modules. The launch of several modules is configured in `tracks.py`.
7. For 1inch_swap, api key is required, which can be obtained here : https://portal.1inch.dev/dashboard.
8. Asichronism: you can run several wallets at the same time.


<h1>Setting</h1>
1. All settings are made in the file `setting.py`, the description is the same.<br>
2. If you want to run multiple modules in one chain, you need to configure them in `tracks.py`.<br>
3. In folder `data` rename files `wallets_EXAMPLE.txt` = > `wallets.txt`, `proxies_EXAMPLE.txt` = > `proxies.txt`, `data_EXAMPLE.py` = > `data.py`<br>
4. In folder data there are 5 files :
<ul><li>`wallets.txt`- here we write wallets (coupers / addresses).</li>
<li>`recipients.txt`- here we write the addresses for the transfer, used only in the transfer module when we display from the wallet to the address. 1 wallet = 1 address.</li>
<li>`proxies.txt` - we write proxies here, they are used in a debank checker, without them it will not work, and in web3, if `USE_PROXY = True` (in the config). Format : http://login:password@ip:port</li>
<li>`starknet_address.txt`- here we write down the addresses of starknet wallets. if you don’t shave from the orbit to the stark, you can not insert.</li>
<li>`data.py`- here is all private information: rpc, tg_token, tg_id, api keys to exchanges.</li></ul>
5. You need to configure modules in value classes in a file `setting.py`.
6. You need to start the file `main.py`, if `USE_TRACKS = False`, then in the terminal there will be a list with modules, you will need to select one.

<h1>Information on tracks(several modules)</h1>
1. To make the mode work, you need to `setting.py` do `USE_TRACKS = True`.<br>
2. `tracks.py` tracks with modules are tuned, you can make several tracks and select them in `setting.py` in variable `TRACK`.<br>
3. Function `wait_balance` only works in track mode: you select the network in which you will wait for the coin, and the minimum balance. When the coin balance becomes larger `min_balance`, the script will go to the next module. Check balance every 10 seconds.<br>

We install libraries : `pip install -r requirements.txt`<br>
Attention! The code may be with errors, and for the lost money we do not bear responsibility. I advise you to first test everything for small amounts.<br>
A huge request to first read everything 10 times, test everything, google it and only then ask questions to [Cipher_Airdrop Admin](https://t.me/Ma63838373)

<p>Share it as much as u can</p>
