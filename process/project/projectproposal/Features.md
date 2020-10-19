| Issue | #8 |
| ----- | -- |
| author | Thomas Stoiber @11777755 |
| released by | Lisa Fürst @11775842 |
| release date | 2020-10-15 |

### Features

The main feature of the application is that a customer can adopt an animal from an animal shelter. This animal should be suited for him/her. The basic workflow (not complete) is illustrated here:

![image](uploads/5209944a98bfb004a641054fd4fbbdb6/image.png)

 * A customer can use the adoption services using the Web app in the browser or by downloading the Android app.
 * After a customer is logged in, he/she can set preferences in the system. These include but are not limited to type of animal, characteristics of the animals, interests of the person (active lifestyle, ...).
 * When the customer has set preferences, he/she gets to see recommended animals based on his/her preferences.
 * In the Android app, the customer navigates through the recommended animals by swiping left and right (like Tinder).
 * A customer can view animal details. This includes pictures, a description and the preferences of the animal (e.g. needs garden, very active, ...).
 * When using the Android app, the customer has the possibility to view a 3D model of the animal using Augmented Reality. However, this has the following prerequisite: The keeper has either (a) uploaded an individual 3D model (e.g. an .obj model) that they previously downloaded via websites (e.g. https://free3d.com/de/3d-models/tiere) or (b) created the model using 3rd party software, e.g. [Autodesk](https://www.autodesk.com/solutions/3d-cad-software). It is out of scope of this project to provide means for scanning or creating 3D models. In case of (a), the customer can see a 3D model of the actual animal. In case of (b), the customer sees a 3D model that does not truly represent the actual animal but resembles the actual animal.
 * The customer can add animals he/she is interested in to the watchlist or remove animals from the watchlist. When he/she is satisfied with the list, he/she can make an appointment at the animal shelter to adopt an animal.
 * The customer can also view all of his/her previously adopted animals in a list.
 * The keepers at the animal shelter can add new animals, edit existing ones and delete them from the system. Additionally, the keeper has two possibilities adding an 3D model:
    - (a): The keeper can upload an individual 3D model (e.g. an .obj model that they downloaded via websites or created using 3rd party software.
    - (b): The keeper can also select a 3D model of a selection of at least 5 predefined models that this software provides, e.g. a predefined model for a Siberian Husky. Additionally, the keeper can select one of predefined coat colors that this software also provides.
 * At an appointment, the keeper can assign an animal to a customer, so that the animal is no longer available for adoption.

Without being logged in, a person can:
 * Register to become a customer.
 * See and filter available animals.
 * View the animal details including pictures, descriptions, preferences and a 3D augmented reality model.

Additionally to the adoption, the system also needs administration:
 * Customers may change their password.
 * Customers may delete their account.
 * Customers may see the data retention policy.
 * Customers may see the general terms and conditions.
 * Keepers may change their password.
 * Administrators may lock and unlock users.
 * Administrators may create new keepers and administrators.
 * Administrators may reset passwords.
 * Administrators may update the data retention policy.
 * Administrators may update the general terms and conditions.

\[1\] [Features_working](uploads/3dc21e398e07a9cf8dd7771054e514e1/Features_working.png)