
# Exposed

## /w3/languages
	headers={}
	type=JSON
	description = returns the list of languages supported by the server

## /w3/wallet/<lang>/nfts
	headers = { wallet-addr : ERC20 checksumed address }
	type=JSON
	description = returns a JSON array for all the NFTs owned by `wallet-addr` in any language using `lang` in the URL.

## /w3/wallet/<lang>/cardpacks
	headers = { wallet-addr : ERC20 checksumed address }
	type=JSON
	description = returns a JSON array for all the CardPacks owned from NFTs by `wallet-addr` in any language using `lang` in the URL.

## /w3/chains
	headers={}
	type=JSON
	description = returns a JSON array for all the chainIds supported

## /get/metadata/<nft_id>
	headers={}
	type=JSON
	description = returns the NFT with `nft_id` equal to token id 

## /get/images/<image_name>
	headers={}
	type=PNG
	description = returns the image. used for monster images

## /get/videos/<video_name>
	headers={}
	type=MP4
	description = returns the video. used for turnables and CGI

## /get/models/<model_name>
	headers={}
	type=GLB
	description = returns the 3D-Model. not yet implemented for AR or Gameplay

## /get/proposals/<proposal_number>
	headers={}
	type=TEXT
	description = returns the raw contents of the proposal. Implemented as the proposals for the DAO.

## /get/cardpacks/<cardpack_id>
	headers={}
	type=JSON
	description = returns the JSON representation of any cardpack. Not yet implemented with `cardpack_id`

## /private/getCount
	headers={}
	type=JSON
	description = returns the current amount of NFTs that has been already minted

## /private/monster/ids/<monster_name>
	headers={}
	type=JSON
	description = returns all the different NFTIDS for any monster specified for `monster_name`

## /hardFetch/eth
	headers={}
	type=number
	description = returns the value of ethereum in USD at any given moment with a 10-second delay and to 2-decimal prescision

## /fake/token/balance
	headers = { wallet-addr : ERC20 checksumed address }
	type=JSON
	description = returns the current balance of `wallet-addr` using fake $AEG token

## /fake/cmc
	headers = { aeg-cmc-code : bytes8 code starting with `0xa314` }
	type=JSON
	description = returns the success on correct calls to redeem VALID coinmarketcap code `aeg-cmc-code`

## /fake/bot/status
	headers={}
	type=JSON
	description = returns the current status of the bot

## /fake/bot/params
	headers={}
	type=JSON
	description = returns the current configurations for the bot

## /fake/bot/balances
	headers={}
	type=JSON
	description = returns the current balances for the bot

## /fake/bot/addresses
	headers={}
	type=JSON
	description = returns the current addresses for the bot

### JSON Representations 

```json
	{
	NFT : {
	   "name": "Shiny Tergy",
	    "description": "Gates of Ethernity Genesis NFT by Aether Games Inc. An exclusive collection of 3000 GoE creatures. On top of being playable creatures within the upcoming game Gates of Ethernity, these NFT give you access to exclusive skins, consumables, and more within the Aether Games franchise.",
	    "image": "https://api.goe.gg/get/videos/GOLD_RARE_CHAOS_STALKER.mp4",
	    "video": "https://api.goe.gg/get/videos/GOLD_RARE_CHAOS_STALKER.mp4",
	    "attributes":
	    [
	        {
	            "name": "Race",
	            "value": "Dragon",
	            "trait_type": "Race"
	        },
	        {
	            "name": "Element",
	            "value": "Chaos",
	            "trait_type": "Element"
	        },
	        {
	            "name": "Evolution",
	            "value": 1,
	            "display_type": "number",
	            "trait_type": "Evolution"
	        },
	        {
	            "name": "Attack",
	            "value": 8,
	            "max-value": 20,
	            "trait_type": "Attack"
	        },
	        {
	            "name": "Defense",
	            "value": 4,
	            "max-value": 20,
	            "trait_type": "Defense"
	        },
	        {
	            "name": "Speed",
	            "value": 6,
	            "max-value": 20,
	            "trait_type": "Speed"
	        },
	        {
	            "name": "Aether",
	            "value": 5,
	            "max-value": 20,
	            "trait_type": "Aether"
	        },
	        {
	            "name": "Crit Chance",
	            "value": 8,
	            "max-value": 20,
	            "display_type": "boost_percentage",
	            "trait_type": "Crit Chance"
	        },
	        {
	            "name": "Overall",
	            "value": 31,
	            "max-value": 100,
	            "trait_type": "Overall"
	        },
	        {
	            "name": "Rarity",
	            "value": "Ethernal mini pet",
	            "trait_type": "Rarity"
	        },
	        {
	            "name": "Card Type",
	            "value": "3D Ethernal",
	            "trait_type": "CoE asset"
	        }
	    ],
	    "animation_url": "https://api.goe.gg/get/videos/GOLD_RARE_CHAOS_STALKER.mp4",
	    "external_url": "https://goe.gg",
	    "coe_image": "https://api.goe.gg/get/images/COE-GOLD_RARE_CHAOS_STALKER.png"
	},
	CARD : {
		"ID": 241,
		"card_name":"COE-Shiny Tergy",
		"card_image":"https://api.goe.gg/get/images/COE-GOLD_RARE_CHAOS_STALKER.png",
		"attributes":{
			"onChain":[
		        {
		            "name": "Race",
		            "value": "Dragon",
		            "trait_type": "Race"
		        },
		        {
		            "name": "Element",
		            "value": "Chaos",
		            "trait_type": "Element"
		        },
		        {
		            "name": "Evolution",
		            "value": 1,
		            "display_type": "number",
		            "trait_type": "Evolution"
		        },
		        {
		            "name": "Attack",
		            "value": 8,
		            "max-value": 20,
		            "trait_type": "Attack"
		        },
		        {
		            "name": "Defense",
		            "value": 4,
		            "max-value": 20,
		            "trait_type": "Defense"
		        },
		        {
		            "name": "Speed",
		            "value": 6,
		            "max-value": 20,
		            "trait_type": "Speed"
		        },
		        {
		            "name": "Aether",
		            "value": 5,
		            "max-value": 20,
		            "trait_type": "Aether"
		        },
		        {
		            "name": "Crit Chance",
		            "value": 8,
		            "max-value": 20,
		            "display_type": "boost_percentage",
		            "trait_type": "Crit Chance"
		        },
		        {
		            "name": "Overall",
		            "value": 31,
		            "max-value": 100,
		            "trait_type": "Overall"
		        },
		        {
		            "name": "Rarity",
		            "value": "Ethernal mini pet",
		            "trait_type": "Rarity"
		        },
		        {
		            "name": "Card Type",
		            "value": "3D Ethernal",
		            "trait_type": "CoE asset"
		        }
	    	],
			"offChain":[
		        {
		            "name": "Race",
		            "value": "Dragon",
		            "trait_type": "Race"
		        },
		        {
		            "name": "Element",
		            "value": "Chaos",
		            "trait_type": "Element"
		        },
		        {
		            "name": "Evolution",
		            "value": 1,
		            "display_type": "number",
		            "trait_type": "Evolution"
		        },
		        {
		            "name": "Attack",
		            "value": 8,
		            "max-value": 20,
		            "trait_type": "Attack"
		        },
		        {
		            "name": "Defense",
		            "value": 4,
		            "max-value": 20,
		            "trait_type": "Defense"
		        },
		        {
		            "name": "Speed",
		            "value": 6,
		            "max-value": 20,
		            "trait_type": "Speed"
		        },
		        {
		            "name": "Aether",
		            "value": 5,
		            "max-value": 20,
		            "trait_type": "Aether"
		        },
		        {
		            "name": "Crit Chance",
		            "value": 8,
		            "max-value": 20,
		            "display_type": "boost_percentage",
		            "trait_type": "Crit Chance"
		        },
		        {
		            "name": "Overall",
		            "value": 31,
		            "max-value": 100,
		            "trait_type": "Overall"
		        },
		        {
		            "name": "Rarity",
		            "value": "Ethernal mini pet",
		            "trait_type": "Rarity"
		        },
		        {
		            "name": "Card Type",
		            "value": "3D Ethernal",
		            "trait_type": "CoE asset"
		        }
	    	]
		}
	},
	CMC : {
		"cmc_code":"0xa314000000000000",
		"reedemable":false
	},
	BOT_STATUS : {
		"running":true,
		"auto_sell":true,
		"auto_buy":false
	},
	BOT_PARAMETERS : {
		"max_increase_precentage":5,
		"max_decrease_precentage":25
	},
	BOT_ADDRESSES : {
		"token_address":"0x0",
		"paired_address":"0x0",
		"factory_address":"0x0",
		"router_address":"0x0",
		"pair_address":"0x0"
	},
	BOT_BALANCES : {
		"token_balance":0,
		"pair_balance":0,
		"token_reserve":0,
		"pair_reserve":0
	},
	DAO_PROPOSAL : {
		"Title":"Create AEG DAO",
		"ID":1,
		"Status":"Final",
		"Resolution":"Accepted",
		"Description":"Create a community driven DAO to decide on proposals via a voting system based on GoEGenesis NFT holdings per wallet",
		"With":1,
		"Against":0,
		"Neutral":0
	}
	}
```
