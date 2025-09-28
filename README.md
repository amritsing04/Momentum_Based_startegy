# Momentum_Based_startegy 
Momentum_based Quant Startegy is very simple and beginner friendly strategy which simply suggest that if any asset in stock market has performed well in past, It is highly possible that it can perform well in future as well.
For this strategy, we have used PHLX Gold/Silver Sector (^XAU). For this is highly compatible for strategy.

# data['Returns']=np.log(data['Close']/data['Close'].shift(1))

This line of code is used to calculate return of asset using log.

# data['position']=np.sign(data['Returns'].rolling(3).mean())
# data['strategy']=data['position'].shift(1)*data['Returns']

To understand the logic of code, First we try to understand that position is used to show whether we have bought or sold the asset. From returns of the asset, we have calculate the mean of previous 3 days; then if the mean is negative, we short the asset or if the mean is positive, we long the asset.


