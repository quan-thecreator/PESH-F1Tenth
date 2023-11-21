# Posterior probability

The posterior probability is a type of conditional probability that results from updating the prior probability with information summarized by the likelihood via an application of Bayes' rule. From an epistemological perspective, the posterior probability contains everything there is to know about an uncertain proposition (such as a scientific hypothesis, or parameter values), given prior knowledge and a mathematical model describing the observations available at a particular time. After the arrival of new information, the current posterior probability may serve as the prior in another round of Bayesian updating.In the context of Bayesian statistics, the posterior probability distribution usually describes the epistemic uncertainty about statistical parameters conditional on a collection of observed data. From a given posterior distribution, various point and interval estimates can be derived, such as the maximum a posteriori (MAP) or the highest posterior density interval (HPDI). But while conceptually simple, the posterior distribution is generally not tractable and therefore needs to be either analytically or numerically approximated.


## Definition in the distributional case

In variational Bayesian methods, the posterior probability is the probability of the parameters 
  
    
      
        θ
      
    
    {\displaystyle \theta }
   given the evidence 
  
    
      
        X
      
    
    {\displaystyle X}
  , and is denoted 
  
    
      
        p
        (
        θ
        
          |
        
        X
        )
      
    
    {\displaystyle p(\theta |X)}
  .
It contrasts with the likelihood function, which is the probability of the evidence given the parameters: 
  
    
      
        p
        (
        X
        
          |
        
        θ
        )
      
    
    {\displaystyle p(X|\theta )}
  .
The two are related as follows:
Given a prior belief that a probability distribution function is 
  
    
      
        p
        (
        θ
        )
      
    
    {\displaystyle p(\theta )}
   and that the observations 
  
    
      
        x
      
    
    {\displaystyle x}
   have a likelihood 
  
    
      
        p
        (
        x
        
          |
        
        θ
        )
      
    
    {\displaystyle p(x|\theta )}
  , then the posterior probability is defined as 

  
    
      
        p
        (
        θ
        
          |
        
        x
        )
        =
        
          
            
              p
              (
              x
              
                |
              
              θ
              )
            
            
              p
              (
              x
              )
            
          
        
        p
        (
        θ
        )
      
    
    {\displaystyle p(\theta |x)={\frac {p(x|\theta )}{p(x)}}p(\theta )}
  ,where 
  
    
      
        p
        (
        x
        )
      
    
    {\displaystyle p(x)}
   is the normalizing constant and is calculated as

  
    
      
        p
        (
        x
        )
        =
        ∫
        p
        (
        x
        
          |
        
        θ
        )
        p
        (
        θ
        )
        d
        θ
      
    
    {\displaystyle p(x)=\int p(x|\theta )p(\theta )d\theta }
  for continuous 
  
    
      
        θ
      
    
    {\displaystyle \theta }
  , 
or by summing 
  
    
      
        p
        (
        x
        
          |
        
        θ
        )
        p
        (
        θ
        )
      
    
    {\displaystyle p(x|\theta )p(\theta )}
  
over all possible values of 
  
    
      
        θ
      
    
    {\displaystyle \theta }
   for discrete 
  
    
      
        θ
      
    
    {\displaystyle \theta }
  .The posterior probability is therefore proportional to the product Likelihood · Prior probability.


## Example

Suppose there is a school with 60% boys and 40% girls as students. The girls wear trousers or skirts in equal numbers; all boys wear trousers. An observer sees a (random) student from a distance; all the observer can see is that this student is wearing trousers. What is the probability this student is a girl? The correct answer can be computed using Bayes' theorem.
The event 
  
    
      
        G
      
    
    {\displaystyle G}
   is that the student observed is a girl, and the event 
  
    
      
        T
      
    
    {\displaystyle T}
   is that the student observed is wearing trousers. To compute the posterior probability 
  
    
      
        P
        (
        G
        
          |
        
        T
        )
      
    
    {\displaystyle P(G|T)}
  , we first need to know:

  
    
      
        P
        (
        G
        )
      
    
    {\displaystyle P(G)}
  , or the probability that the student is a girl regardless of any other information. Since the observer sees a random student, meaning that all students have the same probability of being observed, and the percentage of girls among the students is 40%, this probability equals 0.4.

  
    
      
        P
        (
        B
        )
      
    
    {\displaystyle P(B)}
  , or the probability that the student is not a girl (i.e. a boy) regardless of any other information (
  
    
      
        B
      
    
    {\displaystyle B}
   is the complementary event to 
  
    
      
        G
      
    
    {\displaystyle G}
  ). This is 60%, or 0.6.

  
    
      
        P
        (
        T
        
          |
        
        G
        )
      
    
    {\displaystyle P(T|G)}
  , or the probability of the student wearing trousers given that the student is a girl. As they are as likely to wear skirts as trousers, this is 0.5.

  
    
      
        P
        (
        T
        
          |
        
        B
        )
      
    
    {\displaystyle P(T|B)}
  , or the probability of the student wearing trousers given that the student is a boy. This is given as 1.

  
    
      
        P
        (
        T
        )
      
    
    {\displaystyle P(T)}
  , or the probability of a (randomly selected) student wearing trousers regardless of any other information. Since 
  
    
      
        P
        (
        T
        )
        =
        P
        (
        T
        
          |
        
        G
        )
        P
        (
        G
        )
        +
        P
        (
        T
        
          |
        
        B
        )
        P
        (
        B
        )
      
    
    {\displaystyle P(T)=P(T|G)P(G)+P(T|B)P(B)}
   (via the law of total probability), this is 
  
    
      
        P
        (
        T
        )
        =
        0.5
        ×
        0.4
        +
        1
        ×
        0.6
        =
        0.8
      
    
    {\displaystyle P(T)=0.5\times 0.4+1\times 0.6=0.8}
  .Given all this information, the posterior probability of the observer having spotted a girl given that the observed student is wearing trousers can be computed by substituting these values in the formula:

  
    
      
        P
        (
        G
        
          |
        
        T
        )
        =
        
          
            
              P
              (
              T
              
                |
              
              G
              )
              P
              (
              G
              )
            
            
              P
              (
              T
              )
            
          
        
        =
        
          
            
              0.5
              ×
              0.4
            
            0.8
          
        
        =
        0.25.
      
    
    {\displaystyle P(G|T)={\frac {P(T|G)P(G)}{P(T)}}={\frac {0.5\times 0.4}{0.8}}=0.25.}
  An intuitive way to solve this is to assume the school has N students. Number of boys = 0.6N and number of girls = 0.4N. If N is sufficiently large, total number of trouser wearers = 0.6N+ 50% of 0.4N. And number of girl trouser wearers = 50% of 0.4N. Therefore, in the population of trousers, girls are (50% of 0.4N)/(0.6N+ 50% of 0.4N) = 25%. In other words, if you separated out the group of trouser wearers, a quarter of that group will be girls. Therefore, if you see trousers, the most you can deduce is that you are looking at a single sample from a subset of students where 25% are girls. And by definition, chance of this random student being a girl is 25%. Every Bayes-theorem problem can be solved in this way.


## Calculation

The posterior probability distribution of one random variable given the value of another can be calculated with Bayes' theorem by multiplying the prior probability distribution by the likelihood function, and then dividing by the normalizing constant, as follows:

  
    
      
        
          f
          
            X
            ∣
            Y
            =
            y
          
        
        (
        x
        )
        =
        
          
            
              
                f
                
                  X
                
              
              (
              x
              )
              
                
                  
                    L
                  
                
                
                  X
                  ∣
                  Y
                  =
                  y
                
              
              (
              x
              )
            
            
              
                ∫
                
                  −
                  ∞
                
                
                  ∞
                
              
              
                f
                
                  X
                
              
              (
              u
              )
              
                
                  
                    L
                  
                
                
                  X
                  ∣
                  Y
                  =
                  y
                
              
              (
              u
              )
              
              d
              u
            
          
        
      
    
    {\displaystyle f_{X\mid Y=y}(x)={f_{X}(x){\mathcal {L}}_{X\mid Y=y}(x) \over {\int _{-\infty }^{\infty }f_{X}(u){\mathcal {L}}_{X\mid Y=y}(u)\,du}}}
  gives the posterior probability density function for a random variable 
  
    
      
        X
      
    
    {\displaystyle X}
   given the data 
  
    
      
        Y
        =
        y
      
    
    {\displaystyle Y=y}
  , where

  
    
      
        
          f
          
            X
          
        
        (
        x
        )
      
    
    {\displaystyle f_{X}(x)}
   is the prior density of 
  
    
      
        X
      
    
    {\displaystyle X}
  ,

  
    
      
        
          
            
              L
            
          
          
            X
            ∣
            Y
            =
            y
          
        
        (
        x
        )
        =
        
          f
          
            Y
            ∣
            X
            =
            x
          
        
        (
        y
        )
      
    
    {\displaystyle {\mathcal {L}}_{X\mid Y=y}(x)=f_{Y\mid X=x}(y)}
   is the likelihood function as a function of 
  
    
      
        x
      
    
    {\displaystyle x}
  ,

  
    
      
        
          ∫
          
            −
            ∞
          
          
            ∞
          
        
        
          f
          
            X
          
        
        (
        u
        )
        
          
            
              L
            
          
          
            X
            ∣
            Y
            =
            y
          
        
        (
        u
        )
        
        d
        u
      
    
    {\displaystyle \int _{-\infty }^{\infty }f_{X}(u){\mathcal {L}}_{X\mid Y=y}(u)\,du}
   is the normalizing constant, and

  
    
      
        
          f
          
            X
            ∣
            Y
            =
            y
          
        
        (
        x
        )
      
    
    {\displaystyle f_{X\mid Y=y}(x)}
   is the posterior density of 
  
    
      
        X
      
    
    {\displaystyle X}
   given the data 
  
    
      
        Y
        =
        y
      
    
    {\displaystyle Y=y}
  .


## Credible interval

Posterior probability is a conditional probability conditioned on randomly observed data. Hence it is a random variable. For a random variable, it is important to summarize its amount of uncertainty. One way to achieve this goal is to provide a credible interval of the posterior probability.


## Classification

In classification, posterior probabilities reflect the uncertainty of assessing an observation to particular class, see also class-membership probabilities. 
While statistical classification methods by definition generate posterior probabilities, Machine Learners usually supply membership values which do not induce any probabilistic confidence. It is desirable to transform or rescale membership values to class-membership probabilities, since they are comparable and additionally more easily applicable for post-processing.


## See also

Prediction interval
Bernstein–von Mises theorem
Probability of success
Bayesian epistemology
Metropolis–Hastings algorithm


## References



## Further reading

![Bayes_icon.svg](./images/Bayes_icon.svg)
![Nuvola_apps_edu_mathematics_blue-p.svg](./images/Nuvola_apps_edu_mathematics_blue-p.svg)
