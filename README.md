<h1 align="center" style="display: block; font-size: 3.5em; font-weight: bold; margin-block-start: 1em; margin-block-end: 1em;">

<br /><br /><strong>Reservation System</strong>

</h1>


## Introduction[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#introduction)

  

**Reservation System** was an academic project for Software Engineering course at university, in which a general reservation site with more than 50 use cases was modeled and analyzed.

  

  

## Table of contents[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#table-of-contents)

- [Introduction](#introduction)

- [Table of contents](#table-of-contents)

- [Requirements](#requirements)

- [Requirements Specification Phase](#software)
     - [Use Case Model](#logging-service)
       - [Use case Diagrams](#Usecase-Diagrams)
       - [Use case Descriptions](#Usecase-Diagrams)
       
     - [Problem Domain Model](#logging-service)
       - [Class Diagram](#logging-service)

     - [Interface Model](#logging-service)
       - [User Interface](#development)

- <a href="#analysis"> Analysis Phase </a>  
     - [Behavior Model](#logging-service)
       - [Interaction Diagrams](#development)
       - [State Chart Diagrams](#development)
       - [Activity Diagrams](#development)
       
- <a href="#design"> Design Phase </a> 
  - <a href="#development">Deployment Diagram </a>

  

  

  

## Requirements[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#requirements)

  

In this project we used draw.io site and EdrawMax software in order to draw UML diagrams, so you required to download EdrawMax in order to see or alter the diagrams.

  

Note that the final PDF is available and you can see the project without installing anything.

  

  

## Requirements Specification Phase[![](https://raw.githubusercontent.com/aregtech/areg-sdk/master/docs/img/pin.svg)](#software)

<img width="1230" alt="fig1" src="https://user-images.githubusercontent.com/87521998/217460349-8895d69a-2ee3-4272-ad5f-6c7f66aa9828.png">

### 1) Use Case Model

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


### 2) Problem Domain Model
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

### 3) Interface Model

#### User Interface
- Specification of the user interface for each use case / actor
  - not explicitly supported by UML

-  Specification of the internal interfaces  
   -  supported by UML in terms of interfaces
  
<h2 id='analysis'>Analysis Phase </h2>

* Models of the Analysis Phase

<img width="1192" alt="fig3" src="https://user-images.githubusercontent.com/87521998/217464538-6d46693b-9db9-4829-8a02-f8f9ed488617.png">


* Results of the Analysis Phase

<img width="1219" alt="fig4" src="https://user-images.githubusercontent.com/87521998/217464663-470e6c51-bb56-4ce5-8e24-6587545b7f40.png">


### 1) Behavior Model

#### Interaction Diagrams (Sequence and Collaboration Diagram)
 Both specify the same information, However, each emphasizes different aspects.

- sequence diagram is “temporally” - oriented
   -  shows graphically the order of messages
    - does not show how to get the receiver object  
    
 - collaboration diagram is “spatially” - oriented
    - shows the static and dynamic relationships between objects - the context aspect
     - the order of messages is expressed by means of decimal classification only
     -  time is no dimension on its own

  

#### State Chart Diagrams
- describes  
  - the life cycle of the instances of a class
  -  the execution of an operation on an instance of a class
  
- models
   -  the possible states of the instances of a class
   -  the possible transitions from one state to another one
   - the events firing transitions
   -  the operations (actions and activities) which are executed within states or during a transition
  

#### Activity Diagrams
- Describes a process
consisting of:
   -  actions and activities  
   -  control flow  
   -  input and output objects, object flow 
   - responsible objects
  
  
- Control flow
  - order of actions / activities
  -  represented by transition arrows
  - no events - as soon as execution of the predecessor is finished, execution of the successor is started
   - guards and (send-) actions are allowed

<h4 id='design'> Design Phase </h4> 
<h5 id="development">Deployment Diagram </h5>

- Shows the actual HW configuration consisting of
   - nodes (processors (default), I/O, ...) 
   -  SW-components  
   - processes  
   -  objects and of the communication channels between nodes

- Properties of nodes can be denoted by means of tagged values and/or stereotypes (e.g., capacity, reliability)
  
<br/>1 `star` == 1 `thank you`. By starring the project you thank the contributors for work.
<div align="right">[ <a href="#table-of-contents">↑ to top ↑</a> ]</div>

  

<!-- markdownlint-enable -->
