# Using Samsung Pay to Open Doors

## Background 
Samsung Pay is Samsung's "wallet" app that allows you to use your phone to store cards and make payments using your phone, similar to Google Pay and Apple pay. What separates Samsung Pay from other apps is on Samsung phones there is an added technology called Magnetic Secure Transmission (MST). MST mimics magnetic swipes, such as when you swipe a debit card at a terminal to pay for an item. However, using Samsung Pay we can expand the capabilities of this technology to do more than just pay for a morning coffee. 

At the College I attend, every student and employee has an ID card that you can swipe in one of these ![card swipe](https://github.com/L1t3Br1t3/L1t3Br1t3.github.io/blob/master/ITEMS_SWIPECARD_LENEL_LNL-2005W.jpg) to unlock doors and get into buildings. After losing my card one day and getting locked out of my building, I had an idea: Could I use put my ID card in Samsung Pay so I can get back to my room even if I don't have my card on me? 

## Step 1: Find Out What Data Is On My ID Card
Before putting any information into Samsung Pay about my ID Card, I needed to figure out what data was on the card. I got a magnetic card reader ![card reader](https://github.com/L1t3Br1t3/L1t3Br1t3.github.io/blob/master/card_reader.jpg) to accomplish this. Open up notepad, plug in the reader to your computer, and swipe the card. For my card, this resulted in the output in the format
```
;5555555501?
```
In my case, my school's ID cards use "Track 2", which begins with the "start sentinel" ```;``` and "end sentinel" ```?```. Other places cards might not be the same format depending on the standard used. The "55555555" represents my student ID, a number assigned to me and only me, which is written on the front of my ID card. I am not certain what the two numbers at the end represent. For me, it was "01". From my research, I saw the theory that this could be how many times your card has been replaced. In my case, I had not replaced my card, so it starts at "01". I got my friends to swipe their cards, and theirs ended in "01" as well and they had not replaced their card before either. Later, for my job at the school, I was given access to card swipe data for faculty and students and I was able to look at what number was after the ID. I only saw between "01" and "07", so even if you do not have a card swipe reader you could guess what number is appended after your ID very quickly.

## Step 2: Putting data in Samsung Pay
Now that I knew what data was on my card, it was time to put it in a card in Samsung Pay. Open Samsung Pay, go to "Add card", and select "Membership". At a glance, "credit/debit card", "SamsungPay Cash", and "PayPal" all sounded like they would not work for this purpose because the card numbers are longer, there are expiration dates, and security codes of some sort. "Gift" cards sounded promising, but they also add the complexity of PINs. This leaves "Membership". 

There are a ton of different cards to choose from, but for our purposes we can break them into two different groups. Ones that just create a barcode, and others that actually enable the magnetic swipe using the MST. If it just creates a barcode, such as a "24 Hour Fitness" membership card ![barcode](https://github.com/L1t3Br1t3/L1t3Br1t3.github.io/blob/master/barcode.jpg)
it won't work for our purposes.

At the moment, I know the "Panera Bread" card uses MST, so select the Panera Bread card. I do not know what other cards use MST as opposed to just making a barcode, but you only need to find one to make this work. 
![panera](https://github.com/L1t3Br1t3/L1t3Br1t3.github.io/blob/master/panera.jpg)

When you add a new card, enter the numbers that you got from the swipe (e.g. 5555555501), or your ID plus the two numbers in the "Card number (required)" field. Don't include the start and end characters (';' and '?'). You'll know if the card uses MST when you select the card and press "Use card", the message "Place the back of your phone against the card reader." pops up. If you see that, then success! To open doors now as if you were swiping your actual ID card, select that Samsung Pay card, press "use card", and hold your phone against the card reader. 

## Potential Security Issues
I was able to effectively clone my ID card with just a Samsung phone, and 2 pieces of information: my ID and the number right after. A person's ID is not exactly a secret, as it is printed (in large font) right on the front of the card. And the number that is added after the ID has very few possible choices, anywhere between "01" and "07" from my research. This would be trivial to brute force as you could just make cards starting at "01" and work your way up. If you know someone else's ID number you essentially have a copy of their ID card, and you would have access to the same rooms and buildings that they do. All you would have to do is take note of a person's ID the next time they go to swipe into a room, or look as they pay for a drink at the cafe, since most people pay for food and drinks using their ID card. 

## Conlusion
If you have a Samsung phone and you are a student or faculty at a College, or you have some other ID card similar to this, I would recommend using this guide to put that card on your phone. It bailed me out multiple times when I forgot to bring my physical card somewhere.

I think this is a cool example of using something in an unintended way. And I'd encourage anyone reading to think of even more new ways to use this neat technology! :)
