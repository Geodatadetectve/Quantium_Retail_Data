# Quantium_Retail_Data
Data preparation and customer analytics, Experimentation and uplift testing Analytics and commercial application 

Insights
Sales are coming mainly from Budget - older families, Mainstream - young singles/couples, and Mainstream - retirees

There are more Mainstream - young singles/couples and Mainstream - retirees who buy chips. This contributes to there being more sales to these customer segments but this is not a major driver for the Budget - Older families segment.

Older families and young families in general buy more chips per customer.

Mainstream midage and young singles and couples are more willing to pay more per packet of chips compared to their budget and premium counterparts. This may be due to premium shoppers being more likely to buy healthy snacks and when they buy chips, this is mainly for entertainment purposes rather than their own consumption. This is also supported by there being fewer premium midage and young singles and couples buying chips compared to their mainstream counterparts.

## Welch Two Sample t-test
## data:  data[LIFESTAGE %in% c("YOUNG SINGLES/COUPLES", "MIDAGE SINGLES/COUPLES") & PREMIUM_CUSTOMER == "Mainstream", price] and data[LIFESTAGE %in% c("YOUNG SINGLES/COUPLES", "MIDAGE 
## SINGLES/COUPLES") & PREMIUM_CUSTOMER != "Mainstream", price]
## t = 40.61, df = 58792, p-value < 2.2e-16
## alternative hypothesis: true difference in means is greater than 0
## 95 percent confidence interval:
## 0.3429435       Inf
## sample estimates:
## mean of x mean of y 
## 4.045586  3.688165 

The t-test results in a p-value < 2.2e-16, i.e. the unit price for mainstream, young and mid-age singles and couples are significantly higher than that of budget or premium, young and midage singles and couples.

  BRAND targetSegment       other affinityToBrand
 1:   TYRRELLS   0.029586871 0.023912522       1.2372962
 2:   TWISTIES   0.043306068 0.035252480       1.2284545
 3:     KETTLE   0.185649203 0.154084100       1.2048563
 4:   TOSTITOS   0.042581280 0.035346801       1.2046714
 5:        OLD   0.041597639 0.034722996       1.1979853
 6:   PRINGLES   0.111979706 0.093662914       1.1955608
 7:    DORITOS   0.122877407 0.106044691       1.1587323
 8:       COBS   0.041856492 0.036343603       1.1516880
 9:  INFUZIONS   0.060649203 0.053111307       1.1419264
10:      THINS   0.056611100 0.053038423       1.0673602
11:    GRNWVES   0.030674053 0.029027293       1.0567314
12:   CHEEZELS   0.016851315 0.017355067       0.9709738
13:     SMITHS   0.093419963 0.121609803       0.7681943
14:     FRENCH   0.003701595 0.005359149       0.6907057
15:    CHEETOS   0.007532615 0.011230632       0.6707205
16:        RRD   0.045376890 0.068367732       0.6637179
17:    NATURAL   0.018378546 0.028716462       0.6400004
18:        CCS   0.010483537 0.017586582       0.5961100
19:   SUNBITES   0.005953614 0.011708668       0.5084791
20: WOOLWORTHS   0.028189066 0.057379333       0.4912756
21:     BURGER   0.002743839 0.006139441       0.4469201
         BRAND targetSegment       other affinityToBrand

We can see that :
• Mainstream young singles/couples are 23% more likely to purchase Tyrrells chips compared to the rest of the population
• Mainstream young singles/couples are 56% less likely to purchase Burger Rings compared to the rest of the population

 PACK_SIZE targetSegment       other affinityToPack
 1:       270   0.029845724 0.023357314      1.2777892
 2:       330   0.057465314 0.046686760      1.2308696
 3:       380   0.030156347 0.024669233      1.2224274
 4:       134   0.111979706 0.093662914      1.1955608
 5:       110   0.099658314 0.083570565      1.1925050
 6:       210   0.027308967 0.023380894      1.1680035
 7:       135   0.013848623 0.012169555      1.1379728
 8:       250   0.013460344 0.011895166      1.1315809
 9:       170   0.075740319 0.075375355      1.0048420
10:       300   0.054954442 0.057214272      0.9605023
11:       175   0.239102299 0.251301201      0.9514570
12:       150   0.155130462 0.163306123      0.9499366
13:       165   0.052184717 0.057953834      0.9004532
14:       190   0.007014910 0.011580049      0.6057755
15:       180   0.003365086 0.005646399      0.5959703
16:       160   0.006005384 0.011515739      0.5214936
17:        90   0.005953614 0.011708668      0.5084791
18:       125   0.002821495 0.005618532      0.5021766
19:       200   0.008412715 0.017363642      0.4845017
20:        70   0.002847380 0.005884345      0.4838908
21:       220   0.002743839 0.006139441      0.4469201
    PACK_SIZE targetSegment       other affinityToPack

It looks like Mainstream young singles/couples are 27% more likely to purchase a 270g pack of chips compared to the rest of the population but let’s dive into what brands sell this pack size.

[1] "Twisties Cheese     270g" "Twisties Chicken270g"  
Twisties are the only brand offering 270g packs and so this may instead be reflecting a higher likelihood of purchasing Twisties

Conclusion
Sales have mainly been due to Budget - older families, Mainstream - young singles/couples, and Mainstream retirees shoppers. We found that the high spend in chips for mainstream young singles/couples and retirees is due to there being more of them than other buyers. Mainstream, midage and young singles and couples are also more likely to pay more per packet of chips. This is indicative of impulse buying behaviour.

We’ve also found that Mainstream young singles and couples are 23% more likely to purchase Tyrrells chips compared to the rest of the population. The Category Manager may want to 
increase the category’s performance by off-locating some Tyrrells and smaller packs of chips in discretionary space near segments where young singles and couples frequent more often to increase visibilty and impulse behaviour. 

Quantium can help the Category Manager with recommendations of where these segments are and further help them with measuring the impact of the changed placement. We’ll work on measuring the impact of trials in the next task and putting all these together in the third task.

