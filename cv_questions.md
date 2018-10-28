#### Project Question
1. Predicting Poverty competition in DRIVENDATA
2. Mercari Price Suggestion Challenge in Kaggle
3. Implement Convolution Neural network in Numpy
4. Predicting CO_2 concentration by Gaussian Process Regression
5. Decrypting Messages with MCMC samples
>1. use MCMC to find the key of decrypting message.
>2. Follow the rule of markov chain, the status in the markov
> chain will convergen through transition probability matrix.
> stationary distribution is expected posterior distribution.
> MCMC have accept rate, Metropolis-Hastings algorithm to adjust
> the accept rate to 1.
> become efficient, increase the accept rate.


6. Training mixture of Gaussian Model for distinguishing apple pixel
7. Copper Price Prediction
> Using machine learning algorithm to predict copper future
> price with rolling windows.
>
> Features:
> cu_shfe_price
> cu_lme_price
> cu_lme_stock
> ted: 3-Month US treasury note
> ted_spread: Spread between 3-Month LIBOR and treasury bill
> bdi: Baltic Dry Index
> vix: CBOE Volatility Index
> gsci: Goldman Sachs Commodity Index
>
>Data Process:
>match all features to same date, fill nan value, no need to
>address data frequency, transform closed data with log-return
>in order to match in normal distribution and be stationary.
>Stationary test: autocorrelation and partial autotcorrelation.
ADF: augmented Dickey-Fuller(adf) TEST
>
>ARIMA(autoregressive integrated moving average)
>with different lag price
>ARIMA model to approach stationary stochastic process
>parametric method
>AR: explain the momentum and mean reversion effect
>I: difference of observation to make it stationary
>capture the shock effect observed in white noise term
>How to select model: AIC(akaike information criterion) to mearsure
>model performance
>
>Gaussian Process Regression
>For the arima, we assume the process is linear
>non-parametric method, no assumption about the stochastic process
>we can consider extra feature and non-linear relationship, learn the
probability distribution of stochastic process.
>Kernel: RBF, Matern, Rational Quadratic, Dot-Product, Exp-Sine-Squared
>Gaussian Process Regression: we use zero mean GP as prior of underlying function,
>and additive noise model as likelihood to define the bayesian inference.\
>posterior P(Y|f)
>finally, we get the mean and covariance of underlying function
>
>The time comlexity of gaussian process is O(n3) because inverse matrix.
> if we use matrix-vector , we can reduce the complexity to O(n2)
>
>Multiple kernel learning
>apply multiple learning in kernel ridge regression
>In simple, we replace a simple kernel with multiple weighted kernel linearly
>The weight value can be assumed as regulazation parameter. Then we can find
>the value through lagrangian.
>
>
>Evaluation:
>MSE: Mean Square Error
>Spearman Rank correlation: Difference in paired rank and n is the
number of pairs


8. Real-time Traffic Control System

9. News Stance
>news headline, news body text, label is the relative level, agree, disagree,
> discuss, unrelated
> 1. split to train data and test data.
> we want to find features!!!
> 2. transfrom word to vector representation: 1. word2vec 2.TF-IDF to transfomr
> word to vector and then compute cosine similarity. The higher value of cosine similarity
> of a pair is more similar between headline and article body.
> 3. Language model based representation
>    LDA to find document-topic-word distribution.
>    Then use KL-divergence to compute headline distribution
> and the article body distribution.
>    function: get_document_topic can return the headline distribution.
> 4. use linear or logistic regression to train the model


10. Latent Dirichlet Allocation with Gibbs Sampling
> Gibbs sampling satsify detailed balanced. finanlly get the joint distribution
> p(x1, x2, x3, x4,... xn) we only select one axis to transfer.
>support we have D document, A article, w words
>we want to find the topic distribution of each document and
> word distribution of each topic.
>we set the prior of topic and word is Dirichlet distribution（设定主题跟词的分布是Dirichlet分布）
>
>Dirichlet-multinoimal conjugate to find the posterior of the document-topic distribution and
> topic-word distribution. Then we can get the document-words joint distribution.
>
>process:
>use gibbs to set topic for each words because we have the joint distribution of
>word and topic.
>
>
>LDA是文本分析里面一个很有名的topic model，它基于一个简单的词袋模型，通过概率建模，得到文档和词汇的主题分布。由给定的先验Dirichlet分布，得到文档生成的似然函数，然后得到Gibbs Sampling收敛时的分布，就是topic的对应分布. Gibbs Sampling采样的是每个词每一次应该如何决定跳转到哪个topic。
>
>
>
>
>
>
>
>
>
>
>
>


11. Kernel Canonical Correlation Analyst
>its a method to capture non-linear association in high
>dimensional data.
>
>Canonical correlation analyst:
>Given two one column vector X= (x1,x2..xn) and Y=(y1, y2,...,yn), and then
> we can compute the covariance matrix of this two vector. CCA is
> to seeks vectors a and b such that the random variable a'X and b'Y
> maximize the correlation p= corr(a'X, b'Y). In simple, find the projection
of X and Y which have maximum correlation.
>
>KCCA, one column become high dimenstion, then we use kernel trick.
>Using lagrangian to maximize the covariance.

#### Experience Question
1. Schneider Electric
> The project is to find a smart real-time monitor for the large
> switchboard. Since the switchboard are used in large public building, such as school,
> hospital, and it may gradually damaged by air or moist environment. Firstly, I get to know basic
> attribute, temperature test, mechanical test, partical charge test. Then, find possible monitor
embed in the switchboard and upload machine data in real-time. Finally, try to find some algorithm to
predict the possible problem in the future.

#### Academic Study Question
1. Natural Language Process
2. Data Mining
