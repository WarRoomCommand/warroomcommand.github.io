---
layout: page
title: Donor Directions
description: Industries of donors to 2020 presidential campaigns
img: /live_assets/img/single_radar.png

---

<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_pca.png" title="Primary PCA"/>
</div>

Since it's election season, there are hundreds of articles analyzing each candidate's base of support, picking them apart along income, race, gender, and other lines. One avenue that's been underexplored, however, is how support for candidates differs across different professional occupations. When combined with more traditional measures of candidate support, such information could provide a more complete picture of who is voting for which candidates and why.

Unfortunately, there aren't many direct polls that help provide this data. As a result, we used the self-reported employment information provided by political donors to the [FEC](https://projects.propublica.org/itemizer/presidential-contributors/2020) instead. Although people with the means and motivation to donate to political campaigns of course are not fully representative of the overall electorate, the relative support of different candidates within a particular occupational group could still provide us some hints as to how each candidates' base differs.

However, with hundreds of thousands of different people donating this election cycle, manually classifying each job would be intractable. So instead, we hand-classified around 10,000 different jobs and then used a simple Naive Bayes to classify the rest. 

To the best of our knowledge, [OpenSecrets](https://www.opensecrets.org/2020-presidential-race/industry-totals?highlight=y&ind=B02&src=a) has the only other systematic attempt of performing a similar type of analysis. However, our methodology differs from [theirs](https://www.opensecrets.org/industries/methodology.php) in such a way that we think our approach provides greater clarity to the overall presidential race. Most notably, their approach classifies donors based on the industry of their employer, while ours classifies donors based on their job description. So, for example, an executive at Walmart who donates to a campaign would be classified as a "retail" donor under their methodology, while they would be an "executive" under ours.

<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_trump_v_biden.png" title="Trump v. Biden donors"/>
</div>
<div class="col three caption">
    Percentage of Trump and Biden donors that come from each occupation
</div>

Here we look specifically at donors to Trump and Biden in the month of May. Note that what's being measured is not the number of donors to each candidate but rather their degree of reliance on donors from that particular industry. For example, 26% of Trump's donors are managers or executives, while 19% of Biden's donors are managers or executives. Although we did also track the overall number of donors, we found that looking at the candidate's reliance on a particular class of donors was more relevant because some candidates just had substantially more donors than others (for the month of May, Trump had substantially more donors than did Biden while during the primaries, Sanders had way more donors than any other Democratic candidate).

The results from the Trump-Biden comparison are unsurprising. Professors and lawyers disproportionately break towards Biden while blue collar workers disproportionately break towards Trump. Note that the percentages graphed will not add up to 100% because not all occupations that we tracked were shown in the graph -- in total, we tracked seventeen different occupations, with many of the occupations making up only a tiny percentage of overall donors. Moreover, unlike OpenSecrets, we tracked, but did not record retirees -- we found that although retirees do make a high percentage of donors, it appears that different campaigns have offered different guidance to their donors as to how to list their employment status if they are retired; the Trump campaign, for example, has a very high number of "retired" donors and very few "not employed" donors, while Biden is the reverse. Our inability to distinguish between the reasons a person might list themselves as "not employed" caused us to eliminate retirees from our analysis.

<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_main_radars.png" title="Main radar projections"/>
</div>
<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_other_radars.png" title="Other radar projections"/>
</div>
<div class="col three caption">
    Radar projections for the Democratic primary candidates
</div>

In addition to looking at the general election, we also tracked donations to the Democratic primary candidates for the length of 2019. Since this data spanned multiple reporting quarters, we tried to eliminate duplicates by not counting any donor that had the same name, state, and address as another donor that had already been counted. At the top of this post is a projection of all the candidates' donor bases using Principal Component Analysis. The divide between the bases of the more progressive candidates, like Warren and Sanders, and the more moderate candidates, like Klobuchar and Biden, is quite evident from the projection. However, a radar projection better shows precisely how these candidates' bases actually differ. Broadly speaking, the candidates plotted in yellow are substantially more reliant on donations from businesspeople and lawyers than the candidates plotted in blue. Unsurprisingly, the candidates more reliant on businesspeople and lawyers were those perceived as more moderate, like Biden, Klobuchar, Gillibrand, Booker, and Bennet.

<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_popular_bars.png" title="Bar graph of most popular occupations"/>
</div>
<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_medium_bars.png" title="Bar graph of middlingly popular occupations"/>
</div>
<div class="col three caption">
    Reliance by candidate for the more frequently-donating occupations
</div>

Just as the splits among businesspeople and lawyers weren't shocking, so too were the splits among professors and tech workers. Professors broke most towards the more progressive candidates and most heavily towards the former professor Warren. Tech workers, meanwhile, also broke more for Sanders and Warren -- surprising given their more critical stance towards big tech companies but perhaps unsurprising given that the tech industry skews young -- with a significant number also going to the more idiosyncratic candidates Yang, a former tech executive himself, and Gabbard. 

<div class="img center">
	<img class="col three" src="{{ site.baseurl }}/assets/img/donor_directions/dd_unpopular_bars.png" title="Bar graph of less popular occupations"/>
</div>
<div class="col three caption">
    Reliance by candidate for the less frequently-donating occupations
</div>

Here too, we don't have many surprises. Blue-collar workers and service workers were a larger part of Yang and Sanders' base, while workers in the finance industry donated similarly to lawyers and businesspeople. 

