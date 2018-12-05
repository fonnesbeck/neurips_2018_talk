---?image=assets/img/PyMC3_bug.png&size=auto 80%&position=right
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

### Each slide in this presentation is provided as a *template*.

<br><br>

1. Select only the slide templates that you need.
1. Customize the template _markdown content_.
1. Optionally, override template _styles_ and _settings_.
1. Then present and publish with GitPitch @fa[smile-o]
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



---?image=assets/img/winbugs.jpg&opacity=20

@snap[north span-50 headline]
# WinBUGS
@snapend

---
@title[Academic Code]

```
class DisasterSampler(MetropolisSampler):
	"""
	Test example based on annual coal mining disasters in the UK. Occurences 
	of disasters in the time series is thought to be derived from a
	Poisson processes with a large rate parameter in the early part of 
	the time series, and from one with a smaller rate in the later part.
	We are interested in locating the switchpoint in the series using
	MCMC. 
		"""

	def __init__(self,burn=1000):
	
		MetropolisSampler.__init__(self,burn=burn)
		
		'Sample changepoint data (Coal mining disasters per year)'
		self.data = (4,5,4,0,1,4,3,4,0,6,3,3,4,0,2,6,
			3,3,5,4,5,3,1,4,4,1,5,5,3,4,2,5,
			2,2,3,4,2,1,3,2,2,1,1,1,1,3,0,0,
			1,0,1,1,0,0,3,1,0,3,2,2,0,1,1,1,
			0,1,0,1,0,0,0,2,1,0,0,0,1,1,0,2,
			3,3,1,1,2,1,1,1,1,2,4,2,0,0,1,4,
			0,0,0,1,0,0,0,0,0,1,0,0,1,0,1)
	
		'Switchpoint is specified as a parameter to be estimated'
		self.parameter(name='k',init_val=50,dist='uniform',scale=4,
			minval=0,maxval=len(self.data)-1)

		'Rate parameters of poisson distributions'
		self.parameter(name='Lambda',dist='exponential',
			init_val=[1.0,1.0],minval=0)
```


Note:

- heavy object oriented implementation
- goal: generality


---
@title[PyMC2]


Note:

- FORTRAN project on GH


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


Note:

- Monthly lab meetings
- Journal club
- Face-to-face meetings

---
@title[Final Slide]

