| Issue |  #33 |
| ----- | ---  |
| author       | Günter Windsperger @01302775 |
| released by  | Nicolas Griebenow @01617265  |
| release date | 2020-11-05         |

# Testing

Our application is divided into three different parts: angular front-end, java-backend and android mobile application.

### Test-Frameworks:

In our application we will use the following testing frameworks:

- **JUnit5** for unit tests regarding the java-backend and android mobile-app.
- Integration tests of the java-backend using the **Spring Test Context framework**.
- **Jest** for UI unit tests of the web-app
- **Protractor** for automated End-To-End UI tests for the web-app
- **Espresso** Test Framework for automated End-To-End UI tests of the android-app

Furthermore we are using the **JaCoCo** plugin for test-coverage of the java-backend. In combination with our CI-pipeline, the plugin will automatically generate coverage-reports of all unit and integration tests of the java-backend, which will be available as artifacts to download and optionally deployed to gitlab-pages.

For our test plan we are specifying a **lower barrier that should be always fulfilled**. Additionally, we will perform further testing if feasible and sensible. 
If automated tests are not feasible to create, a manual test should be performed, especially for the advanced AR-feature. Due to the complexity of this library, this feature must be tested in detail manually.

### Test-Plan:

**1.	Unit testing**  
Every essential functionality of a component should be tested with at least two tests (one positive and negative test) and further tests as it is sensible. 

**2.	Component testing**  
Every finished component should be tested in its entirety, at least every specified functionality should be covered with two tests (one positive and negative test). 

**3.	Integration testing**  
The integration of components should be tested with at least one integration test, testing the general interaction. 

**4.	End-To-End testing**  
The major UI interactions of web and android components should be tested.

**5.	Manual system testing**  
Before each deliverable there will be a full mandatory system test with a predefined test protocol.


  
#### Test-Protocol:
- [System test protocol-MUSTER](uploads/92686eb43264c1296d56ef6c5c85e5c8/Systemtest_VORLAGE.xlsx)
