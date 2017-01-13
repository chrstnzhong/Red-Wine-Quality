
Red Wine Quality by Christina Zhong
===================================

Introduction
============

I would like to investigate this dataset on red wines and their attributes in order to better understand how variables are related to the quality of a wine. Each wine was evaluated on a scale of 1 to 10, with 10 being the best, by three wine experts. I am curious to see how certain attributes may play more heavily in the taste of a red wine.

Univariate Plots Section
========================

    ## 'data.frame':    1599 obs. of  13 variables:
    ##  $ X                   : int  1 2 3 4 5 6 7 8 9 10 ...
    ##  $ fixed.acidity       : num  7.4 7.8 7.8 11.2 7.4 7.4 7.9 7.3 7.8 7.5 ...
    ##  $ volatile.acidity    : num  0.7 0.88 0.76 0.28 0.7 0.66 0.6 0.65 0.58 0.5 ...
    ##  $ citric.acid         : num  0 0 0.04 0.56 0 0 0.06 0 0.02 0.36 ...
    ##  $ residual.sugar      : num  1.9 2.6 2.3 1.9 1.9 1.8 1.6 1.2 2 6.1 ...
    ##  $ chlorides           : num  0.076 0.098 0.092 0.075 0.076 0.075 0.069 0.065 0.073 0.071 ...
    ##  $ free.sulfur.dioxide : num  11 25 15 17 11 13 15 15 9 17 ...
    ##  $ total.sulfur.dioxide: num  34 67 54 60 34 40 59 21 18 102 ...
    ##  $ density             : num  0.998 0.997 0.997 0.998 0.998 ...
    ##  $ pH                  : num  3.51 3.2 3.26 3.16 3.51 3.51 3.3 3.39 3.36 3.35 ...
    ##  $ sulphates           : num  0.56 0.68 0.65 0.58 0.56 0.56 0.46 0.47 0.57 0.8 ...
    ##  $ alcohol             : num  9.4 9.8 9.8 9.8 9.4 9.4 9.4 10 9.5 10.5 ...
    ##  $ quality             : int  5 5 5 6 5 5 5 7 7 5 ...

![](projectTemplate_files/figure-markdown_github/Histograms1-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    4.60    7.10    7.90    8.32    9.20   15.90

![](projectTemplate_files/figure-markdown_github/Histograms2-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.1200  0.3900  0.5200  0.5278  0.6400  1.5800

The range for volatile acidity is much smaller than the range is for fixed acidity. However both distributions are slightly skewed right as they may have some relation to each other. I will explore this later in the bivariate plots section.

![](projectTemplate_files/figure-markdown_github/Histograms3-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   0.000   0.090   0.260   0.271   0.420   1.000

It seems many of the wines have close to no citric acid. Although citric acid can add "freshness" to the taste of the wine, I wonder if such small amounts of citric acid will be noticeable.

![](projectTemplate_files/figure-markdown_github/Histograms4-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   0.900   1.900   2.200   2.539   2.600  15.500

![](projectTemplate_files/figure-markdown_github/Histograms4-2.png)

    ##     Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
    ## -0.04576  0.27880  0.34240  0.36930  0.41500  1.19000

Most of the red wines have around 2-3 grams of sugar per liter.

![](projectTemplate_files/figure-markdown_github/Histograms5-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ## 0.01200 0.07000 0.07900 0.08747 0.09000 0.61100

![](projectTemplate_files/figure-markdown_github/Histograms5-2.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  -1.921  -1.155  -1.102  -1.088  -1.046  -0.214

Most red wines have around 0.1 grams of salt per liter.

Similar to citric acid, I wonder if such small amounts of residual sugar and chlorides will affect the taste of the wine.

![](projectTemplate_files/figure-markdown_github/Histograms6-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    1.00    7.00   14.00   15.87   21.00   72.00

![](projectTemplate_files/figure-markdown_github/Histograms6-2.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.0000  0.8451  1.1460  1.1060  1.3220  1.8570

![](projectTemplate_files/figure-markdown_github/Histograms7-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    6.00   22.00   38.00   46.47   62.00  289.00

![](projectTemplate_files/figure-markdown_github/Histograms7-2.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.7782  1.3420  1.5800  1.5640  1.7920  2.4610

As free sulfur dioxide and total sulfur dioxide are both right skewed, I wonder how strongly they are related to each other. Again, I will revisit this in the bivariate plots section.

The median total sulfur dioxide is 38 ppm while the mean sulfur dioxide is 46.47 ppm. Only concentrations over 50ppm are noticeable in the taste of the wine. How many of the red wines have a ppm of 50 or above?

    ## [1] 557

There are 557 wines with a ppm level of 50 or above, which makes up 35% of the wines.

![](projectTemplate_files/figure-markdown_github/Histograms8-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.9901  0.9956  0.9968  0.9967  0.9978  1.0040

Density has a fairly normal distribution with an extremely small range. 50% of the wines have a density between 0.9956 and 0.9978.

![](projectTemplate_files/figure-markdown_github/Histograms9-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   2.740   3.210   3.310   3.311   3.400   4.010

The distribution of pH levels is also fairly normal. The mean and median are almost the same. 50% of the wines have a pH level between 3.21 and 3.40.

![](projectTemplate_files/figure-markdown_github/Histograms10-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##  0.3300  0.5500  0.6200  0.6581  0.7300  2.0000

![](projectTemplate_files/figure-markdown_github/Histograms11-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##    8.40    9.50   10.20   10.42   11.10   14.90

The median alcohol content is 10.20% and the mean is 10.41%. However there is a spike in the number of wines with an alcohol content of around 9.5%

![](projectTemplate_files/figure-markdown_github/Histograms12-1.png)

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   3.000   5.000   6.000   5.636   6.000   8.000

Most wines received a 5 or 6 rating, with very few receiving a very bad (3) rating or a very good (8) rating.

Univariate Analysis
===================

### What is the structure of your dataset?

The dataset consists of 1599 observations with 11 input variables and 1 output variable.

Input Variables:

-   Fixed Acidity
-   Volatile Acidity
-   Citric Acid
-   Residual Sugar
-   Chlorides
-   Free Sulfure Dioxide
-   Total Sulfure Dioxide
-   Density
-   pH
-   Sulphates
-   Alcohol

Ouput Variable: Quality (score between 0 and 10, with 10 being the best)

Observations:

-   Most wines are rated a quality score of either a 5 or 6, with none dropping below 3 and none receiving a score higher than 8.
-   Most of the wines have a volatile acidity level between 0.2 and 0.8
-   75% of wines have citric acid levels less than 0.42
-   The median residual sugar level is 2.2 gram/liter
-   35% of wines have total sulfur dioxide concentrations over 50 ppm
-   The middle 50% of wines have pH levels between 3.2 and 3.4
-   The median percent alcohol content of the wines is 10.2%

### What is/are the main feature(s) of interest in your dataset?

I am interested in determining which variables impact the quality of the wine the most. The main features of interest in this dataset are alcohol, volatile acidity, citric acid, residual sugar, total sulfur dioxide, and chloride levels as I believe these would affect the taste of the red wine.

### What other features in the dataset do you think will help support your investigation into your feature(s) of interest?

As some of the variables may be correlated, I am interested to see if fixed acidity and free sulfur dioxide also affect the quality of the wine as they seem to be linked to volatile acidity and total sulfur dioxide respectively.

### Of the features you investigated, were there any unusual distributions? Did you perform any operations on the data to tidy, adjust, or change the form of the data? If so, why did you do this?

I log-transformed residual sugar, chlorides, free sulfur dioxide, and total sulfur dioxide as these distributions were skewed right. The transformed distribution for all of these were unimodal with the exception of free sulfure dioxide which seems to be bimodal.

Bivariate Plots Section
=======================

Although we looked at the distribution of each attribute in the univariate section, I'm curious to see how distributions may vary across the different qualities.

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality1-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_fixed.acidity median_fixed.acidity
    ##     <int>              <dbl>                <dbl>
    ## 1       3           8.360000                 7.50
    ## 2       4           7.779245                 7.50
    ## 3       5           8.167254                 7.80
    ## 4       6           8.347179                 7.90
    ## 5       7           8.872362                 8.80
    ## 6       8           8.566667                 8.25

The distribution for fixed acidity becomes more normal as the quality increases.

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality2-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_volatile.acidity median_volatile.acidity
    ##     <int>                 <dbl>                   <dbl>
    ## 1       3             0.8845000                   0.845
    ## 2       4             0.6939623                   0.670
    ## 3       5             0.5770411                   0.580
    ## 4       6             0.4974843                   0.490
    ## 5       7             0.4039196                   0.370
    ## 6       8             0.4233333                   0.370

The distribution for volatile acidity becomes more right-skewed as the quality increases. Although fixed acidity and volatile acidity had similar overall distributions, it seems as if the distributions are very different when grouping by quality. These two attributes may not be as closely related as I originally thought.

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality3-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_citric.acid median_citric.acid
    ##     <int>            <dbl>              <dbl>
    ## 1       3        0.1710000              0.035
    ## 2       4        0.1741509              0.090
    ## 3       5        0.2436858              0.230
    ## 4       6        0.2738245              0.260
    ## 5       7        0.3751759              0.400
    ## 6       8        0.3911111              0.420

The distribution for citric acid seems to become more normal as the quality increases. This is similar to the distribution for fixed acidity. I will explore later how correlated citric acid and fixed acidity are.

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality6-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_free.sulfur.dioxide median_free.sulfur.dioxide
    ##     <int>                    <dbl>                      <dbl>
    ## 1       3                 11.00000                        6.0
    ## 2       4                 12.26415                       11.0
    ## 3       5                 16.98385                       15.0
    ## 4       6                 15.71160                       14.0
    ## 5       7                 14.04523                       11.0
    ## 6       8                 13.27778                        7.5

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality7-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_total.sulfur.dioxide median_total.sulfur.dioxide
    ##     <int>                     <dbl>                       <dbl>
    ## 1       3                  24.90000                        15.0
    ## 2       4                  36.24528                        26.0
    ## 3       5                  56.51395                        47.0
    ## 4       6                  40.86991                        35.0
    ## 5       7                  35.02010                        27.0
    ## 6       8                  33.44444                        21.5

The distributions of free sulfur dioxide and total sulfur dioxide seem to move in the same direction depending on the quality of the wine. This again reinforces my suspicion that they are related. I will investigate their correlation more later in this section.

![](projectTemplate_files/figure-markdown_github/Distribution_by_quality11-1.png)

    ## # A tibble: 6 × 3
    ##   quality mean_alcohol median_alcohol
    ##     <int>        <dbl>          <dbl>
    ## 1       3     9.955000          9.925
    ## 2       4    10.265094         10.000
    ## 3       5     9.899706          9.700
    ## 4       6    10.629519         10.500
    ## 5       7    11.465913         11.500
    ## 6       8    12.094444         12.150

The distribution seems to vary widely by quality for alcohol levels, with a right-skewed distribution for a quality score of 5

Now I want to create a couple of correlation matrixes in order to see the relationship among all of the variables.

    ##                                 X fixed.acidity volatile.acidity
    ## X                     1.000000000   -0.26848392     -0.008815099
    ## fixed.acidity        -0.268483920    1.00000000     -0.256130895
    ## volatile.acidity     -0.008815099   -0.25613089      1.000000000
    ## citric.acid          -0.153551355    0.67170343     -0.552495685
    ## residual.sugar       -0.031260835    0.11477672      0.001917882
    ## chlorides            -0.119868519    0.09370519      0.061297772
    ## free.sulfur.dioxide   0.090479643   -0.15379419     -0.010503827
    ## total.sulfur.dioxide -0.117849669   -0.11318144      0.076470005
    ## density              -0.368372087    0.66804729      0.022026232
    ## pH                    0.136005328   -0.68297819      0.234937294
    ## sulphates            -0.125306999    0.18300566     -0.260986685
    ## alcohol               0.245122841   -0.06166827     -0.202288027
    ## quality               0.066452608    0.12405165     -0.390557780
    ##                      citric.acid residual.sugar    chlorides
    ## X                    -0.15355136   -0.031260835 -0.119868519
    ## fixed.acidity         0.67170343    0.114776724  0.093705186
    ## volatile.acidity     -0.55249568    0.001917882  0.061297772
    ## citric.acid           1.00000000    0.143577162  0.203822914
    ## residual.sugar        0.14357716    1.000000000  0.055609535
    ## chlorides             0.20382291    0.055609535  1.000000000
    ## free.sulfur.dioxide  -0.06097813    0.187048995  0.005562147
    ## total.sulfur.dioxide  0.03553302    0.203027882  0.047400468
    ## density               0.36494718    0.355283371  0.200632327
    ## pH                   -0.54190414   -0.085652422 -0.265026131
    ## sulphates             0.31277004    0.005527121  0.371260481
    ## alcohol               0.10990325    0.042075437 -0.221140545
    ## quality               0.22637251    0.013731637 -0.128906560
    ##                      free.sulfur.dioxide total.sulfur.dioxide     density
    ## X                            0.090479643          -0.11784967 -0.36837209
    ## fixed.acidity               -0.153794193          -0.11318144  0.66804729
    ## volatile.acidity            -0.010503827           0.07647000  0.02202623
    ## citric.acid                 -0.060978129           0.03553302  0.36494718
    ## residual.sugar               0.187048995           0.20302788  0.35528337
    ## chlorides                    0.005562147           0.04740047  0.20063233
    ## free.sulfur.dioxide          1.000000000           0.66766645 -0.02194583
    ## total.sulfur.dioxide         0.667666450           1.00000000  0.07126948
    ## density                     -0.021945831           0.07126948  1.00000000
    ## pH                           0.070377499          -0.06649456 -0.34169933
    ## sulphates                    0.051657572           0.04294684  0.14850641
    ## alcohol                     -0.069408354          -0.20565394 -0.49617977
    ## quality                     -0.050656057          -0.18510029 -0.17491923
    ##                               pH    sulphates     alcohol     quality
    ## X                     0.13600533 -0.125306999  0.24512284  0.06645261
    ## fixed.acidity        -0.68297819  0.183005664 -0.06166827  0.12405165
    ## volatile.acidity      0.23493729 -0.260986685 -0.20228803 -0.39055778
    ## citric.acid          -0.54190414  0.312770044  0.10990325  0.22637251
    ## residual.sugar       -0.08565242  0.005527121  0.04207544  0.01373164
    ## chlorides            -0.26502613  0.371260481 -0.22114054 -0.12890656
    ## free.sulfur.dioxide   0.07037750  0.051657572 -0.06940835 -0.05065606
    ## total.sulfur.dioxide -0.06649456  0.042946836 -0.20565394 -0.18510029
    ## density              -0.34169933  0.148506412 -0.49617977 -0.17491923
    ## pH                    1.00000000 -0.196647602  0.20563251 -0.05773139
    ## sulphates            -0.19664760  1.000000000  0.09359475  0.25139708
    ## alcohol               0.20563251  0.093594750  1.00000000  0.47616632
    ## quality              -0.05773139  0.251397079  0.47616632  1.00000000

![](projectTemplate_files/figure-markdown_github/Scatterplot_Matrix-1.png)

It seems as if alcohol, volatile acidity, and sulphates have the highest level of correlation to quality. Residual sugar, free sulfur dioxide, and pH have the lowest correlation to quality.

As I suspected, fixed acidity and volatile acidity do not have as strong of a relationship to each other (Pearson's R of -0.26). However citric acid's correlation to fixed acidity is one of the strongest in the set (Pearson's R of 0.67). Free sulfur dioxide and total sulfur dioxide also share one of the highest correlation (Pearson's R of 0.67).

Next I'll graph the relationship between quality and the various attributes to visually see their correlations.

![](projectTemplate_files/figure-markdown_github/Scatterplot1-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$fixed.acidity
    ## t = 4.996, df = 1597, p-value = 6.496e-07
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.07548957 0.17202667
    ## sample estimates:
    ##       cor 
    ## 0.1240516

The median fixed acidity rises as the quality rises, although there's a spike at 7.

![](projectTemplate_files/figure-markdown_github/Scatterplot2-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$volatile.acidity
    ## t = -16.954, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.4313210 -0.3482032
    ## sample estimates:
    ##        cor 
    ## -0.3905578

The median volatile acidity drops as the quality rises. The range also decreases as the quality increases.

![](projectTemplate_files/figure-markdown_github/Scatterplot3-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$citric.acid
    ## t = 9.2875, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.1793415 0.2723711
    ## sample estimates:
    ##       cor 
    ## 0.2263725

The median citric acid level increases as quality increases. Although the level of citric acid was small in the wines, it seems to have been enough to make a difference in the taste of the wines.

![](projectTemplate_files/figure-markdown_github/Scatterplot4-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$residual.sugar
    ## t = 0.5488, df = 1597, p-value = 0.5832
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.03531327  0.06271056
    ## sample estimates:
    ##        cor 
    ## 0.01373164

The median residual sugar level stays pretty consistent as quality rises.

![](projectTemplate_files/figure-markdown_github/Scatterplot5-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$chlorides
    ## t = -5.1948, df = 1597, p-value = 2.313e-07
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.17681041 -0.08039344
    ## sample estimates:
    ##        cor 
    ## -0.1289066

The median chloride level stays pretty consistent as quality rises.

We can see the lack of a correlation especially for residual sugar and chlorides as the plots have a horizontal pattern and the medians stay level. As I had stated before, this may be due to the fact that the levels are so low they are unnoticeable in the wines.

![](projectTemplate_files/figure-markdown_github/Scatterplot6-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$free.sulfur.dioxide
    ## t = -2.0269, df = 1597, p-value = 0.04283
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.099430290 -0.001638987
    ## sample estimates:
    ##         cor 
    ## -0.05065606

It's interesting to see a rise and then a drop in median sulfur dioxide levels as quality increases. The range also increases and then decreases as quality increases.

![](projectTemplate_files/figure-markdown_github/Scatterplot7-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$total.sulfur.dioxide
    ## t = -7.5271, df = 1597, p-value = 8.622e-14
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.2320162 -0.1373252
    ## sample estimates:
    ##        cor 
    ## -0.1851003

Once again for total sulfur dioxide, we also see a rise and then a drop in the median as the quality increases. From these two graphs we can see that sulfur dioxide is not correlated to the quality of the red wine. Free sulfur dioxide has a Pearson's R of -0.5 to quality and total sulfur dioxide has a Person's R of -0.19 to quality.

![](projectTemplate_files/figure-markdown_github/Scatterplot9-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$pH
    ## t = -2.3109, df = 1597, p-value = 0.02096
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.106451268 -0.008734972
    ## sample estimates:
    ##         cor 
    ## -0.05773139

There's a slight decline in median pH levels as quality increases, while the range is pretty consistent across all scores.

![](projectTemplate_files/figure-markdown_github/Scatterplot11-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$quality and wine$alcohol
    ## t = 21.639, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.4373540 0.5132081
    ## sample estimates:
    ##       cor 
    ## 0.4761663

Median alcohol levels increase as quality increases. Alcohol also has the strongest correlation to quality.

Next I want to explore the relationships between other variables.

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot0-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$density and wine$alcohol
    ## t = -22.838, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.5322547 -0.4583061
    ## sample estimates:
    ##        cor 
    ## -0.4961798

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot1-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$density and wine$fixed.acidity
    ## t = 35.877, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.6399847 0.6943302
    ## sample estimates:
    ##       cor 
    ## 0.6680473

I was surprised to see that density was so closely related to both alcohol and fixed acidity.

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot2-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$citric.acid and wine$fixed.acidity
    ## t = 36.234, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.6438839 0.6977493
    ## sample estimates:
    ##       cor 
    ## 0.6717034

Here we can see the strong relationship between fixed acidity and citric acid.

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot3-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$pH and wine$fixed.acidity
    ## t = -37.366, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.7082857 -0.6559174
    ## sample estimates:
    ##        cor 
    ## -0.6829782

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot4-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$pH and wine$citric.acid
    ## t = -25.767, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  -0.5756337 -0.5063336
    ## sample estimates:
    ##        cor 
    ## -0.5419041

pH has a stronger correlation to fixed acidity than it does to citric acid.

![](projectTemplate_files/figure-markdown_github/Other_Scatterplot6-1.png)

    ## 
    ##  Pearson's product-moment correlation
    ## 
    ## data:  wine$free.sulfur.dioxide and wine$total.sulfur.dioxide
    ## t = 35.84, df = 1597, p-value < 2.2e-16
    ## alternative hypothesis: true correlation is not equal to 0
    ## 95 percent confidence interval:
    ##  0.6395786 0.6939740
    ## sample estimates:
    ##       cor 
    ## 0.6676665

Here we can see a strong relationship between free sulfur dioxide and total sulfur dioxide.

Bivariate Analysis
==================

### Talk about some of the relationships you observed in this part of the investigation. How did the feature(s) of interest vary with other features in the dataset?

Percent alcohol correlated the strongest with quality with a correlation of 0.48. As the percent alcohol increased, the quality of the wine increased as well.

Volatile acidity had the second strongest correlation with quality, with a correlation of -0.39. This was in line with my initial intuition because too much volatile acidity in wine can lead to a vinegar taste. Thus we see from the data that the lower the volatile acidity, the higher the quality of the wine.

I had originally thought that total sulfur dioxide would have a stronger correlation with the quality of wine. However since only 35% of wines had sulfur concentrations over 50ppm (level in which the sulfur dioxide becomes evident in the taste of the wine), it makes sense that this variable did not make as big of an impact in the overall ratings of the wine as it was undetectable in 65% of the wines.

I was surprised to see that residual sugar and chlorides had such low correlation with the quality of the wine. It seems as if for most of the wines the levels of sugar and chlorides were so low that they were undetectable in the taste of the wine.

### Did you observe any interesting relationships between the other features (not the main feature(s) of interest)?

There were many strong correlations between the various acid variables along with pH levels, which was not too surprising given that they all have to do with acid. However what did surprise me was how strong of a relationship density had with both alcohol and fixed acidity.

### What was the strongest relationship you found?

The strongest relationship I found for quality was the percent alcohol in the wine with a correlation of 0.48.

The strongest relationship I found between any two variables was between pH and fixed acidity with a correlation of -0.68.

Multivariate Plots Section
==========================

![](projectTemplate_files/figure-markdown_github/Multivariate_Plots1-1.png)

Wines with lower levels of volatile acidity and higher levels of citric acid tend to be of better quality.

![](projectTemplate_files/figure-markdown_github/Multivariate_Plots2-1.png)

Wines with higher levels of sulfate and lower levels of volatile acidity tend to be of better quality.

![](projectTemplate_files/figure-markdown_github/Multivariate_Plots3-1.png)

Wines that are less dense with higher alcohol content tend to be of better quality.

![](projectTemplate_files/figure-markdown_github/Multivariate_Plots4-1.png)

Wines with higher alcohol content and higher levels of sulphates tend to be of better quality.

Multivariate Analysis
=====================

### Talk about some of the relationships you observed in this part of the investigation. Were there features that strengthened each other in terms of looking at your feature(s) of interest?

As the amount of acetic acid decreases, the amount of citric acid increases. Those wines with lower levels of acetic acid and higher levels of citric acid tend to be rated better quality.

The amount of acetic acid also shows some relationship with the amount of sulphates in the wine. Those wines with more acetic acid tend to have less sulphate, which correlates to a lower quality wine.

### Were there any interesting or surprising interactions between features?

As mentioned before, what surprised me was the correlation between alcohol and density. We can see from the Quality x Density x Alcohol plot that those wines that are less dense tend to be of higher alcohol content and better quality.

------------------------------------------------------------------------

Final Plots and Summary
=======================

### Plot One

![](projectTemplate_files/figure-markdown_github/Plot_One-1.png)

### Description One

The distributions for fixed acidity and citric acid show similar movement as the quality of the wine gets better. Both distributions became more normal as the quality increased. This relationship led me to believe that these two attributes were correlated. They have a Pearson's R of 0.67, which is one of the strongest relationships in the dataset.

### Plot Two

![](projectTemplate_files/figure-markdown_github/Plot_Two-1.png)

### Description Two

Alcohol showed the strongest correlation to the quality of wine with a Pearon's R of 0.48. With this graph we can see that the median % alcohol content increases as the quality of the wine increases.

### Plot Three

![](projectTemplate_files/figure-markdown_github/Plot_Three-1.png)

### Description Three

The relationship between density and alcohol % surprised me so I wanted to investigate further how these attributes affected the quality of the wine. It seems as if wines that are less dense with higher alcohol content tend to be of better quality.

------------------------------------------------------------------------

Reflection
==========

This red wine dataset contains 1599 observations with 11 input variables and 1 output variable. I first analyzed the data by looking at the distribution of the various attributes across the red wines. I then dove deeper to understand how the attributes affected each other as well as the quality of the wine.

After analyzing the data, I have concluded the following:

-   Most wines received a 5 or 6 rating
-   The correlation of volatile acidity, citric acid, and sulphate levels to quality are in line with my initial intuition. However it seems I was incorrect to think that residual sugar, chloride, and sulfur dioxide would affect the quality of the wine as these attributes had very low correlation to quality.
-   % alcohol has the strongest correlation with the quality of the red wine with a Pearson's R of 0.48. As the % alcohol increases, the quality of the wine increases as well.
-   % Fixed acidity and pH show the strongest correlation in the dataset with a Pearon's R of -0.68.
-   Fixed acidity has a stronger correlation to citric acid than it does to volatile acidity.
-   Residual sugar, free sulfur dioxide, and pH have the weakest correlation with red wine quality.

Because there were so few wines that were rated either a 3 or an 8 and too many wines rated a 5 or a 6, I feel as if the sample sizes for 3s and 8s were not large enough to test correlation for the high-quality and low-quality wines. This made it difficult to see a strong relationship between the the attributes and quality.

Although there is some correlation between the various attributes and the quality of the red wine, the relationships are not as strong as I originally believed them to be. This may be due to the fact that the quality rating was subjective to each wine expert. What one expert prefers in a wine may not be similar to what another expert believes to be high-quality wine. Thus in order to better test which attributes influence the nose and taste of the wine, we would need a more objective method of testing the quality. It would be interesting to test how the attributes are affected depending on the type of wine (e.g. cabernet sauvignon vs merlot).
