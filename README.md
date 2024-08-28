# Test Class

## Introduction

In Salesforce, a test class is used to test the functionality of Apex classes and triggers. The purpose of writing a test class is to ensure that your code works as expected and that it meets the requirements of your business logic.

Test classes help you to catch errors before they occur in production, so it is crucial to write good test classes.

- It's important to note that Salesforce requires a minimum of 75% code coverage for all Apex classes and triggers.
- This means that at least 75% of the lines of code in your classes and triggers must be covered by test methods.

## Benefits of Test Classes in Salesforce

- **Ensuring code quality:** Test classes help to ensure that your code works as intended and meets the requirements of your business logic.
- **Catching errors early:** Test classes help to catch errors early in the development process before they reach production. This saves time and reduces the risk of costly errors that can impact business processes.
- **Meeting code coverage requirements:** Test classes are required in Salesforce to meet code coverage requirements.
- **Facilitating collaboration:** Test classes can help facilitate collaboration between developers and QA teams.
- **Facilitating code maintenance:** Test classes can help with code maintenance by providing a way to test changes made to existing code.

In summary, test classes are an essential part of the development process in Salesforce. They help to ensure code quality, catch errors early, meet code coverage requirements, facilitate collaboration, and facilitate code maintenance.

## Important Annotation of Test Class

- **@isTest** - If we use this annotation at the top of the Apex Class, then the class will act as a Test Class. If we use this annotation at the top of an Apex method, then the method will act as a Test method inside the Test class.
  
- **@testSetup** - This method always gets executed before any test method is executed. This method is used to prepare all the data that is required for the complete test class. We use it to create the common data that is required across all the test cases inside that test class.

- **Test.startTest() & Test.stopTest()** - These methods are very important as we will always test our code within these two methods. *These methods provide a fresh set of governor limits for the execution of our business logic.*

- **System.runAs()** - This annotation allows you to write code that runs as a different user than the one currently logged in.

- **@testVisible** - This annotation will be used in the class on top of the private variable or method to make that variable or method visible to Salesforce.

- **@isTest(SeeAllData=false) - RECOMMENDED** - If we use this annotation on top of the Apex Class or Test Class method, then you have to create the object that is being used in the complete process.

- **@isTest(SeeAllData=true) - NOT RECOMMENDED** - If we use this annotation on top of the Apex Class or Test Class, then the test class will use or read the data from Salesforce itself. This will start creating problems when you are trying to deploy the code to production.

