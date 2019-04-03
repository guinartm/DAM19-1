### Assignment: Decision Making

##### Task:    
___
  ● Clients complain that the searches for a destinations sometimes fail. Head of product decided to address
the issue, and ask development team to work on fix.

● The team committed to work out the solution during August. It was agreed that the team’s bonus payout
would depend on effectiveness of the solution.

● The Head of Product ask you to analyze the data and help him to decide whether the team deserve
the bonus?

● Your answer should be documented and submitted to the GitHub so that any changes can be easily
tracked.

##### Useful context:
● Data for Barcelona destination (18452212) is representative so that any conclusions can be extrapolated
for other destinations.

#### AWS Configuration
````
$ aws configure
AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
Default region name [None]: eu-west-1
Default output format [None]: ENTER
````

#### Collect Data from Bdata S3 Buckets


#### Data Analisis

We use R to create a Boxplot of the data for Visual Analysis

````
> library(readxl)
> Data1 <- read_excel("~/Desktop/Data1.xlsx")
> View(Data1)   
````

![boxplot](https://github.com/nicodalessandro11/DAM19/blob/master/Rplot.png)





At first sigth, we can appreciatte that some of the values are significative far from de



Given that Boxplots displays a difference between the months, whe propose to run a confirmatory data analisis trough a statistical hypothesis testing.

For this case 

Null hypothesis H0 = 
Alternative Hipothesis H1 = 

Regarding the assupmtion that the observations from both groups are statistically independent of each other, data are paired and come from the same population, we decided to run a non parametric test to decided 

````
wilcox.test(error~month, mu=0,alt="two.sided", correct=TRUE, paired=FALSE, conf.int=TRUE, data = Data1)
````

#### Conclusion

As we have found estadistical significance after the Mann-Withney test in our data, we decided to reject nule Hipothesys nule and to pay thge Bonus to the team.



La U de Mann-Whitney es una prueba no paramétrica que se emplea para contrastar la hipótesis nula de que dos muestras provienen de la misma población. Al encontrar diferencias estadísticamente significativas, podemos afirmar que las muestras no presentan la misma distribución. En nuestro ejemplo, se encuentran evidencias que la distribución de ambas muestras son diferentes, y que en el mes de septiembre hay una disminución estadisticamente significativa en el número de errores con respecto al mes de agosto, por lo que considero pertinente el pago del bono a los técnicos						
						
						
						
						
						



