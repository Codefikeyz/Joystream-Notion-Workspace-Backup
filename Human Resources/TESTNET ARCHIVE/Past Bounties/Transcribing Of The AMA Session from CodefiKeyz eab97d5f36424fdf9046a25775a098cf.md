# Transcribing Of The AMA Session from CodefiKeyz

### **From** [https://dao.joystream.org/#/bounty/preview/179](https://dao.joystream.org/#/bounty/preview/179)

**CodefiKeyz**

[Joystream Governance App](https://dao.joystream.org/#/forum/thread/649)

There we go, welcome back everybody to another community call. I guess we have July 6th we postponed from last week but good to see everybody here and those with us. Martin has also graced us with his presence so good to see you as well. I'm just going to hand it over to bedale and he will present some news and we will do some calls and as always guys in the chats, you will get priorities so if you have a question feel free to throw it in the chat or even better raise your hand and we will unmute you and feel free to bring your questions and have a discussion with us live, you know the drill by now.

Speaker to Bedale: Hey! Wassup

Bedale: Umm, Cool. Very happy to have you guys join us. I'll try to give an overview of where we are, addressing some questions that have been posted in the chat. Just ask some more questions as we go and hopefully will cover some more topics. So as always, why don't we start with the timeline, sort of what the future looks like. So right now the immediate next week is the Carthage network which is the last testnet. I'll be repeating some topics because not everyone has been following everything.  I think 1st of July is the estimate that we have on the game timeline right now I think we're looking at having a first fully working staging network as early as next Monday so that's a new Blockchain, new query node, new storage providers and distributors all working with the final blockchain and then after that we have a bunch of tests and updates to apply some pioneers and so on.

Then after that there is mainnet which in this timeline I'm affording let's say 4weeks an actual Carthage network testing and whatever problems that may occur. So that's of course the major milestone that we're working towards. You'll also notice that the first immediate timeline is actually your deadline to cash out your tJoy if you want to do that.

Bedale to Host: Do you people see my coins by the way?

Host: Yea, Yea, yea, we do.

Bedale: Yes ok so this deadline, so I want to say is a fixed deadline, I lifted it off the block when I was meant for the Carthage network. So the Carthage network as I'll cover has a new genesis block which we are trying to have look as similar as possible to the main network, so that means we're going to have to give all the main network stakeholders allocation so they try out their investings, schedules and their lucks and accounts and everything but means any tJoy allocations that existed are gonna be a minority and so if you want to get a credit for that you're going to have to cash out your tJoy at your earliest convenience. You see that you can keep earning joy so I'm not sure if people are confused about this and if people have stop putting in effort, I know some people and wonder why they're there when it stops so I would say effort towards the founding member program is going to be recorded all the way up till the main network of course there's a separate question of well what if I don't earn enough to become a founding member as indicated by the current limit, we'll get back to that topic later, I guess in the presentation, so these are the important milestones.

Bedale to Robert & Martin: Anything I should dwell on here, Robert? Martin?

Robert: I don't know about that but I was thinking you could probably throw your camera ON that you are sharing your screen.

Bedale: (Turns Camera On)

Robert: Nice

Martin: Cool

Bedale: The Carthage Network, let us quickly cover what's in that and I can also give you a quick breakdown of where we are with the different parts to that release.

They're all really 3 sort of big goals that were aiming towards, one is to have a ready run time which would sort of future complete scope so we're upgrading to a new version of substrate which for example is required to be a pair chain down the road and fix a number of issues that were pointed out in prior audits about the sub version we were using was a bit old. We're addressing the issues from the recent audit with work squad which is our second auditing partner at that one very well we'll be publishing all of those auditing reports at a later time. The creator tokens will be part of the blockchain but they are not part of atlas, so pseudo tokens for those of you don't know are all these kind of pseudo equity tokens that creators can use to raise funds and share rewards and incentivize a community to support them and you get a cut of the revenue from Nfts and from the council from your channel through those tokens and there are some really innovative designs that are being done right now, we do post them regularly so you can sort of get a peek into how it's going to look but it won't be in atlas at launch, then the creator payouts feature will also be finished at launch and in the runtime again this is where you allow the council to payout creators for the content they put out, so that's really important. There is a new version of the bounty module which will be disabled in Pioneer as we've said before takes too long to update Pioneer on the cuarto to support the new multi-module so that will be sort of disabled but that's the final version and then we will work on updating Pioneer post launch, it will be the real token issuing and so if you guys remember we had an issue a while back about what should be issued and what should be the name of the smallest unit I think we actually landed on I don't love this to be honest with you but that was chosen HAPI as in happy don't blame me, blame cardish, I think you know that's what we ended up with so this is our gray of satoshi if you will. If I don't get these numbers wrong I think we will have 10 billion HAPI in each JOY then we are gonna have a billion JOY.

This is the denomination insuance that I believe we went for.  Adding multi signatures to accounts that's important for example JF genesis has an allocation that any security on and having a single account is not a good idea, so  if you were a big holder on launch you should consider using the feature. We can have a fully bench marked runtime on reference hardwares, that means the final fees will be revealed to us in terms of the JOY or HAPI units and also by implications if you use a market cap valuation also real dollar price for making a profile uploading a video or making NFTs, so that'll be interesting. We are targeting those to be as cheap as possible while being secure, so that's what I'm focusing on these days. I'll jump over to see the real fees parameter values is what I just talked about. Investing, we will be covering investing later in the presentation, obviously funds are all locked and they will increasingly get unlocked over time, that's gonna be a part of Carthage as well.

Lastly the bootstrapping is going to be the real bootstrapping so from lunch is going to be a special script that we run which kind of induct the founding members into the blockchain and we don't actually have a blockchain level concept for the founding members currently. The way the structure of the genesis block is going to be is based on 90% I am thinking in terms of joy tokens, it's going to be kind of a projection of the actual genesis block and 10% is going to be the rhodes accounts because we know that people will have people who are not founding members will you know you don't want them to lose their access to their funds to be able to upload and do whatever they have to do so we are still gonna retain those. Again if you want credit for them, however you earned them, you are gonna have to cash them out before the deadline.

We've also started working towards mainnet and these are some other things we are working on that are pretty cool, we are going to first redesign and update our websites and we are going to update

pioneer it's kind of the new focus we are having. If you look at our website right now the projects then is all about improvement and there isn't a founding member program post mainnet, it doesn't mean that we won't give out tokens to people post mainnet but the founding members program per say won't exist post mainnet, so we have to change our messaging and the structure of the website to be compatible for lunch and we are also working on separating atlas and its own products so that's going to run on some new domain and it's probably gonna be renamed so I'll be interested in getting people's input in the community about what it is and make people understand that atlas is not joystream and joystream is not atlas.

If you google atlas right now you will see joystream in the header of the product and history, the goal is for people that run their own atlas instances with their own branding and so they were taking the first step to to make it possible and convenient for people to run their own standalone atlas like versions I think we should probably start linking to them as soon as people still running some real contenders to the JS Genesis version which is gonna run on some unknown domain we are working on fiat onboarding in obviously for using some high-powered features like NFTS, bidding and creator token purchasing, you need people to have a unique way to get access to the native token.

Not everyone has a like crypto already, I think selling crypto to people is like a big pain in the behind, so we're working on getting kinda like a widget going with a with a partner so that people could easily get JOY so they can use it for all the things they need primarily in atlas really, because we will be running faster still for Pioneer for the smaller value operations.

So that's kind of a timeline for now, let's go to the founding member program but let's take some questions.

Any questions??

No?

Alright, I will keep going. I thought it would be instructive cuz it's in our hands to ask questions about the history of the program and can it's kinda not transparent ruler and where they came from and me and Martin had a long session today trying to break down what different spreadsheets and databases included and how we got those values and so on So I'm gonna try to give you the history of where those numbers come from and if we could ever gonna put this in the handbook so people can verify and check that this is correct and definitely check the run out locations and someone but we just started with the history. There so the V1 version this is the version where it effectively was just a volunteer efforts were a few very early people on this, if this is really early I think we are talking basically early 2019 at this point we had people show up, manned the telegram channel, write software, test software, run validators, whatever there was, there was no fame and glory at that point it was all just hard work and obscurity and out all over after a period of time we decided to do okay we need a real program the V2 program and so we decided to say okay we need to kind of honour the people who have put in the most effort by giving them an allocation already before we start and and that's why you see that breakdown for a @tomato @nexusfallout @enjoythefood @l1dev and @freakstatic. Again it's not a coincidence that many of those people are the kind of senior most knowledgeable members today they've been at it for a long time.

Bedale to Martin: Do you still remember Martin, when we transitioned into the scoring periods and KPIs and that kind of stuff feel.

Martin: I feel like it was early 2021, but it sounds a bit like a year or something but I'm not sure but I might check.

Host: Alright so, that was the actual founding member program and so in that program people had to report what they were doing there to describe what are the contributions they made whatever nodes they were running and basically we would decide at some arbitrary point whether they became a founding member and they would immediately earn like 0.02% and then beyond that they would get basically a share of a 10% pool based on how many scores you got, so if you look at this line over here at the pools 10% and then if you take all of these fixed induction kind of cliffs and these numbers that were pre-assigned I think you get this number, I hope that's correct. That gives you 7.62% and everyone's scores from the V2 were converted into Joy allocations by basically splitting the sub proportion that was the beginning of incentives V3.

And they're as the story goes and that still looking at the point today we did weekly council periods basically to cut the long story short the amount of joy you earned was basically proportional to the share of the tJoy as a share of the Joy budget. So yeah Martin claims it fits pretty well, what fits pretty well with the repo.

Martin: I think it's February 2021

Host: Okay and so this program we were imagining allocating 10 percentage points additionally know what happened has been that stuff for the if you take the total amount of enjoy that's been turned in that program V3 and if you consider everyone is everyone I think that everyone see the people who have not become founding members bad constitutes 1.32 percentage points which is very long actually and

So let's obviously mix the result, the story isn't over yet both on the number here or how much they will get right now and this is totally less than what we expected to get . It is less than the speculative number of 233. I will also say it's a whole number in terms of allocation. That's the matter of fact today. If you move this threshold of 15, you will get a bigger number here and here….. uhmm does it make sense so far?

Listener: one question, why are they not inducted, what's missing, kyc or?

Basically yes. That's the practical thing. So they will get inducted uh yeah and then they said we can try the genesis block was the best thing and I guess with a little bit of reveal. This is a preliminary mainnet genesis block. It is preliminary in that the number founding member. I should explain first….it is like what something is for, what the current share of the genesis block is this then there is liquidity that is referred to as  out of all the tokens for this number, 8% are transferable right at launch, then the remaining, i guess 92% unlocks so many locks. So if you look at the following categories, you have the current founding numbers,you have the core team, you have reserved funds of which Genesis will use on the next slide. There is a slot of tokens for possible future parachain slot because the actual mainnet will map the parachain and then there are the investors that funded us through the three rounds we have done and then there is a tiny little share for sudo in order to run the bootstrapping script and just be able to do something while we are uh loading.

Listener: To pay a transaction fee?

Host: basically… yeah ..that kind of stuff.

Uhm so on the parachain side what we have said is that uh we don't want to go any further trying to resolve the details of getting a parachain slot and also the detectable size of incorporating teamwork  and all these kind of things, we rather launch now and then we can transfer over to parachain slot later, and that require using some funds or tokens  which is why this liquidity is a 100%. The process of which we should make this determination should be , I don't know, however the council is made, we need to deploy those slots for crowd mode effect , but anyway that story and so they have to liquid because you apply some destined schedule to them at that point in time.so  there will be different schedule that will come to pass but that is not a 100% sure. Sometimes if we find this is not gonna happen or isn't gonna increase, then we have to dispose of it somehow in case there becomes our open question. They get burned or whether they get redeployed for something  else in the reserved category. Something else in the reserved category so we have to keep that open first because we just don't know if he had a kind of a that's a schedule to that and we kind of handcuff ourselves in terms of the timeline and if we found that it was a good idea  it's still kind of  too complicated

Are these very good areas?

Yeah ….the reserve side like what that means exactly what we're doing, creator programme that was starting  not sure I talked about that , but basically at launch, we will be doing the YouTube sync program which I talked about . But obv getting tokens to creators is super important because they bring the content which brings the audience and developers and everything and also grant support to people building apps, libraries and these sorts of things maybe you don't know you don't know how well internally within the Dell itself will be able to coordinate those things so they can you will still be able to help . And the various other strategic partners while launching and later down the road you can have there's a big kind  of category of service providers and parts that can be helpful in supporting an ecosystem , block chain or all through these things you may want here. So that's kind of a resolved poll, I guess I should, I'm getting a good question from someone who has a name I can't pronounce, there's a you know, new answers of making negotiations for different investors at different times, basically I can tell you we have the opt of treating investors different ways from very early, to the latest round and we found that it was best to just treat everyone the same the investors had a lot of terms and conditions that basically gave them the auction to require so we had to launch that. Okay we could put everyone in that category, but I think really founding members and investors are in very different positions with respect to roles and founding numbers to help the launch firm online do with the project whilst the investors are really financiers. So that difference is not very common , we should put that in a lot of projects.

Uhm current investors holding 32 supplies potentially because you don't see that on the screen. Is not as asking, the current investors category smallest 32 percentage of supply with 79% liquidity on the whole thing. They may potentially want to join a lot of JOY on day 1. The price of joy appreciate in my opinion. Who wants to buy and who wants to sell is very hard and the same label is right about that . I don't know how much we should be paying attention to that but specifically I don't think the price of  JOY for the down and even quite a long time is all that important.  It is really about getting the system to work properly and the people being involved are burning it properly. I think that's more important  than the price itself. So you need some level of press support to pay for validation or all these things and the scale of which necessarily is not that big when we launched so I am not strictly concerned about that.i hope that made sense, and then I understand what you mean but don't you think they sold off all the tokens? For the members to have a reason not to store token for the investors don't have a reason to sell. I'm gonna agree to that. Investors know that their big returns comes from holding the right assets. For a time if you've invested in Google, Facebook or whatever and you sold early, you would have lost more to the upside and made lots of investors know that on current support but some investors will want to that and that's undoubtedly true  and a lot of circumstances for that investors and restrains in the market.so uh yeah.

Guess that's my answer there. Any more questions or stay a bit longer so people can type something if they want to. A friend says what's the only way to get some pairs .

Think you should know this is always worth quite a bit, so,  I mean at this point this not any point you can reverse or something  but me myself, I would always prefer to have more options like there would be a good reason to hold a long period of time if I pull in something.

You said that it is quite important to realise that we are also in your issue. We might say we want to give investors sweet deal, because that will make them better off than anyone else than anyone on the table

When you try to treat investors differently, it can also get complicated wanting to be a smooth process so we spend lots of time trying to put everything together and have everybody be happy with all sorts of terms. Alright, so let's see here.

The next question is again from swazenlinko, please correct me if I'm not pronouncing that correctly. if we manage to give them a part of the tokens after 12 months, it's up to you of course.

well it's more of a transaction between both parties but I get what you mean.

Until someone commits the genesis block into the I'm trying if you don't update anyone or have you done the final testing we can keep changing the locations and the we're not bound by really anything so you can keep doing that and I'm going to talk more about what they do what we do that so the last day is very close before the mainnet launch.

Getting a Question now from Obiechina Odo:

Obiechina: For someone who just joined a working group, what's the fastest way to earn enough to join the funding number program?

I mean the best way to earn enough is to have large number of positions that pay a lot talking I don't know if you can convince your lead to give you a bigger salary because you'll take on more tasks or it would have to be something like that because it getting more tJOY is what gives you more  JOY that would be the mechanism by which you could increase your likelihood of getting as much as possible but I wouldn't sweat it if I were just keep plugging away that would be my suggestion.

Then the question is from swazenlinko again, I'm sorry, how many numbers do you want to see now by the end of the program?

We're not explicitly targeting we never really targeted I gave an estimate on the handbook which strike to say something out well if we make assumptions about redundancy and how what kind of scale we are operating what would we like to see but this was never something that was kind of in the forward out we want as many as many excellent people as possible but we don't dwell on the number of specifically.

I don't actually know how many great people there are who are even in this category of not inductive but on 50k but more importantly perhaps less than 50k and there is an argument from the community cus that's really the point.

It's much more important to capture  someone who is a really great contributor but who ended up not getting that many founding member points so sorry I think that they give a JOY allocation compared to getting a large number of people who are sort of so medium to low level of commitment.

So we don't really do that much. If you look at the really see your people in this category it's hard to say how many tomatoes in some it's like an average contributor worth around some is kindly replaceable cuz they are you know they just have this proportionate

Alright, where was I, I was here.

Someone asked, the reason for his question is the possibility of having for example 14.9k just before mainnet, that will be sad to those who will make it almost. I agree, I agree. We will definitely try to uhh, to avoid that scenario , I agree . Uhm , I wanted us to make a remark. I'm not sure for this question to get more involved because a deputy becomes a lead. There's lots of open positions one can make.

Great, okay, yes, tomatoes have announced that he wanted to talk to us making this remark. Some part of his allocation away to newcomers. I'm not sure what he says with that but he did say that as well. Maybe I could just jump into this conclusion of what we do.

First of all Martin will KYC the not inducted but need to be inducted to 18 people on this list obviously that's happening just to be patient we have not forgotten about you I encourage people to keep earning JOY that is a good idea overall there is, you never want no exactly how long it's going to take these are estimates and I didn't think there are a lot of opportunities still and we will I guess I can explicitly, that JOY above and beyond first of all the limits I think needs to be re examined and I think we are trying to find individuals who should be getting more because they are particularly valuable but they didn't have enough time to accumulate as much so there will be undoubtedly some people you know that will think it isn't fair but at the end of the day we will have to reward people that you know how to train as well as they can and who have a lot of value to bring to the project as they just showed up at different times so I would encourage people to commit to share more about who they think that is including themselves that's fine because that isn't where the profit is going. We are trying to do something more formal, I don't know exactly but we need to try and work around the rigidity of the program because that worked fine while we were sort of running but now we're towards the tail end and we're getting towards actually launching and now the point is more to get the right people the bigger share potentially the more than zero than the other one we get.

All right, going for one time, the question is, does anyone have any questions?

Okay all right must be all clear okay it was a question at the end.

What do you think about reducing resting for tomatoes for people because they have been working very hard?

Uhm, you're saying reducing resting as the reward because they worked for so long, uhmmm

I mean I think the reward is kind of reflected in the bigger allocation than he already has , but not sure of the vesting Christa is something that you will want to specifically target in terms of what you want to reward someone with,  it  is better at more resting but bigger share, that's what people will want.

Is it possible to reconcile the JOY allocation earned by the programme participant? Incentives 3.0 is transparent enough,but before the incentives 3.0 it's like complete darkness.

So this is what I try to break down here

Where that comes from , we're gonna put that in the handbook for historical purposes of which people can always figure out.  Of course they will be the specialty part as well and there will be potentially limited changes but at least this is the backstory so we should put that on a book so people can always check how this came about.

Kate asks only a few weeks left before the new testnet  where we'll have no tJoys, is it right? What about the withdrawal of tJoys? Will everyone be able to exchange their tJoys to BCH? I've been trying to do it several times, but I can't because the cashout is empty.

I think this has been fixed but basically the answer is you will be able to withdraw it you should be going with almost your feeling charitable and I believe that works  right Martin?

Yeah, we've been processing, there was a previous back log, but it's been addressed continuously, so a lot of it has been completed and if you are still missing something, I think we should send an email to [cashout@jsgenesis.com](mailto:cashout@jsgenesis.com) with your information.

(Another question) . Eclipsingbinary: thoughts on modular DAOs? Should Atlas be its own DAO? Where the Joystream DAO deals with the governance of the Blockchain and the Atlas DAO governs Atlas.

I think that there should be many as I said I think you maybe working but what other thing we are doing for mainnet is making out with a stand-alone brand so it's not just understood it's being joystream and then we're going to make it easy for people to make their own branded versions about us remaining so you'll have atlas and full apps and all kind with her different logos and names powered by the same underlying data layer from the joystream blockchain and those properties can of course to be run by DAOs I think that's interesting that will be really cool .

I don't think those DAOs need to be in the joystream blockchain themselves that is the same there like whatever they are token is and whatever their governance features are I don't think we need to build that I think I guess this one of those in the future features but I think we should definitely add a smart contract environment to the joystream train and allow it  to plug into things like memberships and that would allow people deploy smart contracts.

So in that case they could actually do what you're saying, but I don't think that specifically is important in order to allow DAOs to own kind of front ends for these kind of products powered by joystreams but I think that would be cool but I don't think we should invest heavily in it. Either people run it on a different or people been deployed on the smart contract environment that we can't add the choice from I think we probably should not put much effort into it so I hope that answers the question I know tomato was very passionate about this but I basically told tomato that we should not invest  a lot of effort and building DAO that are yet another governance thing that I will get right and invest a lot of effort for it to work.

Yeah so I hope someone does that . . .

Question: So If I want to upload a new video or app, should I wait for a new video or testnet, should I wait or will they be transported to the mainnet?

They will not be transported so to speak over to Carthage I doubt they'll be transported over to mainnet I know that's a downer we are going to be basically rewarding creators for uploading their content back to Carthage so it's not just empty and we kind of you know it's effort to be popular we publish stuff again it's a pain in the behind so I think we will do that to make sure that was just kind of powered by something but unfortunately I would expect that one to be really done again for maintenance but then not after that that will give the last one. I promise.

So, it's an excuse for us to reward some of the good creators that have been active on the platform. Cool

Ismail.malik is asking : council has power to pass any proposal they want or there would be some kind of restriction? (On mainnet)

New council can cancel steps of previous council by proposal? (in mainnet)

For The first one, Yes you can pass any proposal you want but you have to remember that for different proposals you may have it as they have been meant to pass multiple councils so I run the time upgrade we haven't pinned down these exact numbers but let's say let's say accounts for a month and you want to do run upgrade that sounds to me like you don't should have left you need to pass at least two or maybe three councils so accountable as a body can pass any proposals but any given council cannot be passed whatever they want but they're a bunch of proposals will be kind of suggesting after mainnet launch,  we're kind of keeping it I wanted it now just to put up increase the scope but I think there's room for lots of new interesting proposals that will need different kind of it's called constitutionality basically in the system number of councils that given proposal has to pass before except executed. So that's clear, the new council can cancel steps of the previous council. Yes cuz I don't even remember if we have those proposals( yeah we do)

Yep so the council  does have some restrains there. Isn't it asking something up my questions again to reduce risk of them being skipped what's the status of YouTube that was advertised long time ago and it was supposed to be used as a backup for their channels like a big upside initiative which we just haven't been able to execute it on it because the person we hired for this engineer is based in Ukraine and we basically walks contact with this person and we have not heard from them for a long period of time they made a lot of progress but and after that we have been kind of in lindville about taking it up again so the world we will be doing as part of the minute launch is to do a kind of a we will be launching a creator program which will for YouTube players kind of incentivize them to authenticate and connect their channel and then in the future we'll do the same thing so we're kind of taking a halfway step in that direction so there will be an inside of a creators to try to use the platform but the syncing automated syncing will not be ready for main net you know play almost by some miracle and yeah it's not clear exactly the resources for r use in doing that. Cause it's first of it is non trivial, infrastructure to run but then also you need to have people on staff able to monitor it because they will it will go down if she's will have been a man if things kind of break and you can't support it that could be that pretty bad so that's the status there we don't know it's I think there is a big potential upside there but we have been able to protect it DJ says it decided what to do after it set the screen free. The story was just pretty simple once the mainnet is live, in late August despite basically the system is fully able to operate on its own and it has all the basic features just depends if it's still there, and it plans to operate all the 2023 basically with increasing relevance with basically the plan I hope as many people from just join the Dao throughout that year and you know that's up to each individual person but basically there is no clear future for justice after 2023 that's kind of the end of the road.

Of course some irregularities will probably be removed before that probably ends. Sudo key he is suggested at the get people confused that is a very temporary like booting feature like literally in the first x number of blocks like I had a suit up key in the beginning as well as when it was bootstrapping, it's about their settings off so the was going away before jsgenesis goes away so those are not comparable by skills. Where should funds to pay for future parachain  slots come from?, I hope it has been addressed. So I mean if the parachain suddenly goes up, 3x in price, that will be a problem, but there is an allocation which is pretty conventional.

Question: Is the new KYC provider ready to get to work? Many people are waiting.

That's where we're on, by seeing a bunch of stuff on the chart, has anyone looked at this? What should we cover here?

Let me know , we are just shooting the shit a little bit, talking about people being in such.

How many FM slots are remaining?

Unlimited! There is no such thing as FM slots, sonGoku don't worry about it there are no slots and anyone else becoming a FM member does not attract from your ability to do so.

Unless we keep the limit of the statement like theory.

I'm just going to be negative here.

Don't confuse this person.

We're talking about there, if we get the same like 8 years, then yes but basically we have spilled the beans, I'm not sure also I need to be but basically when we will be making sure that people get allocations irrespective of the 15k limit because I think that's too rigid at this point, who exactly I don't know what terms we willing to be seen but I hope, I already know some people will be recognizing initiatives to try and communicate and establish who that should be.

Alright Freakstactic, will there be a transaction period between Rhodes and Carthage to allow people to unlock all their stakes?

No, I don't think so.

I see his point, it's about bouncers so if you want to continue operating your testnet and you want to cashout I guess you will need to unlock them to be able to cashout. So we can say we will allow some time there. I mean if you want to cashout, you will have to quit your job and stake an amount of time and the current work will be discarded, replaced, anyway,

How much is this we are talking about?, Like how much is staked?

I don't know, but I can sum it up

I can't sum it up, but everything else is like peanuts, isn't it?

Yes, of course if they are staking at the same time.

So I think it will bring the opt to, like if you let us know on time it will give us the opt to migrate those tokens and credit you for them but it's kind of difficult to do because that will ofcourse make your calculations to be rough.

They don't need to actually like do the cash out routine like unstake and send them

But they will have to unstake and sign and prove they own the keys and calculate the price at that moment, so it's not trivial, so I think you may sign away because you know you will just put that on someone else.

Yes, that's right.

50 validations, 20million stake is that?

I guess so but you're not doing the maths correctly. I don't think it's from the token price but the dollar price.

What is the tJoy value of a billion dollars?

I don't know If this is like 64 dollars, then I feel like it's not worth our time, oh wow okay , well, okay.

Ellen says we fire everyone in a storage providers and distributors in advance to keep their nodes running and rehire with low stake and at the end of this term , I think I'm running out of steam cos I'm not able to process that,

Uh, I will smoothly skip to this hard question

Kriptos, Good afternoon, Has Cosmos Blockchain been considered for the Joystream core network deployment? Thank you

Yes it has kriptos,  in fact the first testnet we ran was a cosmos Blockchain but in some ways the mainnet will be in the cosmos actually because if not a parachain , it will be a standalone subswitch thing meaning that we don't depend on any other chain for security. And are you aware cosmos chain has a lot of benefits we want like we only have transactions that will lead to blockchain so we don't need to compete with like your smart contract that enough to do this fast finality you know to wait for real long period of time

I think Cosmos is, not sure exactly but pretty quick.

we're six seconds …six seconds a lot of time you can have interoperability so you could be doing a new bridging substrate and you can receive substrate as well just as you can with Cosmos chain so we won't have interoperability it's like probably not going to be as smooth as being in the chain but there is feasibility.

We really want some substrate because we got to pick, we have the opportunity to parachain and we get to pick whatever we want on different cosmos. And also using rust instead of gold was something that was refractive to us, I think that has been of big time, started higher, but I think you get a more safe runtime code . Cosmos doesn't have some credibility unless you run some smart contract cosmos or something like that so that was a big reason to have forecles upgrades for governance could change the rules  to the game because we had a governance in an accidentalist so those were The reason so I think Cosmos is great and the substrate was better fit for us. Hope that answers the question.

Alright I think I have to draw the line here cuz I'm about to faint, so should we just say that's it for now?.

I think we covered a lot, alright, well thank you everyone, it's good to see y'all, good questions and I guess they'll be a space next week probably and we'll see next time, probably a lot of new interesting things we will cover.

Thank you Robert, Martins and every other person.

Bye

Thank you