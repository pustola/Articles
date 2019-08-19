# Articles
## Data engineering
- [Transforming skewed data](https://medium.com/@ODSC/transforming-skewed-data-for-machine-learning-90e6cc364b0)<br>
  - Checking for skew:<br>
    1. Shapiro-Wilks test<br>
    if p-value < 0.05 skew is significant<br>
    
    ```python
    from scipy.stats import shapiro
    shapiro(data)[1]
    ```
    2. Using pandas .skew() (only numerical features)<br>
    
    ```python
    data.skew()
    ```
    
  - Correcting skew:<br>
  
    ```python
    data**2
    1/data
    np.log(data)
    ```
    
    
