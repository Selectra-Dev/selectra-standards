# General Project management workflows

 - Projects
    - Announce the project
    - Define the different steps and the team
    - Write the specifications
    - Quotations
    - Design
    - Kick-off meeting
    - Development
 - Maintenance
     - Generalities
     - Drupal modifications


## Projects
  In order to build a reliable technical infrastructure, improve development time and reduce maintenance cost, it is essential that every project follows precise workflows. Therefore, when starting a new project, you **MUST** follow the following steps:

## 1. Announce the project

The technical staff must be aware of the very existence of the project from the start. To that end, as soon as you start working on a new project you **MUST** :
 - Create a new card on [this board](https://trello.com/b/EI6byZd7). This card should provide a bird view of the project state. Here's what it **MUST** contain : [What should I put in a card?](https://trello.com/c/TiFmB8VC).
 - Announce it on #project: a quick message mentioning the new project will do! And don't forget to add a link to the corresponding trello card.
 - Create a new slack channel: #project-$nameOfyourProject

## 2. Define the different steps of your project, and who should be a part of it

"Do I need a design? Should I include a design for the back office?",
"Do I need an integration?",
"Do I need a back-end developer? ", "is it a Drupal project? "

These are the kind of questions you **SHOULD** ask yourself at the very beginning of the project. It is important to try to define each step of the project - this way, you'll know who you need on your team.

It's of the utmost importance to know from the beginning who will be part of the project. You **SHOULD** try to anticipate every single person who will have a role to play and you **MUST** decide who will be validating each step of the project.

For a project from scratch, here's the overall team:

- *Stake holders*: the people who ordered the project. Most of the time, they are responsible for validating most of the project steps
- *Design*: the designer
- *Front-End*: the developers who will be developing the Front-End. (Remember, Front-End is basically everything you see on a web application)
- *Back-End*: the developers who will be developing the Back-End.
- *System administrator*: who will be responsible for deploying the projects and defining technical constraints. (WARNING don't feed the system administrator after midnight)
- *Project manager*: if you don't know who that is you probably shouldn't be reading this

## 3. Write the specifications

The specifications are here to explain your vision of the product.
When writing specifications the first thing to know is: you can't write perfect specifications. Nobody can, especially for a web application. However, the key is to describe your needs in simple terms. Don't try to mix the description of the functionalities you want with how to implement them. If you do have technical recommendations to make, it **MUST** be completely independent from the functionality description.

It's strongly **RECOMMENDED** that you follow a pattern resembling this:
"As a [user] I want to [functionality] so that [business value of the functionality]"

Specifications **MUST** be validated by the technical staff before being sent to the freelancers.

## 4. Quotations

If you call on freelancers for this project. you **MUST** ask for all the quotations before going to the next step. Quotations **MUST** be validated by the technical staff and the stake holders.

## 5. Design

If you need a design for the project, you **MUST** follow the workflow defined in `design.md`

## 6. Kick-off meeting

Before launching **any** development whatsoever you **MUST** organize a kick-off meeting with every member of the team. This meeting is essential to the development phase. This way, the developers and the sysadmin can discuss the implementation of our standards and other technical concerns.

## 7. Development

Project management methods are currently being studied - in the meantime here are some general recommendations:
 - You **SHOULD NOT** keep the Front-End team and the Back-End team separated, as it could be the source of lots of technical problems. It's better to have both teams work on the same functionality at the same time: it allows things to go more smoothly.
 - If a technical question arises, you **MUST** notify either the system administrator or a digital project manager. This is especially important when working with external freelancers.


# Maintenance

## Generalities

You **SHOULD** always notify the technical staff when you want to perform a technical operation, or modify a file on a FTP (except for images and PDF). A technical operation is any modification made on a web application without using the dedicated Back Office.

Regarding the modification of files directly via FTP: if your need is urgent, you **CAN** make the change yourself, however you **MUST** notify the technical staff afterwards (on the channel of the project, or on #developers).

## Drupal

If the issue is related to a Drupal application, the demand must be made on this [trello board](https://trello.com/b/0DuIl19x)
