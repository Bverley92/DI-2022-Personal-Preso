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

<!--- I am driven   --->
---
<!-- _class: odd -->
# What I do and bring
- DevOps Team
- Ask myself "Is there a better way" as I work
- Constantly thinking about solutions to things even while not working on them
<!---I work on a team that develops or improves tools designed to increase operational efficiency
I have worked on a couple of projects that aim to make health reporting more uniform across customers. But what I have really brought and will continue to bring is a desire to constantly do better. As I’m writing code, I ask myself “Is this a good way to accomplish the task at hand?” Many times, the answer has been “No” And I either switch gears or take the time to think about a better way to do it.--->

---

<!-- _class: even -->
# Personal Investments 
- Leaving Last Job
- Leap of Faith
- Pushed me to find something better
# Professional Accomplishments
- Graduation (finally) last year
- Starting here at Computacenter
<!---leaving my last job was a huge personal investment. It meant giving up a steady paycheck only to search for something better. It was a terrifying leap out of something financially comfortable. Without doing so, I never would have had the time or the drive to find something better for myself. I feel like if I had not left, I might still be there. 
Starting here. I get to work with an incredibly supportive team, working on solving problems and challenges.--->

---
<!-- _class: odd -->
# Planned Investments
### Short Term
- Kubernetes course
- Machine Learning Course
### Long term
- Continued Growth
- Avoid Stagnation

<!---In the short term there are a few courses that I want to take around Kubernetes and Machine learning. In the longer term, I haven’t nailed anything down yet, but I hope to have my sights set on new longer-term objectives soon so that I can constantly be invested in growing and improving my skills--->.

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

<!---I have run into a number of challenges while working at refactoring the daily health report scripts. At first, I had written it to run already written PowerShell scripts that I had adjusted to output a filetype that would work with the email api we wrote. I had planned to write similar code for each type of script I could come across, but after asking myself is this really the best way to do this, I quickly realized I could iterate over the type of scripts I had to run and only write it once. My current challenge is around cleaning text outputs from the machines into usable data. While I wrote something that works for the outputs I have, I know that I likely missed some output potential that what I wrote wont work for. I am hoping that existing apis that the machines have will help by giving data that isn’t text from a console output. --->


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
<!--- I'll end this on a quite story about an assignment I had a couple of years ago. The assignment was to create a class that had 30 parameters. The above script shows how we were taught to create a class, go parameter by parameter take them in at input, define them an so on. For thirty parameters that was going to be excessive. Instead I devised a way to take a dictionary and initialize a class out of it. In order to do this I had to spend far more time and investment figuring out how dictionaries work in then it would have taken me to write out each parameter and be done with it. I think that is a good representation of me. I will go to much farther lengths to accomplish a task efficiently, rather than by brute force. --->