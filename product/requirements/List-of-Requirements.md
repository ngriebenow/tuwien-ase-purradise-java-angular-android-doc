| Issue |  #N |
| ----- | --- |
| author       | Stefan Puntigam @11776838 |
| released by  | |
| release date | 2020-10-DD |

# List of Requirements
The requirements are framed as user stories. Each of them describes expectations from the point of view of a particular stakeholder.

A overview of the User stories from the point of view of people who might adopt an animal

## S: Someone who might adopt an animal

### S1: Register as customer
As someone who might adopt an animal, I can register myself as customer using the web interface or the app so that I can access personalized contents.

### S2: List and filter available animals
As someone who might adopt an animal, I can use the web interface or the app to display a list of available animals. I want to be able to filter for qualities that I am interested in, such as species, age, sex or needs of the animal.

### S3: Details about animal
As someone who might adopt an animal, I can use the web interface or the app to display more detailed information about a specific animal I have found. Ideally, I want that to include images and a more detailed description.

### S4: Augmented reality
As someone who might adopt an animal, I can use the app to use augmented reality through which I can see a static 3D model of a specific animal in my own environment, captured by the camera of my phone.

### S5: Data retention policy
As someone who might adopt an animal, I want to be able to see the data retention policy.

### S6: General terms and conditions
As someone who might adopt an animal, I want to be able to see the general terms and conditions.


## U: Registered User

### U1: Authentication
As a registered user (i.e. a customer, keeper or administrator), I can log in so that I can use personalized contents. As a customer I can log in to the app or the web interface, as a keeper or administrator I can only log in to the web interface. When I am logged in I can log out of the system.

### U2: Change own password
As a registered user (i.e. a customer, keeper or administrator), I can change my password. As a keeper or administrator, I can only do that on the web interface, as a customer, I can also use the app.


## C: Customer

### C1: Voice preferences
As a customer, I can use the app to take a quiz about what kind of animal I would like to adopt so that the system would only present fitting recommendations.

### C2: Browse recommendations
As a customer, I can use the app to browse recommendations. If I have taken the quiz to, I want them to be based on preferences that I have voiced so that I can quickly find an animal that I might adopt.

I want my recommendations to be presented one by one in a fashion like on some dating apps present people (e.g. [Tinder](https://tinder.com)) where I would use gestures to express interest or lack thereof.

### C3: Watchlist
As a customer, I can use the app or the web interface to add animals that I might want to adopt to a list ("watchlist") so that I can easily find them later. I can also remove animals from that list. I want animals that are no more available to be marked as such.

### C4: Make appointment
As a customer, I can use the web interface or the app to schedule an appointment to discuss the adoption of any of the animals on my watchlist.

### C5: Adopted animals
As a customer, I can use the web interface or the app to display a list of animals that I have adopted so that I can easily access data saved about them in the system.

### C6: Delete customer account
As a customer, I can use the web interface or the app to delete my account so that data that is associated with me gets deleted as well.

### C7: Cancel appointments
As a customer, I can cancel an appointments I have made so that the animal keepers are informed that I will not appear.


## K: Keeper

### K1: Add animal
As a keeper, I can use the web interface to register animals so that anyone interested can retrieve information about them.

I want to save information that is of interest for people who are looking to adopt an animal or for other employees of the animal shelter. That includes images, data like the species, name, sex or age of the animal and a description.

Additionally, I want to assign a 3D model, so customers can take a look at the animal. I want to either upload a model of the animal that I have already created using third party software (e.g. [Autodesk](https://www.autodesk.com/solutions/3d-cad-software)), or select the closest fitting one among several predefined models. In that case, I also want to select a predefined coat color, so that customers still find interest in looking at 3D models.

### K2: Edit animal
As a keeper, I can use the web interface to change any of the information that is saved about a specific animal to reflect changes or include new knowledge.

### K3: Assign animal
As a keeper, I can use the web interface to assign an animal to a customer so that other users can know that it is no more available for adoption. The adopting customer should still have access to the information saved about the animal.

### K4: Remove animal
As a keeper, I can use the web interface to remove an animal from the system, even if it has not been adopted. That way, other users can know that it is no more available.

### K5: Manage appointments
As a keeper, I can use the web interface to manage when customers can make an appointment to discuss the adoption of an animal. I can view all upcoming appointments.


## Administrator

### A1: Register employees
As an administrator, I can use the web interface to register new animal keepers or administrators so that they can access functionalities that only employees have access to.

### A2: Delete employee account
As an administrator, I can use the web interface to delete the account of an animal keeper or administrator so that they can no more use functionalities that only those groups have access to. I want that their personal data is being removed.

### A3: Lock employee account
As an administrator, I can use the web interface to lock the account of any keeper or administrator other than myself, so that the employee concerned can not log in anymore. Likewise I can unlock locked employee accounts using the web interface.

### A4: Reset passwords
As an administrator, I can use the web interface to reset the password of any user, so that I can help users who lost access to their account.

### A5: Update data retention policy
As an administrator, I can use the web interface to change the contents of the data retention policy so that I can easily adapt them to (possibly changing) legal environments.

### A6: Update general terms and conditions
As an administrator, I can use the web interface to change the contents of the general terms and conditions so that I can easily adapt them to (possibly changing) legal environments.


## T: Techstories

### T1: Issue management
As team coordinator, I want that all the actions are tracked using an issue management system to facilitate keeping track of the progress of the project.

### T2: Risk management
As risk manager, I want that relevant risks get identified so that countermeasures can be taken.

### T3: Systematic testing
As testing manager, I want that core functionalities of the system are systematically tested so that the software produced complies with our quality standards.

### T4: Continuous integration
As testing manager, I want that continuous integration is being deployed so that incompatible or erroneous changes can quickly be identified as such.

### T5: Consistency in UI design
As UX manager, I want to maintain consistency in the design of the user interface. That includes consistently using a color scheme.

### T6: UI mockups
As UX manager, I want that mockups are being made for some more important parts of the user interface. That way issues with the user experience can be identified early on.

### T7: Security guidelines
As the security manager, I want that that common best practices are consistently applied to reduce security risks and render some more common attacks to not be possible.

### T8: Validation
As the security manager, I want that the correctness of parsing/validation of user data is subject to testing.

### T9: Text in English
As the quality manager, I want any text that is a result of the project to be written in English, including code, product and process documentation.

### T10: Coding guidelines
As the quality manager, I want all code to be in line with the coding guidelines to facilitate reasoning about the system and maintenance.

### T11: Git workflow
As the quality manager, I expect a clean git workflow that consistently satisfies our guidelines so that the course of actions can be retraced later on.

### T12: Build system
As the technical architect, I want that a build system is being used so that artifacts can more easily be generated.

### T13: Layered architecture
As the technical architect, I want the system to consist of cleanly separated layers to facilitate long-term maintainability.

### T14: Documentation guidelines
As the documentation manager, I want that documentation guidelines are applied to both product and process documentation to facilitate maintainability.

## Graphical overview

### Potential adopters
![A overview of the User stories from the point of view of people who might adopt an animal](uploads/d162ee7c6e16b189f751acb99f685f7c/customer.png)

[PlantUML source](uploads/29e7e5658ac85271ffabdc9c9a70d01c/customer.txt)

### Employees
![A overview of the User stories from the point of view of employees](uploads/d6e730722c07c88704659de8d09bba2c/employees.png)

[PlantUML source](uploads/8adc5d637c91fd5f5545a9530dce1213/employees.txt)

