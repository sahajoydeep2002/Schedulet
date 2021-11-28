<h1 align = "center" font = "">Schedulet</h1>
<p align = "center">
<img class = "center" width = 130% src="Presentaion Deck.png">
</p>

<h3 align = "center" font = "">Improving the course organization process.</h3>

This is a web app that allows the user to upload their course outline and get a downloadable excel sheet after it is uploaded.

## Inspiration
I knew about the strenuous task of having to constantly look at my course outlines, or even worse, manually enter every due date into a calendar. However, most of the time, this is the only way to make sure you aren't missing any tasks. I explored other areas when brainstorming on FIGJAM, but decided to go with this direction as it was what I knew best.

## Primary Research Findings

I surveyed 48 students in total and these were the results:

#### When you first get your syllabus, do you record all the deadlines and due dates in your calendar? 71% said yes; 29% said no

#### Have you ever missed a deadline for an assignment or a quiz? 77.4% said yes; 22.6% said no

#### Would you prefer a visually appealing schedule or a simple one? 74.2% said visually appealing; 25.8% said simply

#### Does a lack of organization in your schedule cause you any stress? 71% said yes; 29% said no

#### How often do you forget an assignment or test? 11.8% said never; 70.6% said sometimes; 17.6% said often

#### How long does it take you hours to set up your class schedule? 64.7% said 1 hour; 11.8% said 2 hours; 11.8% said 3 hours; 11.8% said 4 hours

#### Do you ever find it hard to locate information about your classes? 82.4% said yes; 17.6% said no

## What it does
This is why we created Schedulet. Schedulet is a platform that provides an easy way to scan your PDF course outline, extract the important keyword and help create a downloadable excel file with all the important information such as Professor Info, Marks Breakdown and Course Schedule. One of my main features is a modified excel sheet where I help to create a marks breakdown sheet where you can put in the input of your score and calculate your final score.

# Demostration : 

https://youtu.be/2fYlXxG837I

# Try my product :

https://www.figma.com/proto/vDg5Uo5pwHJDrnZ8vTixAb/Pitch-Deck-Design-Community?node-id=102%3A6&scaling=scale-down&page-id=102%3A2&starting-point-node-id=102%3A6

# How I built it
## Figma
I prototyped the solution using Figma. I began by visualizing the process with a user flow so I could anticipate what frames would be needed. I then wire-framed how the website would work and finished off by creating a medium-fidelity prototype and clean branding.

## Back-end
I built my back-end with Flask and front-end with HTML/CSS. I started by breaking the problem into 4 different chunks; user upload, converting data to HTML, filtering HTML with keywords and allowing users to download the final excel file. The reason I convert the data into HTML is that it gives us a structure that I am able to navigate the keyword using BeautifulSoup easily. After extracting all the data that I need, I need to write the data into an excel file. I used openpyxl to help us to do excel modifications such as adding formulas to the mark breakdown sheet with Python. The solution that I currently have is not scalable and not efficient. I would like to further optimize the filtering system with a technology like computer vision and machine learning.

## Challenges I ran into
A major challenge I faced was a time constraint. I had many ideas of all the different aspects I wanted to add to the program but not enough time to execute them.

## Accomplishments that I’m proud of
The major accomplishment I am proud of solving the real-time issue with the use of know tech stacks. I am also proud of how the design of my presentation and demo came out and getting an opportunity to present my project to The World After Covid-19 LIVE By KPMG.

## What I learned
For me, this was my first Hackathon and while it was a learning curve in the beginning I quickly got into the way of how it works. Some of us learned a new programming language and API. My designer also learned how to prototype the full beginning-to-end process on Figma for the first time in a hackathon.

## Built With
#### css
#### figma
#### flask
#### html
#### python

### The filtering/ extract method
The filtering of the course outline is done by converting the pdf file into an HTML structure. This is to allow us to have an easier structure to navigate through and locate the keyword that I need such as Instructor info, Schedule, and Weighting. I use Camelot to find a potential tables where most of the schedule or weighting information will be presented in tables. I use Beautiful Soup to navigate through the converted HTML and get the keywords that I need. 

This solution is not perfect and not scalable. I am planning to further extend the filtering system with computer vision and machine learning. I can use computer vision to scan through the file and give us the most important part of the page and feed it into an ML system where I can predict which part do I need to extract. 

### The modify
After getting all the data into an excel file, I use openpyxl to modify the Weighting sheets where I locate the columns of weight and started to modify the weightage by changing the number formate in excel so that the calculation can be done easily after the user downloaded the file. This part is not scalable too but I am planning to brainstorm more ideas to make this process "smarter"
