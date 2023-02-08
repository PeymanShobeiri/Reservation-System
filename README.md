<h1 align="center" style="display: block; font-size: 3.5em; font-weight: bold; margin-block-start: 1em; margin-block-end: 1em;">

<br /><br /><strong>Reservation System</strong>

</h1>


## Introduction[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#introduction)

  

**Reservation System** was an academic project for Software Engineering course at university, in which a general reservation site with more than 50 use cases was modeled and analyzed.

  

  

## Table of contents[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#table-of-contents)

- [Introduction](#introduction)

- [Table of contents](#table-of-contents)

- [Requirements](#requirements)

- [About Reservation System](#software)

- [Usecase Diagrams](#Usecase-Diagrams)

- [Class Diagram](#logging-service)

- [User Interface](#development)

- [Interaction Diagrams](#development)

- [State Chart Diagrams](#development)

- [Activity Diagrams](#development)

- [Deployment Diagram](#development)

  

  

  

## Requirements[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#requirements)

  

In this project we used draw.io site and EdrawMax software in order to draw UML diagrams, so you required to download EdrawMax in order to see or alter the diagrams.

  

Note that the final PDF is available and you can see the project without installing anything.

  

  

## About Reservation System[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#software)

<img width="1230" alt="fig1" src="https://user-images.githubusercontent.com/87521998/217460349-8895d69a-2ee3-4272-ad5f-6c7f66aa9828.png">



#### Use case Diagrams: 
- Functional decomposition of the system into use cases and actors interacting with them (use cases represent the requirements of the customers)

- Results of constructing the use case model:
  - global use case diagram  
  - a detailed textual description for each use case
  

#### Use case Descriptions
Each use case description contains the following : 
-   Name and Short Description: Insert appointment  
    An appointment can be inserted for one or more participants by an authorized
    user, who does not need to be one of the participants. All participants must be notified of this new appointment. New appointments must be visualized immediately in all open calendars of the respective participants.
    
-    Precondition: User is known by the system.
    
-  Postcondition:
    
    - New appointment is inserted.
    
    -  All participants are notified either about the new appointment or that due to authorization problems it was not possible to change their calendar.
    
    -  All calendar views are updated.
    

-  Failure Situations: The user lacks proper authorization for every participant in order to insert the new appointment into their calendars.

-   Postcondition in case of failure:
    
    -  appointment could not be inserted.
    
    -  The calendars of all participants as well as their views haven„t been changed by the use case.
    
-    Actors: User (primary actor), E-Mail-System (secondary actor), Fax-System (secondary actor).
    
-   Trigger: -
    
-    Main Success Scenario:
	   - User identifies him/herself.
     - The details of the new appointment (time, location, duration, participants, etc.) are being recorded.
     -  User is authorized to insert the appointment for all participants. (4) appointment does not cause any collisions and is inserted.
     -  All participants (except the user in case (s)he is a participant too) are notified according to their preferred type of communication («include» notify participants)
     -  All currently open calendars of participants are updated. («include» update calendar)
    
- Extensions/Variations:  
  -  For at least one participant, the user is not authorized to insert a appointment.
  -  Each participant whose calendar could not be changed is notified about this authorization problem.
  -  All calendars of participants without authorization problems are updated, where proper authorization exists.


### Problem Domain Modeling
> Result of problem domain modeling is class diagram

#### Class Diagram
class diagram, visualizing the static structure of the system under development (“static structure diagram”)

<img width="1171" alt="fig2" src="https://user-images.githubusercontent.com/87521998/217464890-bbaa7c92-b527-494d-a714-c5f5a924adc7.png">

- Properties of attributes:
  - “/” attribute name: derived attribute
  -  {optional}: null values permitted

- Properties of operations: 
  - {query}: operation without side effects
  - {sequential}, {guarded}, {concurrent}: kind of concurrency 

- Visibilities:
  -  '+' : public  
  - '-' : private  
  - '#': protected

### Analysis Phase
* Models of the Analysis Phase

<img width="1192" alt="fig3" src="https://user-images.githubusercontent.com/87521998/217464538-6d46693b-9db9-4829-8a02-f8f9ed488617.png">


* Results of the Analysis Phase

<img width="1219" alt="fig4" src="https://user-images.githubusercontent.com/87521998/217464663-470e6c51-bb56-4ce5-8e24-6587545b7f40.png">

#### User Interface

  

#### Interaction Diagrams

  

#### State Chart Diagrams

  

#### Activity Diagrams

  

#### Deployment Diagram

  

<div align="right">[ <a href="#table-of-contents">↑ to top ↑</a> ]</div>

  
<br/>1 `star` == 1 `thank you`. By starring the project you thank the contributors for work.
<!-- markdownlint-enable -->
