## Data engineering
- [Transforming skewed data](https://medium.com/@ODSC/transforming-skewed-data-for-machine-learning-90e6cc364b0)<br>
  **Checking for skew:**  
  *1.Shapiro-Wilks test*   
  if p-value < 0.05 skew is significant     
  ```python  
  from scipy.stats import shapiro  
  shapiro(features)[1]  
  ```  
  *2.Using pandas .skew() (only numerical features)*  
   ```python  
   features.skew()  
   ```
  **Correcting skew:**    
   ```python
   features**2
   1/features
   np.log(features)
   ```
   *Box Cox transformation combines all three above:*  
   ```python
   from scipy.stats import boxcox
   for i in features:
   df[i], lambda = boxcox(df[i], lmbda=none)
   ```
     
  TO READ: [Imbalanced classes](https://opendatascience.com/strategies-for-addressing-class-imbalance/)
