# R-lab-project
This dataset contains 1728 data about car’s criteria. All criteria has been labeled, so we used unsupervised learning method to infer from the data. The data contains categorical values, so we conduct Classification task to acquire knowledge from the data.

The quality of cars is measured by two main groups of criteria: price (PRICE) and technical characteristics (TECH). The price is determined by buying and maintenance price. Technical characteristic are decomposed into safety and comfort, which further depends on number of doors, size of car (measured as number of persons that fit in the car) and size of the luggage boot.

The concept structure of the data described below:
CAR car acceptability
— PRICE overall price
— — buying buying price
— — maint price of the maintenance
— TECH technical characteristics
— — COMFORT comfort
— — — doors number of doors
— — — persons capacity in terms of persons to carry
— — — lug_boot the size of luggage boot
— — safety estimated safety of the car

The step-by-step implementation method described below:

Analyzing attribute of each criteria.

Apply randomized splitting data set into training set and test set.

Apply C50 algorithm on training set.

Using test set to predict classification accuracy.

Infer decision tree from the model.

 the criteria distribution making enough contribution in order to construct decision tree. The safety criteria which is distributed normally and 100% used split decision tree into two, while persons criteria which is positively skewed and 66.31% used became root node.
Our splitting rule which is 75:35 seems performs good enough, but we may still need to tune the splitting rule in range 60:40 to 80:20 if necessary.
