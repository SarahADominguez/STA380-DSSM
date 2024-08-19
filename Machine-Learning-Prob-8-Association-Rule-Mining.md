    ## Warning: package 'tidyverse' was built under R version 4.3.3

    ## Warning: package 'ggplot2' was built under R version 4.3.3

    ## Warning: package 'tidyr' was built under R version 4.3.3

    ## Warning: package 'purrr' was built under R version 4.3.3

    ## Warning: package 'dplyr' was built under R version 4.3.3

    ## Warning: package 'stringr' was built under R version 4.3.3

    ## Warning: package 'forcats' was built under R version 4.3.3

    ## Warning: package 'lubridate' was built under R version 4.3.3

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

    ## Warning: package 'igraph' was built under R version 4.3.3

    ## 
    ## Attaching package: 'igraph'
    ## 
    ## The following objects are masked from 'package:lubridate':
    ## 
    ##     %--%, union
    ## 
    ## The following objects are masked from 'package:dplyr':
    ## 
    ##     as_data_frame, groups, union
    ## 
    ## The following objects are masked from 'package:purrr':
    ## 
    ##     compose, simplify
    ## 
    ## The following object is masked from 'package:tidyr':
    ## 
    ##     crossing
    ## 
    ## The following object is masked from 'package:tibble':
    ## 
    ##     as_data_frame
    ## 
    ## The following objects are masked from 'package:stats':
    ## 
    ##     decompose, spectrum
    ## 
    ## The following object is masked from 'package:base':
    ## 
    ##     union

    ## Warning: package 'arules' was built under R version 4.3.3

    ## Loading required package: Matrix
    ## 
    ## Attaching package: 'Matrix'
    ## 
    ## The following objects are masked from 'package:tidyr':
    ## 
    ##     expand, pack, unpack
    ## 
    ## 
    ## Attaching package: 'arules'
    ## 
    ## The following object is masked from 'package:dplyr':
    ## 
    ##     recode
    ## 
    ## The following objects are masked from 'package:base':
    ## 
    ##     abbreviate, write

    ## Warning: package 'arulesViz' was built under R version 4.3.3

# Top 20 items across all baskets

    ## 
    ##            whole milk      other vegetables            rolls/buns 
    ##                  2513                  1903                  1809 
    ##                  soda                yogurt         bottled water 
    ##                  1715                  1372                  1087 
    ##       root vegetables        tropical fruit         shopping bags 
    ##                  1072                  1032                   969 
    ##               sausage                pastry          citrus fruit 
    ##                   924                   875                   814 
    ##          bottled beer            newspapers           canned beer 
    ##                   792                   785                   764 
    ##             pip fruit fruit/vegetable juice    whipped/sour cream 
    ##                   744                   711                   705 
    ##           brown bread         domestic eggs 
    ##                   638                   624

![](Machine-Learning-Prob-8-Association-Rule-Mining_files/figure-markdown_github/loading%20file-1.png)
#Understand data

``` r
summary(grocery_transactions)
print(grocery_transactions)
inspect(grocery_transactions[1:5])
```

#First set of rules

support: 0.001 confidence: 0.01 Max length: 4 Lift: No lift yet

``` r
# Step 6: Association Rule Mining
min_support <- 0.001
min_confidence <- 0.01
min_lift <- 4

grocery_rules <- apriori(grocery_transactions, 
                 parameter = list(supp = min_support, conf = min_confidence, maxlen= 4 ))
```

    ## Apriori
    ## 
    ## Parameter specification:
    ##  confidence minval smax arem  aval originalSupport maxtime support minlen
    ##        0.01    0.1    1 none FALSE            TRUE       5   0.001      1
    ##  maxlen target  ext
    ##       4  rules TRUE
    ## 
    ## Algorithmic control:
    ##  filter tree heap memopt load sort verbose
    ##     0.1 TRUE TRUE  FALSE TRUE    2    TRUE
    ## 
    ## Absolute minimum support count: 9 
    ## 
    ## set item appearances ...[0 item(s)] done [0.00s].
    ## set transactions ...[169 item(s), 9835 transaction(s)] done [0.00s].
    ## sorting and recoding items ... [157 item(s)] done [0.00s].
    ## creating transaction tree ... done [0.00s].
    ## checking subsets of size 1 2 3 4

    ## Warning in apriori(grocery_transactions, parameter = list(supp = min_support, :
    ## Mining stopped (maxlen reached). Only patterns up to a length of 4 returned!

    ##  done [0.01s].
    ## writing ... [38947 rule(s)] done [0.00s].
    ## creating S4 object  ... done [0.01s].

``` r
#grocery_rules <- subset(grocery_rules, lift > min_lift)
```

#Inspect first set of rules

(Too big, 39,000 rows, but good for graph)

``` r
# The rules generated
inspect(grocery_rules) # 39,000 rules, with support .001, conf .01, too many, but good for graphs
```

#Graphs for first set of rules

These graphs are for visualizing as much of the data as possible, and
then based of these graphs we pick a subset of the data to look at

    ## Warning: Unknown control parameters: xlim

    ## Available control parameters (with default values):
    ## main  =  Scatter plot for 38947 rules
    ## colors    =  c("#EE0000FF", "#EEEEEEFF")
    ## jitter    =  NA
    ## engine    =  ggplot2
    ## verbose   =  FALSE

    ## To reduce overplotting, jitter is added! Use jitter = 0 to prevent jitter.

![](Machine-Learning-Prob-8-Association-Rule-Mining_files/figure-markdown_github/graphs-1.png)

    ## Warning: Unknown control parameters: xlim

    ## Available control parameters (with default values):
    ## main  =  Scatter plot for 38947 rules
    ## colors    =  c("#EE0000FF", "#EEEEEEFF")
    ## jitter    =  NA
    ## engine    =  ggplot2
    ## verbose   =  FALSE

    ## To reduce overplotting, jitter is added! Use jitter = 0 to prevent jitter.

![](Machine-Learning-Prob-8-Association-Rule-Mining_files/figure-markdown_github/graphs-2.png)
#Look at subsets based off graphs above

``` r
inspect(subset(grocery_rules, support > 0.05)) # 34 rules

inspect(subset(grocery_rules, support > 0.01)) #610 rules

inspect(subset(grocery_rules, confidence > 0.75)) #458
```

## Most relevant subset:

``` r
inspect(subset(grocery_rules, lift > 10)) #78 rules
```

    ##      lhs                         rhs                         support confidence    coverage     lift count
    ## [1]  {softener}               => {detergent}             0.001118454 0.20370370 0.005490595 10.60014    11
    ## [2]  {detergent}              => {softener}              0.001118454 0.05820106 0.019217082 10.60014    11
    ## [3]  {liquor}                 => {red/blush wine}        0.002135231 0.19266055 0.011082867 10.02548    21
    ## [4]  {red/blush wine}         => {liquor}                0.002135231 0.11111111 0.019217082 10.02548    21
    ## [5]  {Instant food products}  => {hamburger meat}        0.003050330 0.37974684 0.008032537 11.42144    30
    ## [6]  {hamburger meat}         => {Instant food products} 0.003050330 0.09174312 0.033248602 11.42144    30
    ## [7]  {mayonnaise}             => {mustard}               0.001423488 0.15555556 0.009150991 12.96516    14
    ## [8]  {mustard}                => {mayonnaise}            0.001423488 0.11864407 0.011997966 12.96516    14
    ## [9]  {liquor,                                                                                             
    ##       red/blush wine}         => {bottled beer}          0.001931876 0.90476190 0.002135231 11.23527    19
    ## [10] {bottled beer,                                                                                       
    ##       liquor}                 => {red/blush wine}        0.001931876 0.41304348 0.004677173 21.49356    19
    ## [11] {bottled beer,                                                                                       
    ##       red/blush wine}         => {liquor}                0.001931876 0.39583333 0.004880529 35.71579    19
    ## [12] {popcorn,                                                                                            
    ##       soda}                   => {salty snack}           0.001220132 0.63157895 0.001931876 16.69779    12
    ## [13] {salty snack,                                                                                        
    ##       soda}                   => {popcorn}               0.001220132 0.13043478 0.009354347 18.06797    12
    ## [14] {Instant food products,                                                                              
    ##       soda}                   => {hamburger meat}        0.001220132 0.63157895 0.001931876 18.99565    12
    ## [15] {hamburger meat,                                                                                     
    ##       soda}                   => {Instant food products} 0.001220132 0.21052632 0.005795628 26.20919    12
    ## [16] {Instant food products,                                                                              
    ##       rolls/buns}             => {hamburger meat}        0.001016777 0.43478261 0.002338587 13.07672    10
    ## [17] {hamburger meat,                                                                                     
    ##       rolls/buns}             => {Instant food products} 0.001016777 0.11764706 0.008642603 14.64631    10
    ## [18] {Instant food products,                                                                              
    ##       whole milk}             => {hamburger meat}        0.001525165 0.50000000 0.003050330 15.03823    15
    ## [19] {hamburger meat,                                                                                     
    ##       whole milk}             => {Instant food products} 0.001525165 0.10344828 0.014743264 12.87866    15
    ## [20] {sugar,                                                                                              
    ##       whole milk}             => {rice}                  0.001220132 0.08108108 0.015048297 10.63243    12
    ## [21] {butter,                                                                                             
    ##       root vegetables}        => {rice}                  0.001016777 0.07874016 0.012913066 10.32546    10
    ## [22] {fruit/vegetable juice,                                                                              
    ##       root vegetables}        => {rice}                  0.001118454 0.09322034 0.011997966 12.22429    11
    ## [23] {ham,                                                                                                
    ##       processed cheese}       => {white bread}           0.001931876 0.63333333 0.003050330 15.04549    19
    ## [24] {processed cheese,                                                                                   
    ##       white bread}            => {ham}                   0.001931876 0.46341463 0.004168785 17.80345    19
    ## [25] {ham,                                                                                                
    ##       white bread}            => {processed cheese}      0.001931876 0.38000000 0.005083884 22.92822    19
    ## [26] {fruit/vegetable juice,                                                                              
    ##       processed cheese}       => {ham}                   0.001118454 0.37931034 0.002948653 14.57233    11
    ## [27] {fruit/vegetable juice,                                                                              
    ##       ham}                    => {processed cheese}      0.001118454 0.28947368 0.003863752 17.46610    11
    ## [28] {ham,                                                                                                
    ##       soda}                   => {processed cheese}      0.001016777 0.20408163 0.004982206 12.31376    10
    ## [29] {domestic eggs,                                                                                      
    ##       processed cheese}       => {white bread}           0.001118454 0.52380952 0.002135231 12.44364    11
    ## [30] {domestic eggs,                                                                                      
    ##       white bread}            => {processed cheese}      0.001118454 0.19298246 0.005795628 11.64406    11
    ## [31] {pip fruit,                                                                                          
    ##       processed cheese}       => {white bread}           0.001016777 0.43478261 0.002338587 10.32871    10
    ## [32] {tropical fruit,                                                                                     
    ##       white bread}            => {processed cheese}      0.001525165 0.17441860 0.008744281 10.52397    15
    ## [33] {soda,                                                                                               
    ##       white bread}            => {processed cheese}      0.001728521 0.16831683 0.010269446 10.15580    17
    ## [34] {rolls/buns,                                                                                         
    ##       white bread}            => {processed cheese}      0.001321810 0.20312500 0.006507372 12.25604    13
    ## [35] {baking powder,                                                                                      
    ##       flour}                  => {sugar}                 0.001016777 0.55555556 0.001830198 16.40807    10
    ## [36] {baking powder,                                                                                      
    ##       sugar}                  => {flour}                 0.001016777 0.31250000 0.003253686 17.97332    10
    ## [37] {flour,                                                                                              
    ##       sugar}                  => {baking powder}         0.001016777 0.20408163 0.004982206 11.53530    10
    ## [38] {baking powder,                                                                                      
    ##       margarine}              => {sugar}                 0.001118454 0.36666667 0.003050330 10.82933    11
    ## [39] {margarine,                                                                                          
    ##       sugar}                  => {baking powder}         0.001118454 0.20370370 0.005490595 11.51394    11
    ## [40] {domestic eggs,                                                                                      
    ##       sugar}                  => {baking powder}         0.001016777 0.20408163 0.004982206 11.53530    10
    ## [41] {sugar,                                                                                              
    ##       whipped/sour cream}     => {baking powder}         0.001321810 0.27083333 0.004880529 15.30831    13
    ## [42] {curd,                                                                                               
    ##       flour}                  => {sugar}                 0.001118454 0.35483871 0.003152008 10.48000    11
    ## [43] {curd,                                                                                               
    ##       sugar}                  => {flour}                 0.001118454 0.32352941 0.003457041 18.60767    11
    ## [44] {flour,                                                                                              
    ##       margarine}              => {sugar}                 0.001626843 0.43243243 0.003762074 12.77169    16
    ## [45] {margarine,                                                                                          
    ##       sugar}                  => {flour}                 0.001626843 0.29629630 0.005490595 17.04137    16
    ## [46] {sugar,                                                                                              
    ##       whipped/sour cream}     => {flour}                 0.001016777 0.20833333 0.004880529 11.98221    10
    ## [47] {citrus fruit,                                                                                       
    ##       sugar}                  => {flour}                 0.001016777 0.21276596 0.004778851 12.23715    10
    ## [48] {root vegetables,                                                                                    
    ##       sugar}                  => {flour}                 0.001423488 0.22222222 0.006405694 12.78103    14
    ## [49] {flour,                                                                                              
    ##       soda}                   => {sugar}                 0.001118454 0.39285714 0.002846975 11.60285    11
    ## [50] {sugar,                                                                                              
    ##       yogurt}                 => {flour}                 0.001321810 0.19117647 0.006914082 10.99544    13
    ## [51] {sugar,                                                                                              
    ##       whole milk}             => {flour}                 0.002846975 0.18918919 0.015048297 10.88114    28
    ## [52] {dessert,                                                                                            
    ##       pip fruit}              => {butter milk}           0.001423488 0.28571429 0.004982206 10.21818    14
    ## [53] {sliced cheese,                                                                                      
    ##       whipped/sour cream}     => {ham}                   0.001016777 0.26315789 0.003863752 10.10999    10
    ## [54] {ham,                                                                                                
    ##       pip fruit}              => {sliced cheese}         0.001016777 0.25641026 0.003965430 10.46388    10
    ## [55] {fruit/vegetable juice,                                                                              
    ##       ham}                    => {white bread}           0.001626843 0.42105263 0.003863752 10.00254    16
    ## [56] {other vegetables,                                                                                   
    ##       root vegetables,                                                                                    
    ##       tropical fruit}         => {turkey}                0.001220132 0.09917355 0.012302999 12.19215    12
    ## [57] {butter,                                                                                             
    ##       root vegetables,                                                                                    
    ##       whole milk}             => {rice}                  0.001016777 0.12345679 0.008235892 16.18930    10
    ## [58] {other vegetables,                                                                                   
    ##       root vegetables,                                                                                    
    ##       yogurt}                 => {rice}                  0.001423488 0.11023622 0.012913066 14.45564    14
    ## [59] {root vegetables,                                                                                    
    ##       whole milk,                                                                                         
    ##       yogurt}                 => {rice}                  0.001423488 0.09790210 0.014539908 12.83823    14
    ## [60] {other vegetables,                                                                                   
    ##       root vegetables,                                                                                    
    ##       whole milk}             => {rice}                  0.001830198 0.07894737 0.023182511 10.35263    18
    ## [61] {curd,                                                                                               
    ##       root vegetables,                                                                                    
    ##       whole milk}             => {herbs}                 0.001220132 0.19672131 0.006202339 12.09221    12
    ## [62] {bottled water,                                                                                      
    ##       citrus fruit,                                                                                       
    ##       whole milk}             => {herbs}                 0.001016777 0.17241379 0.005897306 10.59806    10
    ## [63] {other vegetables,                                                                                   
    ##       root vegetables,                                                                                    
    ##       shopping bags}          => {herbs}                 0.001118454 0.16923077 0.006609049 10.40240    11
    ## [64] {soda,                                                                                               
    ##       white bread,                                                                                        
    ##       whole milk}             => {processed cheese}      0.001016777 0.25000000 0.004067107 15.08436    10
    ## [65] {flour,                                                                                              
    ##       root vegetables,                                                                                    
    ##       whole milk}             => {sugar}                 0.001016777 0.34482759 0.002948653 10.18432    10
    ## [66] {root vegetables,                                                                                    
    ##       sugar,                                                                                              
    ##       whole milk}             => {flour}                 0.001016777 0.29411765 0.003457041 16.91606    10
    ## [67] {other vegetables,                                                                                   
    ##       sugar,                                                                                              
    ##       whole milk}             => {flour}                 0.001220132 0.19354839 0.006304016 11.13186    12
    ## [68] {margarine,                                                                                          
    ##       other vegetables,                                                                                   
    ##       yogurt}                 => {flour}                 0.001016777 0.17857143 0.005693950 10.27047    10
    ## [69] {root vegetables,                                                                                    
    ##       whipped/sour cream,                                                                                 
    ##       whole milk}             => {flour}                 0.001728521 0.18279570 0.009456024 10.51343    17
    ## [70] {domestic eggs,                                                                                      
    ##       other vegetables,                                                                                   
    ##       yogurt}                 => {soft cheese}           0.001118454 0.19298246 0.005795628 11.29751    11
    ## [71] {citrus fruit,                                                                                       
    ##       fruit/vegetable juice,                                                                              
    ##       tropical fruit}         => {grapes}                0.001118454 0.28205128 0.003965430 12.60897    11
    ## [72] {hard cheese,                                                                                        
    ##       whipped/sour cream,                                                                                 
    ##       yogurt}                 => {butter}                0.001016777 0.58823529 0.001728521 10.61522    10
    ## [73] {butter,                                                                                             
    ##       whipped/sour cream,                                                                                 
    ##       yogurt}                 => {hard cheese}           0.001016777 0.26315789 0.003863752 10.73924    10
    ## [74] {chocolate,                                                                                          
    ##       rolls/buns,                                                                                         
    ##       soda}                   => {candy}                 0.001220132 0.30000000 0.004067107 10.03571    12
    ## [75] {pip fruit,                                                                                          
    ##       sausage,                                                                                            
    ##       yogurt}                 => {sliced cheese}         0.001220132 0.30769231 0.003965430 12.55665    12
    ## [76] {coffee,                                                                                             
    ##       other vegetables,                                                                                   
    ##       yogurt}                 => {oil}                   0.001016777 0.28571429 0.003558719 10.18116    10
    ## [77] {citrus fruit,                                                                                       
    ##       fruit/vegetable juice,                                                                              
    ##       root vegetables}        => {oil}                   0.001016777 0.29411765 0.003457041 10.48061    10
    ## [78] {hamburger meat,                                                                                     
    ##       whipped/sour cream,                                                                                 
    ##       yogurt}                 => {butter}                0.001016777 0.62500000 0.001626843 11.27867    10

##Support 0.05% and above

Things to understand:

A big difference between this data set and the playlist data set is how
frequently items appear. In this data set, the support at 0.05% only
draws 34 rules (appears in 5% of baskets or more). Of these rules, 28 of
them are just an item by itself! This gives us insight into the grocery
shopping of individuals, and suggests people have very different grocery
shopping lists. Besides these 28 items, there is a lot of diversity in
what people buy.

These 28 items included: canned beef, coffee, beef, napkins, pork,
newspapers, domestic eggs, butter, fruit/vegetable juice, pastry,
bottled water, soda, yogurt, rolls/buns, other vegetables, milk, etc.

These are very common food items, so it makes sense that they appear
constantly throughout the data. Milk has the highest support of 25%,
which makes sense as our graph earlier had milk as the most common food
item.

The other rules included:

yogurt –\> whole milk

other vegetables –\> whole milk

rolls/buns –\> whole milk

and the opposites of these as well! Notice that these are the top 3
items that appeared across all baskets, and their lifts stay between 1.2
to 1.5. This suggests that these associations are not at all powerful,
and their appearence here is more than likely because they appear
throughout all baskets, not because they have associations with each
other.

The difference between the the grocery data and playlist data is why in
the first graph above, I choose a support of 0.001 and confidence of
0.01. I wanted to capture many rules (graph captured 39,000 rules!), so
I could find interesting patterns and then look at the subsets.

##Confidence 75% and above

when looking at confidence of 75% and above, we find there are 458
rules. This is interesting, as it represents the probability of the
right hand side showing up based on what is in the left hand side.
However, we may run into an issue. If something is very common like
milk, there is a chance that most products will have a high confidence
when milk is on the right side! This doesn’t necessarily indicate a
strong association!

Therefore, when looking for rules it is better to just look at the lift
(which tells us how much *more likely* an item is to be bought if it
appears with another, and accounts for frequency of the right hand side)

However, some of the 458 rules with conf above 75% include:

Citrus fruit, fruit/vegetable juice, grapes –\> tropical fruit (lift of
8!)

frozen meals, tropical fruit, yogurt –\> whole milk (lift of 3)

When looking through the 75% confidence rules, my hypothesis came out
true! As I scrolled down, the majority of the right hand side was milk!
and the lift was around 3 on average for those which contained milk,
suggesting that these rules weren’t very meaningful. I included above
one rule which had a lift of 8 (suggesting it is genuinely strong!) and
one rule with on the right hand side milk and a lift of 3. Notice that
for the first rule, the foods make sense to be bought together. Clearly,
the person is buying things to make something fruity! However, for the
milk rule, notice that frozen meals, tropical fruit, yogurt, and then
milk, don’t really create an intresting meaningful rule. Rather, it
seems to be a conglomerate of random things.

##Lift of 10+

When looking at a lift above 10 (i.e., if item on left hand side
appears, the item on the right hand side is 10 times as likely to
appear), we find 78 rules. I decided on the number ten based on insights
from the graph, and when we look at these 78 rules together, we find
foods/items that tend to go together! For example:

softener –\> detergent (lift: 10)

popcorn, soda –\> salty snack (16)

ham, bread –\> cheese (lift: 22)

bottled beer, red/blush wine –\> liquor (35)

and much more!

These rules make *way* more sense than just looking at the confidence.
It has found associations between cleaning products, alcohol, popcorn,
and sandwich purchases that make perfect sense and by intuition are
quite common!

Something else I noticed is that quite a few of the rules are 2-3 items
together and the inclusion of a 4th. A lot of times this 4th item
doesn’t have as close of an association with the other items, BUT it is
considered a necessity, such:

Butter, root vegetables, and whole milk –\> rice

I personally do not necessarily see a connection with these foods,
however they are considered essential household foods. Perhaps, when we
get rules like these, it suggests that when people buy a lot of food,
they tend to buy many necesities, etc.

#First Igraph code (Turned out pretty ugly)

``` r
# Convert grocery_rules to Graph and Export for Gephi
grocery_graph <- associations2igraph(grocery_rules, associationsAsNodes = FALSE)
igraph::write_graph(grocery_graph, file='grocery_rules.graphml', format = "graphml")
```

<img src="../First_Igraph_(ML prob 8).png" width="100%" />

Above, we see an igraph based on the first settings, which were very
broad. Turned out very ugly, not much can be done with it.

#Second Rules based on previous graphs

support: 0.001 confidence: 0.01 max length: 4

**lift:** 6

``` r
# Step 6: Association Rule Mining
f_grocery_rules <- apriori(grocery_transactions, 
                 parameter = list(supp = 0.001, conf = .01, maxlen=4))
```

    ## Apriori
    ## 
    ## Parameter specification:
    ##  confidence minval smax arem  aval originalSupport maxtime support minlen
    ##        0.01    0.1    1 none FALSE            TRUE       5   0.001      1
    ##  maxlen target  ext
    ##       4  rules TRUE
    ## 
    ## Algorithmic control:
    ##  filter tree heap memopt load sort verbose
    ##     0.1 TRUE TRUE  FALSE TRUE    2    TRUE
    ## 
    ## Absolute minimum support count: 9 
    ## 
    ## set item appearances ...[0 item(s)] done [0.00s].
    ## set transactions ...[169 item(s), 9835 transaction(s)] done [0.00s].
    ## sorting and recoding items ... [157 item(s)] done [0.00s].
    ## creating transaction tree ... done [0.00s].
    ## checking subsets of size 1 2 3 4

    ## Warning in apriori(grocery_transactions, parameter = list(supp = 0.001, :
    ## Mining stopped (maxlen reached). Only patterns up to a length of 4 returned!

    ##  done [0.00s].
    ## writing ... [38947 rule(s)] done [0.00s].
    ## creating S4 object  ... done [0.01s].

``` r
f_grocery_rules <- subset(f_grocery_rules, lift > 6)
```

#Second rules graphs

    ## Warning: Unknown control parameters: xlim

    ## Available control parameters (with default values):
    ## main  =  Scatter plot for 721 rules
    ## colors    =  c("#EE0000FF", "#EEEEEEFF")
    ## jitter    =  NA
    ## engine    =  ggplot2
    ## verbose   =  FALSE

    ## To reduce overplotting, jitter is added! Use jitter = 0 to prevent jitter.

![](Machine-Learning-Prob-8-Association-Rule-Mining_files/figure-markdown_github/graphs2-1.png)

    ## Warning: Unknown control parameters: xlim

    ## Available control parameters (with default values):
    ## main  =  Scatter plot for 721 rules
    ## colors    =  c("#EE0000FF", "#EEEEEEFF")
    ## jitter    =  NA
    ## engine    =  ggplot2
    ## verbose   =  FALSE

    ## To reduce overplotting, jitter is added! Use jitter = 0 to prevent jitter.

![](Machine-Learning-Prob-8-Association-Rule-Mining_files/figure-markdown_github/graphs2-2.png)

Based off of previous subsets and the analysis, these above are the
graphs of our final rules for lift, support, and confidence.

#Second and Final Igraph

``` r
# Step 7: Convert to Graph and Export for Gephi
f_grocery_graph <- associations2igraph(f_grocery_rules, associationsAsNodes = FALSE)
igraph::write_graph(f_grocery_graph, file='f_grocery_rules.graphml', format = "graphml")
```

Here is the network graph generated using Gephi:

<img src="../Prob8_Gephi_Graph_Final.png" width="100%" />

By using the Gephi tutorial within the professor’s github, we get this
result. Gephi discovered 6 communities within the data! Gephi also got
their share of all the data:

Purple: 27% Green: 25% Blue: 25% Orange: 12.64% Dark Green: 6.9% Pink:
2.3%

The graph is an association network, so in short terms it represents
items that are bought together. They may indicate common ingredients,
styles of food, necessities, etc. Something which worried me at first,
was how small the whole milk node is. it is in the purple group, below
the butter. I was concerned, as it was the most frequent item but was
small in the results. However, I believe this is due to what was
discussed earlier: frequency **does not ** necessarily indicate strong
association.

**Individual Nodes**

Look at the large nodes, like root vegetables, butter, white break,
tropical fruit, etc. These are nodes that have lots of strong
associations for many other products. As the nodes get smaller and
further away, these have less associations and the associations are
weaker.

Root vegetables for example, are bought often with oil, citrus fruit,
fruit/vegetable juice, herbs, rice, other vegetables, etc. This can be
determined by looking at the arrows and which directions they point in
(although it is a little tough to do)

Another node or community we can look at, is sugar. Based off of the
arrows, we can determine that flour, baking powder, margarine, domestic
eggs, salt, and roll products have strong associations with sugar and
with each other (whenever their arrows point at each other). However,
something like roll products and salt, although they are in the same
community, don’t have an association.

**Communities**

We have already covered two communities, green (root vegetables) and
dark green (sugar). The items within each group do seem to corespond to
each other, and the identity of these communities makes sense.

The orange community also seems to make sense. Whipped/sour cream,
yogurt, curd, cream cheese, sliced cheese do make a lot of sense
together and are relatable! On the outskirts, we see smaller
associations which do still make sense, just not as much and only with
specific other items. For example, deserts, cereal, meat spread, coffee,
etc. Notice how these only have a couple arrows pointing at them. Coffee
only has one! What this has taught me is that the further away/smaller a
point is from the middle of the group, the less relatable and less often
it is bought with those things

The community which makes the most sense and is especially specific is
pink, which only contains softner and detergent. The lift was 10, and
the confidence was 90%, so them being together and their own category
makes sense

Two communities I found to be broad were the purple and blue
communities. Some things don’t necessarily make sense to be a part of
the same community. For example, in purple, napkins, butter, hamburgers,
and chocolate are all in the same group! In order to understand it
better, you must take a look at where the arrows are going and which
arrow is touching which. If you look closely, napkins and hamburgers do
**NOT** have a lie drawn towards each other, even though they are
particularly large nodes in the same community. Rather, they connect
with nodes within the same community, and have sort of their own subsets
of associations. For example, hamburgers has sauces and instant food
products nearby, with suaces only connected to hamburgers.

You can also find another sub community in purple, cat food and pet care
products.

The blue community also has a lot of sub communities, for example:

Popcorn, salty snacks, soda Bread, processed cheese, ham Bottled beer,
liquor, red/blush wine

My personal favorite, there are connections between soda and liquor!
Could this be jack and coke?

In the future, I would love to dive further and understand why the blue
and purple communities have strange associations. I would also like to
perhaps include even more communities!
