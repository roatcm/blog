+++
date = '2025-01-04'
draft = false
title = 'Being Good Is Never Good Enough'
tags = ['layoffs', 'office politics', 'pushed out', 'data', 'schemas', 'competency']
summary = 'The most technically capable boss I ever had, and why the swines in leadership fed him into the woodchipper.'
+++

It was the week before quarter-end, and the dashboards were lying again. Not small, polite lies either - big, brazen, shameless ones, the kind a used-car salesman tells with his hand on a Bible. I had made the mistake of mentioning, quietly, that the revenue number looked a little strange, and within the hour the whole building had come unglued. Directors were materialising at my desk with the wild, hollow eyes of men who hadn't slept since the last audit, and somewhere down the corridor a senior VP was bellowing into a speakerphone: "Why doesn't this match the board pack? WHY DOESN'T THIS MATCH THE BOARD PACK?"

Nobody knew. Nobody had *ever* known. That was the beauty of the thing.

This is the story of possibly the smartest, most technically capable manager I ever had, and how the beasts I worked for chewed him up and spat him out in barely a year. It is not a pretty story. There is no redemption in it. There is only a data warehouse, and fire, and a good man walking out the door with a cardboard box while the vultures circled the parking lot.

You have to understand what we were dealing with. The company's business intelligence estate was not so much a system as a crime scene. A smoking, reeking dumpster fire of a thing, piled high with orphaned tables and half-dead ETL jobs that ran at 3am for reasons nobody alive could explain. There were reports that pulled from views that pulled from other views that pulled from a spreadsheet on a shared drive belonging to a man named Gerry who had left the company in 2017. Gerry's spreadsheet was load-bearing. If anyone had touched it, the entire finance function would have collapsed like a meth lab in a thunderstorm.

Every morning the warehouse was dropped and refreshed. Wiped clean. Burned to the ground and rebuilt from the ashes, like some demented phoenix that forgot everything it had ever been the moment it woke up. Yesterday's numbers? Gone. Last month's numbers, as they were reported to the board? Gone, mutated, rewritten by whatever late-arriving invoice had crawled in overnight. You could ask the warehouse what revenue was on the 14th of March, and it would tell you, with total confidence, a number that had *never once* been true on the 14th of March.

This was considered normal. This was, in fact, *best practice*. It still is, in a lot of places. God help us all.

Into this smoking hellscape walked Jordan.

He came in as a contractor - a hired gun, brought in to put out the fire and then presumably ride off into the sunset with a day rate and a mild case of PTSD. But something happened. He looked into the abyss, and instead of the abyss looking back, the abyss blinked first. Within four months they'd made him VP of Business Intelligence. It was the fastest promotion I have ever seen in a corporate environment, and I've seen men rise through the ranks on nothing but golf handicaps and a willingness to laugh at the CEO's jokes about his boat.

Jordan was different. Jordan had the best natural understanding of anyone I have ever met - before or since - of not just how a database and a business reporting setup *should* look, but, more importantly, *why*. This is rarer than you'd think. Most people in this business can tell you the what. A handful can tell you the how. Almost nobody can tell you the why without retreating into buzzwords and a slide deck the colour of a hospital waiting room.

He knew about costs. He knew about access, and role-based access controls, and which grubby little fingers should be allowed anywhere near the salary tables. He cared about the repeatability of an analysis - the radical, almost subversive idea that if you ran the same query twice you should get the same answer - with an intensity that nobody before or since has ever bothered to muster. Sitting in a meeting with him was like watching a man calmly defuse a bomb while everyone else in the room argued about what colour the wires should be.

Every great madman has a vision, and Jordan's was beautiful.

He wanted to tear out the drop-and-refresh model entirely and replace it with something that *remembered*. An append-only log of every change to every financial metric. Nothing deleted, nothing overwritten, nothing quietly rewritten in the dead of night. Every number would carry its own history on its back like a turtle. You could stand at any point in time, turn around, and see the world exactly as it had looked - what the warehouse knew, and when it knew it.

Think about what that means. When the CFO stood up in front of the board and said "Q2 revenue was X", you could go back a year later and prove *exactly* what X was at that moment, and exactly which late-arriving garbage had changed it since. No more arguments. No more archaeology. No more hunting through Gerry's spreadsheet like a man digging through a landfill for his wedding ring. Proper Kimball Type II slowly changing dimensions, time-travel, audit trails - the whole sacred, boring, magnificent apparatus that a sane company would sell its grandmother for.

It was the kind of idea that makes people like me go weak at the knees. It was also, I see now, the kind of idea that makes people like *them* deeply, primally nervous. Because a system that remembers everything is a system that remembers what you said, and when you said it, and whether the numbers backed you up. There are certain men in certain corner offices for whom that is a far more terrifying prospect than any dumpster fire.

Jordan's problem - and I say this with love, and with the bitter taste of hindsight in my mouth - was that he was too nice.

He was a lovely, pleasant guy to know and to talk to. You could bring him the wildest, most deranged suggestion - "What if we just put the whole warehouse in a Google Sheet?" - and he would nod along, gently, thoughtfully, like a priest hearing a confession, and then calmly walk you through why the opposite was, in fact, preferable. By the end you'd be agreeing with him and thanking him for the privilege. It was a kind of magic. It was also, in the jungle we were living in, a death sentence.

Because the corporate world is not a seminar. It is a knife fight in a phone box, and the people who win knife fights are the people who *bring knives*. Jordan was smart, he knew his stuff, but there was no blood-lust in the man. None. There was nothing in his make-up that would let him stick the knife into a rival in a public meeting, or hire a sycophant over someone capable just to have another vote in the room. He didn't play politics, at least none that I could see. He just quietly, capably, relentlessly pursued the single goal of saving us from ourselves.

And meanwhile, all around him, the reptiles were doing what reptiles do. Basking. Watching. Flicking their tongues. Every one of them had a pet project or a pet vendor or a pet metric that the new world order would have exposed, and every one of them knew that the nice man with the append-only log would never, ever come for them first. So they came for him.

For that, much like some kind of BI Jesus, he was betrayed and crucified. Only there was no resurrection on the third day. There was just a calendar invite titled "Quick chat" from someone in HR.

He told me at our weekly sync. Same room, same time, same bad coffee. He was calm about it - of course he was calm about it, the man was a monk - and he said, with a kind of rueful half-smile, that he was leaving, and that it "wasn't quite by mutual agreement".

I remember staring at him across the table and feeling something cold and ugly crawl up the back of my neck. Not quite by mutual agreement. The most polite way imaginable of saying *they've thrown me off the bus and are now reversing back over me to make sure*.

The evil bastards in leadership had fired probably the one guy in the building who might have turned a few scattered, stinking outhouses into a cathedral of BI reporting. And they did it without a flicker of shame, without understanding what he'd been trying to build, and without caring a hoot about what would happen once he was gone.

What happened once he was gone was exactly what you'd expect.

The dumpster fire re-ignited. Of course it did. It had never really gone out - Jordan had just been standing on the lid. The append-only log was quietly shelved, then forgotten, then referred to in a planning meeting eighteen months later as "that thing Jordan wanted to do" in the same tone you might use for a bad haircut from your twenties. Drop-and-refresh came roaring back like a bad habit. Gerry's spreadsheet, I am told, is still out there somewhere, humming away on a shared drive, holding up the whole rotten edifice like a single matchstick under a piano.

And to this day, in that place, nobody can figure out a way to preserve Kimball Type II table structures in the data warehouse. Ask them what revenue was on the 14th of March and they will tell you a number. It will be wrong. It will always be wrong. And nobody will ever know by how much.

## The Moral, Such As It Is

I have thought about Jordan a lot over the years, usually late at night, usually staring at a query that returns a different answer than it did yesterday.

Here is what I've come to believe, and I hate believing it. In the corporate world, being good is never good enough. Being right is never good enough. You can be the most competent person in the building, you can see the future with perfect clarity, you can have the plan that saves everyone - and none of that will protect you for a single second if you don't also have the stomach to fight for it in the gutter, with the rats, by their rules.

That isn't a lesson about how the world *should* work. It's a dispatch from how it *does*. Somewhere out there Jordan is probably building something beautiful for someone who has the sense to appreciate it. I hope so. I hope they let him keep his history.

The rest of us are still here, in the fire, dropping and refreshing, forgetting everything every morning and calling it progress.
