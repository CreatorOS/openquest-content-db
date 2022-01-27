# Open-source content curation for Openquest.xyz

This repository is a low-key open-source database for all the content that is available on [openquest.xyz](https://openquest.xyz). You can create your own quests and raise a PR to add the same to [openquest.xyz](https://openquest.xyz). 

## Add a new quest/tutorial

To add a quest first of all fork this repo and add the quest metadata as per below instructions. Then raise a PR.
The detailed schema is available [here](/schema.json).
Suppose you want to add a new quest in Ethereum track.
Add a new object under `quests` array of the `build-on-ethereum` value object.
Fill in the details as per `schema.json`.

- Please note the github_url should look like this: `https://raw.githubusercontent.com/CreatorOS/Building-a-bank-with-Solidity-that-isnt-a-toy-For-beginners/main`

## The structure of the content repo

Below are the instructions for structuring the content repo that is referenced by the `github_url` key of the object in the `quests` array.

- The repo should contain a file named `LEARN.md` which will contain all the quest content in markdown format.
- The quest name should be an H1 tag formatted using `#` at the top and immediately below that brief description of the quest.
- The quest should be divided in subquests.
- The title of the subquest will be an H2 tag formatted usign `##`.
- The subquest content should be right below that.
- Please note there should be only one H1 tag which will be the quest title at the top and all other subquests titles should be h2 tags.
- Put all the image assets that you will show in markdown under `learn_src/learn_assets` directory at the root.
- All links to those images should be absolute links. e.g. `https://raw.githubusercontent.com/CreatorOS/deploying-the-program-on-to-solana/main/learn_src/learn_assets/1.png`
- Properly formate code using triple back ticks. The code should be diplayed like below. 
```
console.log('Hello, Web3');
```
- If applicable please include the working codebase of the quest in the content repo itself.

