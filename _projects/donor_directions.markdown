---
layout: page
title: Donor Directions
description: Industries of donors to 2020 presidential campaigns
img: /live_assets/img/dd_all_radars.png
---

Since it's election season, there are hundreds of articles analyzing each candidate's base of support, picking them apart along income, race, gender, and other lines. One avenue that's been underexplored, however, is how support for candidates differs across different professional occupations. When combined with more traditional measures of candidate support, such information could provide a more complete picture of who is voting for which candidates and why.

Unfortunately, there aren't many direct polls that help provide this data. As a result, we used the self-reported employment information provided by political donors to the [FEC](https://projects.propublica.org/itemizer/presidential-contributors/2020) instead. Although people with the means and motivation to donate to political campaigns of course are not fully representative of the overall electorate, the relative support of different candidates within a particular occupational group could still provide us some hints as to how each candidates' base differs.

However, with hundreds of thousands of different people donating this election cycle, manually classifying each job would be intractable. So instead, we hand-classified around 10,000 different jobs and then used a simple Naive Bayes to classify the rest. 

To the best of our knowledge, [OpenSecrets](https://www.opensecrets.org/2020-presidential-race/industry-totals?highlight=y&ind=B02&src=a) has the only other systematic attempt of performing a similar type of analysis. However, our methodology differs from [theirs](https://www.opensecrets.org/industries/methodology.php) in such a way that we think our approach provides greater clarity to the overall presidential race. Most notably, their approach classifies donors based on the industry of their employer, while ours classifies donors based on their job description. So, for example, an executive at Walmart who donates to a campaign would be classified as a "retail" donor under their methodology, while they would be an "executive" under ours.

<div class="img">
	<img src="{{ site.baseurl }}/assets/img/donor_directions/dd_trump_v_biden.png" title="Trump v. Biden donors"/>
</div>

