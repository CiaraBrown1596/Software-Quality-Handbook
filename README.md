# Employee handbook for Software Quality control.

## A useful guide on best practices when writing and reviewing code
___
  # Table of contents
- [Employee handbook for Software Quality control.](#employee-handbook-for-software-quality-control)
  - [A useful guide on best practices when writing and reviewing code](#a-useful-guide-on-best-practices-when-writing-and-reviewing-code)
- [Table of contents](#table-of-contents)
    - [1.0 Introduction](#10-introduction)
    - [2.0 Task Estimation in scrum](#20-task-estimation-in-scrum)
      - [2.1 _Estimation based on story points in practice_](#21-estimation-based-on-story-points-in-practice)
      - [2.2  _Things to avoid during task estimation_](#22-things-to-avoid-during-task-estimation)
      - [2.3 _Summary_](#23-summary)
    - [3.0 Coding Standards](#30-coding-standards)
      - [3.1 _Common Aspects of a Coding Standard_:](#31-common-aspects-of-a-coding-standard)
      - [3.2 _Naming Conventions_](#32-naming-conventions)
      - [3.3 _Formatting and Indentation_](#33-formatting-and-indentation)
      - [3.4 _Comments and Documentations_](#34-comments-and-documentations)
      - [3.5 _Classes, Functions and Interfaces_](#35-classes-functions-and-interfaces)
      - [3.6 _Pointer and Reference Usage_](#36-pointer-and-reference-usage)
      - [3.7 _Testing_](#37-testing)
    - [4.0 Code Review](#40-code-review)
      - [4.1 _Tips for effective Code Review_](#41-tips-for-effective-code-review)
      - [4.2 _Unhelpful Practices_](#42-unhelpful-practices)
      - [4.3 _Summary_](#43-summary)



### 1.0 Introduction
This document serves as the complete definition of our organisations coding standards for source code.
This guide is will give you an introduction into the style of code and quality control that is currently practises within this company. The following is a guide into good tips and practices to follow and bad practices to avoid.

___

### 2.0 Task Estimation in scrum 

In Scrum Projects, Estimation is done by the entire team during Sprint Planning Meeting. The objective of the Estimation would be to consider the User Stories for the Sprint by Priority and by the Ability of the team to deliver during the Time Box of the Sprint. 

* Take care when selecting user stories for the Sprint, take into account the size of the product increment and the time it will take to complete. 

* A key benefit to task estimation in scrum is it gives the team a shared perspective of the user stories. 

*  The estimates for story points for all remaining work should be updated during the Sprint, even for those stories that have already been estimated. 

* This reflects the current state the development is in but can have the disadvantage that less planning will be done as the team knows they can alter estimates as they go along, if this can be avoided it is a good practice to adopt  

* When making estimates try not to estimate with the agenda of low value, you want your estimates to be unbiased. 

* Finally, we never provide that single estimate. We slap 25% and even 50% as most likely and worst-case scenarios on top. 

--- 
 

 #### 2.1 _Estimation based on story points in practice_

1. Team meeting. 

2. Discussion on the user story and its details. 

3. Individual estimation, with everyone making an estimate without revealing it. 

4. Once every team member has made an estimate, everyone simultaneously discloses the values they assigned. 

5. If team members agree as to the value, the user story is assigned the given number of points. If not, the team negotiates and goes back to point 3. 

--- 

#### 2.2  _Things to avoid during task estimation_ 

* Different understanding of story points within the team can lead to over or under estimations, make sure the story points are clear and concise. 

* The more complex the task the higher rate of inaccuracy. 

* Avoid changing the value of story points during the implementation process. 

* Be realistic, don't rely on overly optimistic work conditions and outcomes. 
 

--- 

#### 2.3 _Summary_ 

Test yourself when you start estimating, estimate the work first yourself before asking team members to provide estimates, then discuss how close you were and how each team member came up with their estimate. The more practice you get the more accurate it will become. You should be able to work out early if task estimations is a strenght or weakness of yours and the team can plan accordingly. Watch out for the issues mentioned above when putting together timeframes for a project.

___
___

### 3.0 Coding Standards 

Coding standards are a set of conventions and guidelines for a specific programming language that recommend programming style, practices, and methods for each aspect of a program written in that language. 

A coding standard does not usually concern itself with wrong or right in a more abstract sense. It is simply a set of rules and guidelines for the formatting of source code. 

___ 

 
 

#### 3.1 _Common Aspects of a Coding Standard_: 

 
 

* Naming Conventions 

* Formatting and Indentation 

* Comments and Documentation 

* Classes, Functions and Interfaces 

* Pointer and Reference Usage  

* Testing 

___ 

####  3.2 _Naming Conventions_ 

* Meaningful variable names so everyone understands the reason for using it. 

* Local variables should start with a lower case. 

* Avoid using digits in variable names 

* Good practice for variable names to be descriptive. 

* Global variables must have _STRONGLY_ defined names. 

___ 

#### 3.3 _Formatting and Indentation_ 

* The best style of Indentation is a consistent style; you should follow the existing style that is being used when collaborating on a project. 

* The reason for this is that these aspects play a critical role in the readability of source code. 

* Whitespace is a critical component of style because of cross-compatibility. The code must be readable across different platforms 

* Keep indentation style consistent. The following are a list of acceptable styles to use. 

 
 

Style 1: 

 
 

 ```function foo() { 

    if ($maybe) { 

        do_it_now(); 

        again(); 

    } else { 

        abort_mission(); 

    } 

    finalize(); 

} 

 
 

Style 2: 

 
 

function foo() 

{ 

    if ($maybe) 

    { 

        do_it_now(); 

        again(); 

    } 

    else 

    { 

        abort_mission(); 

    } 

    finalize(); 

} 

 
 

Style 3: 

 
 

function foo() 

{   if ($maybe) 

    {   do_it_now(); 

        again(); 

    } 

    else 

    {   abort_mission(); 

    } 

    finalize(); 

} 

``` 

___ 

#### 3.4 _Comments and Documentations_ 

* The code should be properly commented for understanding easily. Comments regarding the statements increase the understandability of the code. 

* Strategic comments help others understand the code clearer. 

* Write comments as you go on all global and public variables as well as all major functions. 

* Major functions comments should include a header and a description of the function. 

* if complicated logic is being used, it is a good practice to leave a comment "block" near that part so that another programmer can understand what exactly is happening. 

* Commenting your code is fantastic; however, it can be overdone or just be plain redundant. Take this example: 

``` 

// get the country code 

$country_code = get_country_code($_SERVER['REMOTE_ADDR']); 

  

// if country code is US 

if ($country_code == 'US') { 

  

    // display the form input for state 

    echo form_input_state(); 

} 

``` 

When the text is that obvious, it's not productive to repeat it within comments. 

 
 

If you must comment on that code, you can simply combine it to a single line instead: 

``` 

// display state selection for US users 

$country_code = get_country_code($_SERVER['REMOTE_ADDR']); 

if ($country_code == 'US') { 

    echo form_input_state(); 

} 

``` 

 
 

#### 3.5 _Classes, Functions and Interfaces_ 

* The code that a programmer writes should be simple.  

* Complicated logic for achieving a simple thing should be kept to a minimum since the code might be modified by another programmer in the future. 

* Too many levels of nesting can make code harder to read and follow, for readability, it is usually possible to make changes to your code to reduce the level of nesting. 

* Lengthy functions are very difficult to understand, functions should be small enough to carry out small work and lengthy functions should be broken into small ones for completing small tasks. 

 
 
 

#### 3.6 _Pointer and Reference Usage_ 

* They can be as short as a single character. 

* Use plain objects and references unless you really can't. 

* Use plain pointers, you should be really known what are you doing if you are this far. 

* Use consistent names for your temporary variables that have the same kind of role. 

``` 

{ for (int i=0;i<=10;i++) 

    System.out.println("Index is : " + i); 

    i++; 

} 

``` 

#### 3.7 _Testing_ 

* Start testing code as early as possible, don't have to test all the code at once but test functions as they are developed. It is important to determine the test objects and scope as early as possible. 

* Testing should be split into prioritize sections so that section with the highest priority are tested first. 

* Be aware that software will very rarely be 100% bug-free. Testing can never prove the software to 100% bug-free. 

* Test cases should be planned before coding starts, test cases are developed while the application is being designed. 

* _Note_ that time available for testing is not unlimited and that an effective test plan is very crucial before starting the process of testing. 

 
___
___
### 4.0 Code Review  

 
 

Code review is a software quality assurance activity in which one or several people check a program mainly by viewing and reading parts of its source code, and they do so after implementation or as an interruption of implementation. It is important that at least one of the persons reading must not be the code's author. 

It is important to _Note_ People make mistakes and that is completely all right. Bugs might appear in code, even after a good review. 

 
 

Although quality problem discovery is a main goal of a code review, they are also performed to reach other goals too, such as;  

 
 

* Complying with QA guidelines i.e., air-travel software.  

 
 

* Finding bugs or potential problems and provide ways they could be fixed.  

 
 

* Helps in transferring knowledge about the codebase, solution approaches, expectations regarding quality, both to the reviewers as well as to the author. 

*  Improve the structure of the code if possible. 

 
 
 

___ 

 
 

#### 4.1 _Tips for effective Code Review_  

 
 

* Take your time when reading but don't read any more than 200 - 400 lines of code at one time, you need to have a break in between review sessions to give your brain a chance to rest.  

 
 

* It is important when reviewing that you understand the code, what it is trying to accomplish and what the requirements are so you can confirm that it is fulfilling its requirement.  

 
 

* Try is be constructive with your feedback, rather than critical, try to explain to the auther how they could make it clearer to the reader.  

 
 

* Everyone is included in the review process, no matter how senior, everyone needs to review and be reviewed so we can produce the best quality product for customers. Developers at different levels will notice different types of problems.  

* Good code review will improve overall quality of the code, but it will also reduce the risk related to a new feature. 

 * Use a checklist, Checklists are the most effective way to eliminate frequently made errors.They also provide team members with clear expectations for each type of review and can be helpful to track for reporting and process improvement purposes.
 

___ 

 
 

#### 4.2 _Unhelpful Practices_  

* Make sure the auther knows why you are editing something, clear documentation is needed here, don't make changes out of personal preference. Be sure to provide context for your recommendation. 

* Style and syntax have nothing to do with the issues the developer might be trying to solve so they shouldn't be discussed in the review. 

* When pointing out an error, if it continues throughout the code in the same way try to avoid pointing it out every time, after the first comment the auther can find each instance of it and make that change themselves. It allows you to convey the same message without overwhelming the review seeker. 

* Review seekers can contribute to unsupportive environments, too. If you merge code without addressing all the feedback, people are left wondering why they bothered to help you, and you send the message that some opinions are worth more than others. 

 * If a comment is out of scope or you won’t be taking action on the feedback, just provide a brief note explaining why. 

 ___
 #### 4.3 _Summary_
The code review is extremely important part of the whole software development process. Therefore, whole team must make enough effort to properly plan time needed for process. Mistakes are bound to happen to those who work in developing code. Code review is essentially a risk management, therefore it should be treated as such.
Feedback is important and it is important that developers can support each other when reviewing or being reviewed to ensure the code is up to standard and becoming a strong as a development team.

















