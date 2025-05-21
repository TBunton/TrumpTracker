# TrumpTracker
Truth social scraper which then is analysed by ChatGPT to provide market analysis.

This is my first market analysis project in Python and achieved my outcomes of providing a fast market analysis of Truth Social posts by @realDonaldTrump which is then posted onto my X account https://x.com/TrumpAnalyser.
I hope to improve this project in the future and perhaps incorporate it into an algorithmic trading model in which we trade based on Alpha provided by Donald Trump's posts.

The code works as follows
1. it uses the TruthBrush API which can be found here https://github.com/stanfordio/truthbrush/tree/main to pull the latest truth social post from Donald Trump's Truth Social account every 2 minutes. The wait time can be changed to provide faster post updates but at <60 seconds wait time CloudFlare may temporarily ban your IP from Truth Social.

2. it then checks that the post pulled is different from the previous post.

3. if it is a new post, it is passed onto the ChatGPT model 4o-mini which was chosen for its low token cost but can be changed to whichever model you wish to use. The model follows the system and user prompts given which are strict on the definition of impactful market news. If the news is unlikely to cause market impact we return the word "Pineapple" which I used as I thought it would be very unlikely for that to be included in a post by @realDonaldTrump. (unless he is a fan of pineapples)

4. if the returned word is "Pineapple" no X post is created as it has no market impact. If market analysis is returned then it will be posted onto X.

5. the final outcome will look something like this:

Post from @realDonaldtrump https://truthsocial.com/@realDonaldTrump/posts/114491534347862682

For many years the World has wondered why Prescription Drugs and Pharmaceuticals in the United States States of America were SO MUCH HIGHER IN PRICE THAN THEY WERE IN ANY OTHER NATION, SOMETIMES BEING FIVE TO TEN TIMES MORE EXPENSIVE THAN THE SAME DRUG, MANUFACTURED IN THE EXACT SAME LABORATORY OR PLANT, BY THE SAME COMPANY??? It was always difficult to explain and very embarrassing because, in fact, there was no correct or rightful answer. The Pharmaceutical/Drug Companies would say, for years, that it was Research and Development Costs, and that all of these costs were, and would be, for no reason whatsoever, borne by the “suckers” of America, ALONE. Campaign Contributions can do wonders, but not with me, and not with the Republican Party. We are going to do the right thing, something that the Democrats have fought for many years. Therefore, I am pleased to announce that Tomorrow morning, in the White House, at 9:00 A.M., I will be signing one of the most consequential Executive Orders in our Country’s history. Prescription Drug and Pharmaceutical prices will be REDUCED, almost immediately, by 30% to 80%. They will rise throughout the World in order to equalize and, for the first time in many years, bring FAIRNESS TO AMERICA! I will be instituting a MOST FAVORED NATION’S POLICY whereby the United States will pay the same price as the Nation that pays the lowest price anywhere in the World. Our Country will finally be treated fairly, and our citizens Healthcare Costs will be reduced by numbers never even thought of before. Additionally, on top of everything else, the United States will save TRILLIONS OF DOLLARS. Thank you for your attention to this matter. MAKE AMERICA GREAT AGAIN!

Output Analysis and Tweet:

ANALYSIS:
The post announces a forthcoming Executive Order aimed at reducing prescription drug prices in the U.S. by 30%–80%, invoking a "Most Favored Nation" pricing policy. If credible and implemented, such a policy would have material impact on large pharmaceutical companies that derive significant revenue from U.S. drug pricing premiums. A sudden enforced price alignment with the lowest global rates could compress margins and impact earnings forecasts. However, regulatory, legal, and lobbying resistance could delay or dilute implementation.

TICKERS:
$PFE (Pfizer Inc), $LLY (Eli Lilly and Co), $JNJ (Johnson & Johnson)




I hope this project is useful if anyone is thinking of making their own market sentiment analysis bot. Feel free to contact me with any suggestions about improvements or questions.

- Thomas
