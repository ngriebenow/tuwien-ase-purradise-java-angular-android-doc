| Issue        | #7 |
| ------------ | -- |
| author       | Stefan Puntigam @11776838, Lisa Fürst @11775842 |
| released by  |  |
| release date | 2020-10-19 |


# The Project idea in detail

## Project domain

The project that is proposed here is intended to come up with software solutions that support the work of animal shelters. The outcome is not only meant to be of practical value for just one specific animal shelter but potentially for many different ones if they choose to deploy the system.
Specific to the domain of animal shelters are many tasks that revolve around the administration of informations about animals that are in an animal shelters care (e.g. age, vaccinations, observations made about its behavior, informations about its prior life). Also the administration of data about potential adopters (customers) is a task that lies within the application domain of the system developed.

Besides providing assistance with adminstrative tasks, the software will also directly provide utility to customers: The system will consider their wishes and necessities together with data about animals to come up with particularly fitting suggestions. Additionally, potential adopters will be presented with options to use augmented reality.

Implementation-wise, an Android App as well as a web interface will be made. The Android App will only provide functionality intended for customers. The web interface additionally will be useful for animal keepers that are working at an animal shelter. Both will be backed by a REST service.


## Solved problems

One of the central goals of animal shelters in general is to arrange adoptions of animals that are housed by them; it is one of the problems that the software developed in this project should help animal shelters to cope with. That is done by doing several things: Firstly, the system developed should help gain and keep the attention of potential adopters. We hope to achieve this by providing customers with a user interface that is similar to that of dating apps like Tinder. The selection of suggestions that users get is based on their own inputs. Therefore, customers should receive a higher rate of suggestions that harmonize with their wishes and limitations. Then, if an animal has been selected, it is possible to make use of augmented reality which should help to get the customer more involved in the process. Customers that prefer not to partake with this gimmick and want to use a more traditional interface can instead choose to use the web interface. That interface should also be useful for care takers: The system can serve as a kind of "single source of truth" in organizations that are to some extend run by volunteers that might only work there a few hours and otherwise lack a quick overview that the system could provide. A search interface might prove to be useful for many other reasons as well: Animal shelters might use it for planing how much of certain resource is needed or for writing schedules for keepers. Such a "single source of truth" can also provide useful data about a single animal, for example when a customer that is physically at the animal shelter shows interest in taking an animal for a walk or even adopting it.


## Improvements expected by this project

We expect to simplify both the workflow of keepers as well as the whole adoption process for customers. The staff may benefit from the application by having access to a system which is shared by all keepers in order to manage animal and customer information. Customers however profit by receiving tailored recommendations and may save time by being able to view potential new pets at any time and place. Additionally, being able to create and manage appointments with customers/keepers may help both keepers and customers with their time management and may reduce the number of people spontaneously dropping by the shelter, thus reducing the disappointment of customers in the case that there are no available keepers to show them around.

## Integration with existing Systems

The software will not be integrated with any systems that are out of the scope of the project other than commonly used software that is not specific to the domain, such as Android.


## Replacement of existing products

No. While there is the chance that animal shelters may already use software-aided management systems for keepers and customers, we could not find evidence that there are existing applications which support both keepers and customers at the same time. The product is therefore meant to provide a new solution for animal shelters. Similarities to existing systems are described in the Similar Products section.
