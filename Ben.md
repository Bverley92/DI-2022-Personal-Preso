---
marp: true
theme: uncover
style: |
    {
     --color-background: orange;
     font-family: Garamond;
     color: white;
    }
    section.split {
        display: grid;
        grid-template-columns: 500px 500px;
        grid-template-rows: 100px auto;
        grid-template-areas: 
            "slideheading slideheading"
            "leftpanel rightpanel";
    
    }
    section.split h1 {
        grid-area: slideheading;
        font-size: 70px;
    }
    section.split h3 {
        grid-area: slideheading;
        text-align: center
    }
    .ldiv { 
        grid-area: leftpanel;
        margin: auto;
        width: 85%;
        padding: 10px;
        border-style: solid;
        border-width: 5px;
        border-color: white;
    }
    .rdiv { 
        grid-area: rightpanel;
        margin: auto;
        width: 85%;
        padding: 65px;
        border-style: solid;
        border-width: 5px;
        border-color: white;
        }
    .ldiv2 { 
        grid-area: leftpanel;
        margin: auto;
        width: 90%;
        padding: 10px;
    }
    .rdiv2 { 
        grid-area: rightpanel;
        margin: auto;
        width: 99%;
        padding: 1px;
        }
    section.odd {
        --color-background:white;
        color: orange;
    }
    section.even {
        --color-background: orange;
        color: white;
    }

---

<!--_class: odd -->
# Ben Verley 
### DevOps Engineer
B.S. Information Technology - ASU
Start date: Jan 3 2022
![bg right](Photos/Ben.jpg)

---
<!-- _class: split -->
# About Me

<div class=ldiv>

### Driven By
- Quality
- Efficiency
- Self Improvement
- There is always a better way

</div>

<div class = rdiv>

### Challenges
     
- Opportunity for self improvment
- Prevent stagnation

</div>

<!--- 
In terms of coding or other work, I always aks myself is there a better way to accomplish this? This mindset of constant improvement is what drives quality and efficient work.

In temrs of challenges, I relish them. They consistantly provide avenues for self improvement and prevent stagnation. To put it another way I'm the guy that plays strategy games on the hardest difficulty available.
 --->
---
<!-- _class: odd -->
# What I do and bring
- DevOps Team
- Constantly thinking about solutions to things even while not working on them
<!---I work on a team that develops or improves tools designed to increase operational efficiency for the rest of the team.
When I am given a project or a problem, I will keep proccessing that problem until a workable solution is in place. That proccess runs in the back of my mind pretty much all the time regardless of what I am doing. --->

---

<!-- _class: even -->
# Personal Investments 
- Leaving Last Job
- Leap of Faith
- Pushed me to find something better
# Professional Accomplishments
- Graduation (finally) last year
- Starting here at Computacenter
<!---leaving my last job was a huge personal investment. It meant giving up a steady paycheck only to search for something better. It was a leap out of something financially comfortable but physically and mentally debilitating. Without doing so, I never would have had the time or the drive to find something better for myself. I feel like if I had not left, I might still be there. 
As for professional accomplishments, obviously I graduated cum laude last year, which led to starting here. I get to work with an incredibly supportive team, working on solving problems and challenges that operation faces and I coulnd't be more excited about that.--->

---
<!-- _class: odd -->
# Planned Investments
### Short Term
- Kubernetes course
- Machine Learning Course
### Long term
- Continued Growth
- Avoid Stagnation

<!---In the short term there are a few courses that I want to take around Kubernetes and Machine learning. In the longer term, I hope to be constantly be invested in growing and improving my skills and avoiding stagnation--->.

---

<!-- _class: split -->
# What Worked

<div class=ldiv2>

- PowerShell script to post to email API
- Couldn't test for two weeks
- Eventually moved the structure to python
<!---The PowerShell script I wrote to send emails through the email api project we built worked well. I wrote it unable to test it until I was able to get the latest PS version installed. When I went to test it, it worked. I ended up taking that structure and migrating to Python for the rest of the project.--->

</div>

<div class=rdiv2>

```PowerShell
$URL='127.0.0.1:8000/email'
$Form = @{
    Token = $Token
    ID = $ID
    sender = $sendFrom
    subject = $subject
    to = $sendTo
    cc = $cc
    bcc = $bcc
    body = $body
    report_name = $repName
    table_title = $tableTitle
    file = Get-Item $file
}
$Response = Invoke-RestMethod..
return $Response
```

</div>

---

# What hasn't worked
<!-- _class: odd -->
- Mixing Python and PowerShell with some success early on in the Refactor Project
- Ultimately I found myself needing to do things that PS was ill suited for

<!---Early on in the refactor project, I designed a python script that ran powershell scripts that already existed with slight modifications to meet the parameters of the email api. While this was functional, there were things that were a bit clunky to keep doing in powershell, and that python can just do better.. --->


---
# Final Story

Taught in class
```python
class Product:
    def __init__(self, dataSRC='NULL', product = 'NULL', othervar='NULL'):
        self.dataSRC = dataSRC
        self.product = product
        self.othervar = othervar
```

My solution for 30 parameter class
```python
class Product:
    def __init__(self, dictionary):
        self.dictionary = dictionary
        for key, value in dictionary.items():
            setattr(self, key, value)
```
<!--- I'll end this on a quick story about an assignment I had a couple of years ago in school. The assignment was to create a class that had 30 parameters. The above script shows how we were taught to create a class, go parameter by parameter take them in at input, define them an so on. For thirty parameters that was going to be excessive. Instead I devised a way to take a dictionary and initialize a class from it. I had to spend far more time and investment figuring out how dictionaries could be applied in this manner then it would have taken me to write out each parameter and be done with it. I think that is a good representation of me. I prefer to figure out solutions that are effecient, rather than by brute force. --->
