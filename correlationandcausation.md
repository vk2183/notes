# Correlation and Causation
# Correlation:
It is a statistical technique which helps us know the relationship between two variables
- It is a numerical value which lies between -1 to 1
- Lets say A and B are two variables
- It is positive when (directly proportional), A increases when B is increased.
- It is negative when (inversely proportional), A decreases when B is decreased.
- We can say if the two variables are correlated positively or negatively, strongly or weekly by looking at the scatterplots.
### Correlation Matrix:
We can use the corr() function in Python to create a correlation matrix. We also use the round() function to round the output to two decimals
#### Python code for the above is:
```
Corr_Matrix = round(df.corr(),2)
print(Corr_Matrix)
```
### Heat Map:
We use seaborn to visualise the correlation matrix in a better way, refer to this 
[example image](https://www.w3schools.com/datascience/img_stat_heatmap.png)

The closer the correlation coefficient is to 1, the greener the squares get.
The closer the correlation coefficient is to -1, the browner the squares get.
#### Python code for the above is:
```
import matplotlib.pyplot as plt
import seaborn as sns

heatmap_df = df.corr()

axis_corr = sns.heatmap(
heatmap_df,
vmin=-1, vmax=1, center=0,
cmap=sns.diverging_palette(50, 500, n=500),
square=True
)

plt.show()
```
# Causation
When one event causes the creation of another event, its called Causation. also known as the cause and effect relationship.
Eg : Snowfall causes decrease in temperature, vehicles cause pollution

## So what is the difference between correlation and causation?
Even tho two variables are correlated, we cannot say that are causated.
Eg: 
- smoking increases the risks of cancer  - causation
- smoking and alcoholism are correlated but smoking does not cause alcoholism - correlation


