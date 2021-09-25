# AMD-20-21
Market-Basket analysis for the course  "Algorithms for massive datasets" of prof. Malchiodi.

This repository stores my contribution to the project "Market-basket analysis", using the IMDb dataset, available here on Kaggle:
[IMDb dataset](https://www.kaggle.com/ashirwadsangwan/imdb-dataset)

The aim of the project is to implement an algorithm that find frequent itemsets, using movies as baskets and actors as items.

I implemented from scratch the A-Priori algorithm and I evaluted with the common metrics of association rules the frequent itemsets found with the implemented algorithm.

For instance this is the output of the algorithm implemented from scratch:
```
Threshold: 196.828
Passes on baskets data number 1
Creating singletons...
Filtering item sets of dimension 1...
Frequent item sets of dimension 1: 89
['nm0369058', 'nm0006369', 'nm0003501', 'nm0001000', 'nm0000465', 'nm0367928', 'nm0004417', 'nm0419653', 'nm0623427', 'nm0006982', 'nm0374974', 'nm0798827', 'nm0035067', 'nm0315553', 'nm0004437', 'nm0004467', 'nm0420092', 'nm0695199', 'nm0222432', 'nm0619779', 'nm0482320', 'nm0893449', 'nm0433884', 'nm0820286', 'nm0004463', 'nm0007123', 'nm0004429', 'nm0534867', 'nm0304262', 'nm0619107', 'nm0004109', 'nm1352627', 'nm0154164', 'nm1066229', 'nm0793813', 'nm0667985', 'nm0149822', 'nm0619309', 'nm0415549', 'nm0023173', 'nm0305182', 'nm0417314', 'nm0046850', 'nm0837797', 'nm0654710', 'nm0747131', 'nm1006879', 'nm0764298', 'nm0739418', 'nm0021728', 'nm0993695', 'nm0648803', 'nm0945427', 'nm0451600', 'nm0347953', 'nm0659250', 'nm7390393', 'nm0103977', 'nm0158101', 'nm0000616', 'nm0261738', 'nm0419685', 'nm0019382', 'nm0706691', 'nm0246703', 'nm0695177', 'nm0613417', 'nm1001108', 'nm2147526', 'nm0764762', 'nm0453520', 'nm1066548', 'nm0007106', 'nm0688093', 'nm0045119', 'nm0595934', 'nm0419707', 'nm3183374', 'nm0004660', 'nm0659173', 'nm0080173', 'nm2366585', 'nm0159159', 'nm0453523', 'nm0352032', 'nm1894124', 'nm0033136', 'nm0474820', 'nm0482285']
Creating item sets of dimension 2...
Candidates item sets of dimension 2: 3916
Passes on baskets data number 2
Counting 2-sized item sets...
--- 696.8339266777039 seconds ---
Filtering item sets of dimension 2...
Frequent item sets of dimension 2: 1
[('nm0623427', 'nm0006982')]
[('nm0623427', 'nm0006982')]
Creating item sets of dimension 3...
Candidates item sets of dimension 3: 0
Passes on baskets data number 3
Counting 3-sized item sets...
--- 0.22745680809020996 seconds ---
Filtering item sets of dimension 3...
Frequent item sets of dimension 3: 0
[]
[]
--- 699.1253480911255 seconds ---
```

I also implemented the same algorithm using PySpark and the RDD data structure. We can check out the result of the two solutions in terms of time required to output the solution and correctness of the algorithms comparing the results of the two.

For bigger dataset we can implement the SON algorithm which is a distributed version of the implemented solutions. It splits the datasets in chunks, process every chunk and perform the union of items support.
