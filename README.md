# Precision-and-Recall

Precision, recall, and F1 values, as well as micro- and macro-averages, can be easily calculated based on the confusion matrix.

Overall accuracy of the sample (microaverage, all_prediction): Sum of elements on the main diagonal of the confusion matrix divided by the sum of all elements of the confusion matrix. The formula is:
a l l _ p r e d i c t i o n = s u m ( d i a g ( c o n f m a r t i x ) ) s u m ( c o n f m a r t i x ) all\_prediction=\frac{sum(diag(confmartix))}{sum(confmartix)}
all_prediction=
sum(confmartix)
sum(diag(confmartix))
​
 

The precision of a class i ii (label_i_prediction): element c o n f m a r t i x ( i , i ) confmartix(i,i)confmartix(i,i) divided by the sum of the ordinate elements subscripted i ii . The formula is:
l a b e l _ i _ p r e d i c t i o n = c o n f m a r t i x ( i , i ) ∑ j c o n f m a r t i x ( j , i ) label\_i\_prediction=\frac{confmartix(i,i)}{\sum_j{confmartix(j,i)}}
label_i_prediction=
∑
j
​
 confmartix(j,i)
confmartix(i,i)
​
 

The recall of a class of i ii (label_i_recall): the element c o n f m a r t i x ( i , i ) confmartix(i,i)confmartix(i,i) divided by the sum of the abscissa elements labeled i ii . The formula is:
l a b e l _ i _ r e c a l l = c o n f m a r t i x ( i , i ) ∑ j c o n f m a r t i x ( i , j ) label\_i\_recall=\frac{confmartix(i,i)}{\sum_j{confmartix(i,j)}}
label_i_recall=
∑
j
​
 confmartix(i,j)
confmartix(i,i)
​
 

Overall recall of samples (Macro-averaged MACRO-averaged): The average recall of all classes. The formula is:
a l l _ r e c a l l = a v g ( ∑ i l a b e l _ i _ r e c a l l ) all\_recall=avg(\sum_i{label\_i\_recall})
all_recall=avg(
i
∑
​
 label_i_recall)

Overall accuracy of the sample (Macro-averaged MACRO-averaged): Unlike the first, the macro-average is the mean of the accuracy of all classes. The formula is:
a l l _ p r e d i c t i o n = a v g ( ∑ i l a b e l _ i _ p r e d i c t i o n ) all\_prediction=avg(\sum_i{label\_i\_prediction})
all_prediction=avg(
i
∑
​
 label_i_prediction)

F1 value: The precision and recall of the overall sample (or a certain class) are as follows:
F 1 = 2 × p r e d i c t i o n × r e c a l l p r e d i c t i o n + r e c a l l F1=\frac{2\times prediction \times recall}{prediction + recall}
F1=
prediction+recall
2×prediction×recall
