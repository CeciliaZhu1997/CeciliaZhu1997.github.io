---
layout: post
title: "[Conference] Are Housewives Getting Depressed? A Machine Learning Study Based on YouTube"
date:   2024-05-30
tags: [research]
comments: true
author: Dongdong
---

***This paper was accepted by the 74th International Communication Association (ICA) Regional Hub Beijing.***

<h3>Abstract</h3>

This study aims to explore housewives’ digital expression based on 1800 videos from YouTube using a supervised machine learning approach. 

Major Depressive Disorder (MDD) has symptoms including feeling depressed or sad, loss of interest, etc., lasting at least two weeks, according to the American Psychiatric Association. It is considered the leading cause of "disease-related disability" among females according to the World Health Organization’s Global Burden of Disease, with females being at 1.5 to 3 times higher risk than males (Kessler, 2003).

Among the different life stages of females, the mental health of housewives is particularly regarded as "one of the most important and urgent issues related to mental health in societies" (Matinzadeh et al., 2020, p.12). During this period, they experience a shift in identity as they adapt to intimate relationships and parenthood, while their dependence on family and children can, in turn, lead to a higher possibility of aggravating reactive depression, according to early research (Spendlove et al., 1981). Another comparative cross-sectional study in Pakistan (Raza et al., 2017) showed that housewives suffer a higher ratio of depression than working women, with a relatively high proportion of 35.6%.

The growing popularity of social media has empowered females with greater autonomy, leading to increased digital self-representation and visibility (Wotanis & McMillan, 2014). A trend has also been observed in recent years where stay-at-home mothers actively produce vlog videos and post them on social media to present their daily parenthood and domestic labor (He et al., 2022). While multiple studies have investigated females’ depression trends with different themes, such as body image (Jackson et al., 2014) and pregnancy (Kajdy et al., 2020), most studies start from psychology. Regarding social media and communication science, a few studies have conducted qualitative analyses such as content analysis (He et al., 2022;  Wotanis & McMillan, 2014) to observe females’ digital self-presentations and motherhood. Yet there is still a lack of quantitive analysis using computational methods to explore housewives’ mental health based on their extensive digital productions on social media.

Therefore, the research question of this study is as follows:<br>

*RQ*: Do housewife-related videos on social media tend to express depression? 

The hypotheses are as follows:<br>
*H1*: Compared to videos related to working women, housewife-related videos on social media express a higher level of depression.<br>
*H2*: Compared to daily vlog videos, housewife-related videos on social media express a higher level of depression.

YouTube was selected as the research platform for this study. Videos with the hashtags #housewife,  #careen women,  and #vlogs were respectively scraped using the YouTube API v3 provided by Google. For each hashtag, 600 videos' URLs were collected, from which the transcripts were extracted using the YouTube Transcript API. Finally, three datasets of texts for each hashtag were prepared.

Supervised machine learning (SML) was used in this study. The labelled dataset for depression detection is cited from @Iremhttp et al. (2023), where more than 27 thousand texts were annotated with labels 1 or 0 to detect if the texts were depressed or not, with a very balanced distribution (50.5% and 49.5%). Using the Bag of Words approach, multiple classifiers were trained with this labelled dataset after pre-processing. Finally, the Support Vector Machine with Tfidf Vectorizer was selected, achieving a performance of 0.93 accuracy. The unlabeled dataset of each hashtag was then labelled based on the trained classifier.

A one-way ANOVA test was conducted to answer the research question. The results indicate that the depression level of videos related to career women (*M* = 0.35, *SD* = 0.48) was significantly higher than videos related to housewives (*M* = 0.17, *SD* = 0.38) and daily vlogs (*M* = 0.07, *SD* = 0.25), *F* = 34.1596, *p* < 0.001.

Regarding the hypotheses, *H1* can be rejected, as housewife-related videos on social media express a lower level of depression compared to videos related to working women. *H2* can be retained, as housewife-related videos on social media express a higher level of depression than regular vlog videos.

In conclusion, this paper conducted a supervised machine learning study and explored over 1800 videos to explore the depression level represented from videos related to housewives, career women and vlogs. It further expanded the restrictions of traditional qualitative analysis in terms of content analysis or digital ethnography, allowing researchers to comprehensively investigate females’ extensive digital representations online. More research will be conducted to further explore females’ visual representations.

