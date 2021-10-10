# Schedulet

Improving the course organization process.

This is a webapp that allow user to upload their course outline and get a downloadable excel sheet after it is uploaded.

## Inspiration
As a group we all shared one thing in common. School. We knew about the strenuous task of having to constantly look at our course outlines, or even worse, manually enter every due date into a calendar. However, most of the time, this is the only way to make sure you aren't missing any tasks. We explored other areas when brainstorming on FigJam, but decided to go with this direction as it was what we knew best.

## Primary Research Findings

:: marker

We surveyed 48 students in total and these were the results:

When you first get your syllabus, do you record all the deadlines and due dates in your calendar? 71% said yes; 29% said no
Have you ever missed a deadline for an assignment or a quiz? 77.4% said yes; 22.6% said no
Would you prefer a visually appealing schedule or a simple one? 74.2% said visually appealing; 25.8% said simple
Does a lack of organization in your schedule cause you any stress? 71% said yes; 29% said no
How often do you forget an assignment or test? 11.8% said never; 70.6% said sometimes; 17.6% said often
How long does it take you in hours to set up your class schedule? 64.7% said 1 hour; 11.8% said 2 hours; 11.8% said 3 hours; 11.8% said 4 hours
Do you ever find it hard to locate information about your classes? 82.4% said yes; 17.6% said no

What it does
This is why we created Schedulet. Schedulet is a platform that provides an easy way to scan your PDF course outline, extract the important keyword and helps creating a downloadable excel file with all the important information such as Professor Info, Marks Breakdown and Course Schedule. One of our main feature is a modified excel sheet where we help to create a marks breakdown sheet where you can put in the input of your score and calculate your final score.

How we built it
Figma
We prototyped the solution using Figma. We began by visualizing the process with a user flow so we could anticipate what frames would be needed. We then wire-framed how the website would work and finished off by creating a medium fidelity prototype and clean branding.

Back-end
We built our back-end with Flask and front-end with HTML/CSS. We started by breaking the problem into 4 different chunks; user upload, convert data to an html, filtering html with keywords and allow user to download the final excel file. The reason we convert the data into html because it give us a structure that we are able to navigate the keyword using BeautifulSoup easily. After extracting all the data that we need, we need to write the data into an excel file. We used openpyxl to help us to do excel modification such as adding formulas to the mark breakdown sheet with Python. The solution that we currently having is not scalable and not efficient. We would like to further optimise the filtering system with technology like computer vision and machine learning.

Challenges we ran into
A major challenge we faced was time constraint. We had many ideas of all the different aspects of we wanted to add into the program but not enough time to execute them.

Accomplishments that we're proud of
The major accomplishment we are proud of solving the real-time issue with the use of know tech stacks and working as a team to problem solve ideas. We are also proud of how the design of our presentation and demo came out.

What we learned
For a couple of us, this was our first Hackathon and while it was a learning curve in the beginning we quickly got into the way of how it works. Some of us learned a new programming language and API's. Our designer also learned how to prototype the full beginning to end process on Figma for the first time in a hackathon.

Built With
css
figma
flask
html
python

### The filtering/ extract method
The filtering of the course outline is done by converting the pdf file into HTML structure. This is to allow us to have a easier structure to navigate throught and locate the keyword that we need such as Instructor info, Schedule, and Weighting. We use Camelot to find potential table where most of the schedule or weighting information will be presented in tables. We use Beautiful Soup to navigate throught the converted HTML and get the keywords that we need. 

This solution is not perfect and not scalable. We are planning to further extend the filtering system with computer vision and machine learning. We can use computer vision to scan through the file and give us the most important part of the page and feed into a ML system where we can predict which part do we need to extract. 

### The modify
After getting all the data into an excel file, we use openpyxl to modify the Weighting sheets where we locate the columns of weight and started to modify the weightage by changing the number formate in excel, so that the calculation can be done easily after the user downloaded the file. This part is not scalable too but we are planning to brainstorm more ideas to make this processs "smarter"
