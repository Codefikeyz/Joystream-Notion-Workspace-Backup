# Rhodes copy tuning

Participants: Dima, Netguru Design, Klaudiusz
Created By: Klaudiusz
Created: April 14, 2022 11:05 AM
Last Edited Time: April 28, 2022 7:53 PM

## NFT minting

- (banner) You won’t be able to edit this video once you mint an NFT for it.
- (header) Mint NFT
- (switch) Mint NFT for this video
- (tooltip) 🚨 Minting an NFT creates a record of ownership on the blockchain that can be put on sale. This will not impact your intellectual rights of the video.
    
    ![Screenshot 2022-04-14 at 12.31.50.jpg](Rhodes%20copy%20tuning/Screenshot_2022-04-14_at_12.31.50.jpg)
    
- (royalties tooltip) Setting royalties lets you earn commission from every sale of this NFT.
- (modal after minting for the first time) Now that you've minted your first NFT, you can put it on sale by choosing "Start sale" from your video options.
- (success snackbar) Changes published
- (video upload success) Drop the icon from the See on Joystream link

## NFT sale

- (step 3 header) Review listing terms
- (step 1 description) Choose the listing type for your NFT
- (step 1 auction description) Put it on a timed or open auction. See the bids coming.
- (step 1 fixed price) Sell it for a fixed price only. No bids.
- (step 2 fixed price header) Fixed price
- (step 2 fixed price description) Set up the price for your NFT. It can be changed later. Cancel anytime.
- (step 3) Listing settings → Listing terms
- (step 3, listing type fixed price tooltip) Sell it for a fixed price only. No bids.
- (step 3, fixed price tooltip (only buy now)) Price for your NFT as shown to your buyers
- (step 3, Fee tooltip) Fee covers cost of blockchain computation of this transaction
- (step 3, accept terms) **Remove**
- (step 2 auction) Pick a timed or open auction. Optionally set up a buy now price.
- (Open auction description) Pick the winning bid or cancel anytime
- (Time auction description) Highest bidder wins, cannot be cancelled once started
- (Duration headers) Starts, Ends
- (Auction duration total) 10 hours/ 6 300 blocks / 7 days (capitalization)
- (Auction duration tooltip) On blockchain, duration is expressed in number of blocks
- (Minimum bid tooltip) Only bids higher than this value will be accepted
- (step 2 Fixed price header) Buy now price
- (step 2 Fixed price tooltip) Bids matching this value will automatically end your auction
- (step 2 whitelist tooltip) Only members included in the whitelist will be able to bid on this auction.
- (step 2 minimum bid lower than buy now) Minimum bid must be lower than the buy now price
- (step 2 minimum bid lower than 1) Minimum bid must be at least 1
- (step 2 single member whitelist error) Whitelist must contain at least two members
- (step 3 starting date tooltip) The moment in time when your auction becomes active and bids will be accepted
- (step 3 whitelist header) Whitelist (instead of WhiteList)
- (step 3 Submit) Start sale
- (success snackbar) “`NFT put on sale successfully`", Drop the icon for action
- (step 3 start date in the past)
    
    ![Untitled](Rhodes%20copy%20tuning/Untitled.png)
    
    - **Dialog styling:** Preferably it’s the new Alert dialog in the `Informative` variant. If that’s too much effort for now, can we at least change the button styling to be Primary (blue)? 🙏
    - **Header:** Start sale now?
    - **Body:** The start date ([date]) you selected has already passed. Do you want to put your NFT on sale now?
    - **Button 1:** Cancel (takes you back to the previous step)
    - **Button 2:** Start sale now (ideally, starts sale imidietaly)

## NFT purchase

- Payment split → Revenue split
- (Payment split tooltip) Revenue split shows the proceedings from this sale based on royalties set up by the creator.

![Screenshot 2022-04-26 at 16.10.47.jpg](Rhodes%20copy%20tuning/Screenshot_2022-04-26_at_16.10.47.jpg)

- (ending in tooltip) On blockchain, duration is expressed in number of blocks. This auction ends at block XXXXXX

![Screenshot 2022-04-26 at 16.18.48.jpg](Rhodes%20copy%20tuning/Screenshot_2022-04-26_at_16.18.48.jpg)

- (no top bid) No bids yet
- (input placeholder) Enter your bid
- drop “You need to fill out the amount first”

![Screenshot 2022-04-26 at 16.29.39.jpg](Rhodes%20copy%20tuning/Screenshot_2022-04-26_at_16.29.39.jpg)

- After placing your bid, you will not be able to withdraw it. (dot)
- (header) Place bid, Change bid
- Drop the second message
- (open auction input header) Minimum bid
- (open auction exclamation message) Your bid can be withdrawn if it’s not accepted by the owner within 60 seconds from placing it.
- You will be able to change your bid to a lower one after 26 Apr 2022, 16:47.
- (bid too small error) Your bid must be higher than the minimum bid
- (snackbar success) drop dot from the header

![Untitled](Rhodes%20copy%20tuning/Untitled%201.png)

## NFT settling

As in Figma, but:

- drop “here”
- drop “the” from the button
- (snackbar success) add dot at the end, make sure the copy for the seller makes sense, NICE TO HAVE: handle of the member that won the auction for the seller

## NFT widget

- **General note/ask from Adam**
Can we drop all a/an/the articles from all button labels in the NFT widget? Eg. `Withdraw a bid` → `Withdraw bid`.  It was this way in the designs, so I’m not sure how could I miss their presence in the implementation...
- **Withdraw your bid to participate**

You placed a bid in a previous auction that you can now withdraw to be able to participate in this auction.

- **Auction ended**

This auction has ended and no one placed a bid. You can now remove this NFT from sale.

- **Auction ended**

This auction has ended and no one placed a bid. We're waiting for the NFT owner to remove this NFT from sale.

- **Remove from sale?**

Are you sure you want to remove this NFT from sale? You can put it back on sale anytime.

- (remove from sale success) NFT removed from sale successfully
You can put it back on sale anytime.
- You placed a bid in a previous auction that you can now withdraw.
- (snackbar success accepting bid) Bid accepted
Your auction has ended. The ownership has been transferred.
- (Change price modal) You can update the price of this NFT anytime.
- (change price success snackbar) NFT price changed successfully
You can update the price anytime.

## Member NFTs

- **No NFTs found that match filter criteria → No NFTs found**
- Try changing the filters.
- This member hasn't collected any NFTs yet.

## Channel NFTs

- (filters) same as in the member view
- **No NFTs minted**
- This channel hasn’t minted any NFTs yet.

## Notifications

- additional notifs:
    - Auction you participated in has ended
    - xxx settled your auction.

## NFT history

- Removed from sale by xxx
- Price changed by xxx