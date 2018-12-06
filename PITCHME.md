---?image=assets/img/PyMC3_big.png&size=auto 80%&position=right
@title[Title Slide]

@snap[north-west]
## **PyMC's Big Adventure**

#### **Lessons Learned from the Development of Open-source Software for Probabilistic Programming**
@snapend

@snap[south-west byline text-orange]
#### **Chris Fonnesbeck, Vanderbilt University Medical Center**
Machine Learning Open Source Software 2018: Sustainable communities
NeurIPS 2018
@snapend

---
@title[What is PyMC?]

# What is PyMC?

<br><br>

- Select only the slide templates that you need.
- Customize the template _markdown content_.
- Optionally, override template _styles_ and _settings_.
- Then present and publish with GitPitch @fa[smile-o]
<br><br>


---
@title[Origins]



---
@title[Motivation]

@snap[west span-100]
### @color[#E49436](Why PyMC?)

<br> 
#### **Bayesian modeling for @color[#E49436](applied) users @fa[smile-o]**
@snapend

---?image=assets/img/winbugs.jpg&opacity=40

@snap[north headline]
## WinBUGS
@snapend

---

```r
model {
     for (j in 1:J){
       y[j] ~ dnorm (theta[j], tau.y[j])
       theta[j] ~ dnorm (mu.theta, tau.theta)
       tau.y[j] <- pow(sigma.y[j], -2)
     }
     mu.theta ~ dnorm (0.0, 1.0E-6)
     tau.theta <- pow(sigma.theta, -2)
     sigma.theta ~ dunif (0, 1000)
   }

```

---?image=assets/img/pymc_1.png&size=auto 70%

@snap[north]
### PyMC @color[#E49436](1.0)
@snapend

Note:

- heavy object oriented implementation
- goal: generality


---
@title[PyMC2]

### And Then There Were Three ...

@div[left-50]
<br><br>
![MONKEY](assets/img/anand.jpeg)
@divend

@div[right-50]
<br><br>
![MONKEY](assets/img/david.jpeg)
@divend


---
@title[FORTRAN]

![](assets/img/pymc_fortran.png)

---
@title[HMC]


---
@title[John's Blog Post]


---
@title[PyMC3]


---
@title[Showing off]


---
@title[Crisis]

@snap[north-west]
# PyMC3 in Crisis!
@snapend

---?image=assets/img/photo.jpeg&size=auto 90%

---
@Title[Theano's Demise]

---
@title[Keys to Success]


---
@title[Pro Tips]


Note:

- software for remote teams: Slack

---
@title[Building a Culture]

### Project Culture

Note:

- Monthly lab meetings
- Journal club
- Face-to-face meetings

---
### PyMC 