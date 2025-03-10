---
order: -200
description: A project checklist to walk through for Presents projects.
---
# Checklist for Presents Projects

!!!danger
Before proceeding to mainnet upload, please verify that your script behaves as expected across all major web browsers (e.g. Chrome, Firefox, Safari, etc.) We recommend using [Browserstack](https://www.browserstack.com/) to test across devices. If you do not already have an account, select Get started free and set up a free account.
!!!

## Upload

1. Please ensure that you have reviewed and abided by our [Documentation](readme/readme.md#documentation) and [Guidelines & Constraints](readme/readme.md#guidelines-and-constraints). If you are assigning rarity to different things, Art Blocks strongly recommends that you use an instance of the Random class found [here](readme/readme.md#safely-deriving-randomness-from-the-token-hash) to feed all of your project's randomness. Prior to uploading, please verify that your script meets this requirement.
2. Ensure your wallet is funded with enough ETH to pay the gas fees for the upload and unpausing process. For more information on the estimated cost of these steps, [click here.](readme/readme.md#cost)
3. Submit one field at a time. Wait for that transaction to clear before attempting the next field.
4. When you upload your script, please copy it exactly from testnet.
5. Include the following in the Project Base URI field: `https://api.artblocks.io/token/`
   * **Important:** If you are setting this field for an Engine project, rather than an Art Blocks project directly, the `baseTokenURI` field should follow a slightly different structure. Please see the [Art Blocks Engine documentation](../art-blocks-engine-onboarding/art-blocks-engine-101/adding-new-project-shells.md) for more info.
6. As [noted in the main documentation overview](readme/readme.md), please ensure that you are only setting a currency address if you are using some custom ERC20-compatible token (e.g., DAI) for the sale of your work. This field **should not** be set if you are accepting ETH as your payment type.
7. Please double-check, triple-check, and then check again the generated [features script](readme/features.md) results on staging to ensure they are 100% accurate. This is **extremely important** to get right, as it changes to fix any bugs you may introduce in this script may have a massive impact on how the artwork is perceived by collectors and may cause confusion in the secondary market. It is **your responsibility** to guarantee that your features script is properly verified in the artist staging environment.

## Features

1. Please see [Features](readme/features.md) for full details on how you set your project features as an artist.
2. The features script for your project should first be tested on the Goerli testnet (https://artist-staging.artblocks.io), alongside your art script. Ensure that your features are being displayed as expected on testnet before proceeding to project deployment to mainnet.
3. When uploading your feature script to mainnet (https://www.artblocks.io/), please ensure that you are uploading the exact same features script, taking the same care that you would with your art script itself.
4. While the features script _is not_ stored on-chain like the art script is, bugs in your features script will cause meaningful disruptions for collectors trying to explore your work on a per-feature basis.

## Tags

Add relevant tags to your project. More on tags [here](https://docs.artblocks.io/creator-docs/creator-onboarding/readme/project-form-fields-guide/). 

## Economics

1. Review the Project Pricing Model for Dutch auctions [here](https://docs.artblocks.io/creator-docs/creator-onboarding/readme/project-pricing-model/#project-pricing-dutch-auction-settings)
2. Consider the overall economics of your project for a successful release.
3. Artists can only have one active project at a time.
4. In order to submit a new project, your previous project must be closed (sold out/completed).

## Charity Component
To maintain our commitment to charitable giving, we ask artists to consider donating 25% of sales above the resting price via Dutch auction to a charity of their choice. If you elect to participate in this way, please determine your chosen charity, and confirm its eligibility, before mint #0. To whom and how you donate is entirely up to you. Art Blocks does not require you to donate any proceeds in order to engage with our platform. If you do elect to donate to a charity, it is advisable to consider whether the charity which you choose to support qualifies under United States tax law to receive tax-deductible donations. If your project designates only one primary wallet, you may use the additional payee field to manage on-chain donations. All revenue may also be routed to a single wallet and donated after your drop. We encourage you to consult with a tax professional to understand any potential tax implications of your planned giving, as these can be widely variable.

Learn more about Charitable Donation [here](https://docs.artblocks.io/creator-docs/creator-onboarding/readme/charitable-donations/).

## Approve additional payee info for primary and secondary sales⛽
Include the wallet addresses for primary and secondary sales to be distributed. Once submitted, the details will be approved by the Art Team. If you do not have additional wallet addresses that will receive funds from primary or secondary sales you must input `0x0000000000000000000000000000000000000000` in the blank fields. 

## Mint #0

1. Note: Mint #0 will be completed with the Set Price minter. If you are using a fixed price, your project will be unpaused under the Danger tab right before your project’s release. Once a project using Set Price - ETH or Set Price - Custom ERC20 is unpaused, it will be live for minting. If your project will be sold via Dutch auction, please set the minter to Set Price ETH with the set price as your Dutch Auction’s base price for Mint #0.
2.  **Before** minting Mint #0, ensure that your "additional payee wallet" has been set for the same configuration that you will use it for in your project release. E.g., if you are using the "additional payee wallet" field to donate to charity at the time of mint, you must set this before minting your #0. This is done to ensure that this full functionality is tested end-to-end as part of the mint #0 process, and that there are no issues with the wallet selected for the additional payee. **Please note: Art Blocks does not currently support sending primary sales payments into a multi-sig contract and there are known issues when attempting to do so. While we plan to update our minting smart contracts in the near future to resolve this, multi-sig wallets should not be used for this purpose at this time.**
3. Once your project information has been uploaded, **please confirm in your artist DM that you're ready for mint #0**. The Art Blocks Team will look over your project shell and then give you the go-ahead to mint #0. 
4. Mint #0 must occur before your release can be scheduled.

### Payout Details 

Be sure that you've input information in all field forms. If you do not have an additional payee for primary or secondary sales, you may put `0x0000000000000000000000000000000000000000` in the field and 0% for the payee percentage. 

## Initiating your MinterSuite choice

If you are using the Dutch auction - Exponential Price Decrease or Dutch auction - Linear Price Decrease, your project will be unpaused prior to your auction’s start time. Once your project page is public, your project can be unpaused under the Danger tab any time prior to the starting time of your auction. We recommend unpausing projects the morning of your release. Once unpaused, your project will be marked as “Upcoming” and the dutch auction will automatically begin at your start time, leaving the beginning of the auction hands-free. 

## Scheduling

* Once mint #0 and the features script are in place, Art Blocks will work with you to schedule/announce your release.
* After your project has been scheduled, you are free to announce and promote your project on your social media.
* Refer to our Marketing 101 Guide [here](https://docs.artblocks.io/creator-docs/creator-onboarding/readme/marketing101/)

## Allowlist:
The allowlist minter is available for projects in the Presents, Explorations, and Collaborations Collections. This process is supported through the Art Blocks platform as a tool to mitigate botting and to create access to the minting experience for established collectors and to new participants. Art Blocks’ role in the allowlist feature is through smart contract development. Artists are responsible for the selection of allowlisted minters.

1. Artists can choose the list of addresses to allow as well as the number of mints allowed per-wallet. Currently, artists are responsible for crafting their allowlist and uploading a comma-separated list of ETH addresses in a .txt or .CSV file to the minter option.
 a. [Premint](https://www.premint.xyz/) is a super helpful tool for creating an allowlist by using social channels to reach collectors, friends, family, etc. In addition, Art Blocks hosts a Python script for retrieving & snapshotting either a list of all Art Blocks token holders or the token-holders of a specific project.
2. Allowlists are available before the public dutch auction. Artists are responsible for unpausing their project the day prior.
3. Allowlists are sold via a fixed price. The Art Blocks Team recommends a fixed price that is 0.05-0.1 ETH above the auction’s resting price.
4. **Note** The allowlist feature is not a reserve feature. All allowlisted wallets will have access to purchase a mint and there will not be a limit set on the total number of mints via the allowlist.
5. Artists must update the Sales Notes section with the criteria for the allowlist, the open date/time for the allowlist, and the close date/time for the allowlist. We also recommend that artists post in our #artist-announcements channel to announce the opening of an allowlist mint.

**To set the allowlist minter:**
1. Select Set Price- ETH, Allowlisted Users Only
2. Upload your .csv or .txt file
3. Enter your fixed price
4. We recommend leaving the mint per wallet limit to 1 for allowlist . If you would like to adjust this, please let the Art Blocks Team know.

## Unpausing

* When it's time, you'll click the Unpause button under the Danger tab.
* When unpausing the project, please send in the tx 30 seconds prior to the top of the hour. To unpause the project, please send high gas (2-3x what is suggested as high gas on https://etherscan.io/gastracker). If you have questions about what you should set your gas to, please ask in your project DM and the Art Blocks Team can advise.
* Once the transaction clears, your project will be live for minting.


## Rarities

* Do not discuss odds or feature rarities about your project until it is completely sold out.

## Finishing Steps

1. Once your project is complete, you may reset the “Additional Payee Percentage” to 0% for any charitable giving conducted during minting. If removing, you will need to edit the secondary payee info to your wallet or set the percentage to 0. In order to successfully update payout details, you will need to enter information into all fields to submit the change.
2. You may also remove any language from your Project Description to describe sales mechanics.
3. Report final charity donation totals in your artist DM
4. **[For previously Curated only]** Please fill out the appropriate form to add bot support to your Discord channel for your completed project: https://github.com/ArtBlocks/artbot/issues/new/choose.



