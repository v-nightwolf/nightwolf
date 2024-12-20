# TOP 50 Manual Testing interview questions

 We have consolidated a list of frequently asked Manual Testing and QA interview questions for Freshers and Experienced QA Engineers.
 You will find these questions very helpful in your interviews for Manual Testers or QA Engineer. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

 {!inpage-ads.md!}

---

1. What is Software Testing?

        * It is a process of analyzing s/w item to detect the differences between existing and required conditions
        and to evaluate the features of the s/w item.
        * It is a verification and validation process.
        * Process of demonstrating that errors are not present.

2. DIFFERENCE BETWEEN VERIFICATION AND VALIDATION?

        * Verification =>
          o It is a process of confirming whether the s/w meets it is requirement or not.
          o Process of examining/reviewing of work product.
          o Are we building the product right?
          o It is a QA activity.
          o It is a static process performed at compile time.
          o It is performed by a QA team or by developer.
          o Cost and time effective.
          o Activities involve in this is testing the application.

        * Validation =>
          o It is a process of confirming whether the s/w meets user  requirement or not.
          o Process of executing a product & examining how it behaves.
          o Are we building the right product?
          o It is a QC activity.
          o It is a dynamic process performed at run time.
          o It is performed by a QC team or by tester.
          o Cost and time taking.
          o Activities involve in this are inspections, reviews, walk-through.

3. DIFFERENCE BETWEEN QUALITY CONTROL AND QUALITY ASSURANCE?

        * QA =>
          o It ensures the prevention of defects in the process used to make s/w application.
          o It involves in process-oriented activities.
          o Aim to prevent defect.
          o Eg:- verification
          o It is the technique of managing the quality.
          o All team members are responsible for QA.
          o QA is responsible for SDLC.
          o It is a process to create the deliverables.

        * QC =>
          o It executes the program or code to identify the defects in the s/w application.
          o It involves in product-oriented activities.
          o Aim to identify and improve.
          o Eg:- validation
          o It is a method to verify the quality.
          o Testing team is responsible for QC.
          o QC is responsible for STLC.
          o It is a process to verify that deliverables.

4. WHAT IS SDLC?

        Ans. Software Development Life Cycle refers to all the activities that are performed during software
        development, including - requirement analysis, designing, implementation, testing, deployment and
        maintenance phases.


5. EXPLAIN STLC - Software Testing life cycle ?

        Software testing life cycle refers to all the activities performed during testing of a software product.
        The phases include =>

          o Requirement analyses and validation - In this phase the requirements documents are analysed and
            validated and scope of testing is defined.
          o Test planning - In this phase test plan strategy is defined, estimation of test effort is defined
            along with automation strategy and tool selection is done.
          o Test Design and analysis - In this phase test cases are designed, test data is prepared and automation
            scripts are implemented.
          o Test environment setup - A test environment closely simulating the real world environment is prepared.
          o Test execution - The test cases are prepared, bugs are reported and retested once resolved.
          o Test closure and reporting - A test closure report is prepared having the final test results summary,
            learning and test metrics.

6. WHAT IS DYNAMIC TESTING?

        It involves in the execution of code. It validates the output with the expected outcome.

7. WHAT IS STATIC TESTING?

        It involves in reviewing the documents to identify the defects in the early stages of SDLC.

8. WHAT IS WHITE BOX TESTING?

        o This also called as glass-box testing, clear-box and structural testing.
        o It is based on applications internal code structure.
        o In this, an internal perspective of the system, as well as programming skills are used to design test
          cases.
        o In white box testing, the tester analyses the internal architecture of the system as well as the quality
          of source code on different parameters like code optimization, code coverage, code reusability etc.
        o This testing usually was done at the unit level.


9. WHAT IS BLACK BOX TESTING?

        o It is a process of testing a system component considering input, output and general function.
        o The tester interact with the system through the interface providing input and validating the received
          output.
        o It does not require the knowledge of internal program structure.
        o In this we test UI & backend (coding/database).
        o External actions are performed.

10. WHAT IS POSITIVE AND NEGATIVE TESTING?

        Positive Testing => 
            o It is determine what system supposed to do.
            o It helps to check whether the application is justifying the requirements or not.

        Negative Testing =>
            o It is determine what system not supposed to do.
            o It helps to find the defects from the s/w.

11. WHAT IS GRAY BOX TESTING?

        It is a combination of both black box and white box testing. The tester who works on this type of testing
        needs to have access to design documents, this helps to create better test cases.

12. WHAT IS TEST STRATEGY?

        It is a high-level document and usually developed by project manager. It is a document which captures the
        approach on how we go about testing the product and achieve the goals.

13. WHAT IS TEST PLAN?

        It is a document which contains the plan for all the testing activities.

14. WHAT IS TEST SCENARIO?

        It gives the idea of what we have to test. Or testable part of an application is called TS. 

15. WHAT IS TEST CASE?

        It is a set of conditions under which tester determines whether an application/ software is working correctly
        or not.

16. WHAT IS TEST BED?

        An environment configured for testing is called test bed. It consist of hardware, s/w, network configuration.

17. WHAT IS TEST SUITE?

        Collection of test cases.

18. WHAT IS TEST DATA?

        It is a document that is basically used to test the s/w program. It is divided into 2 categories:- 
          a) +ve test data which is generally gives to system to generate the expected result. 
          b) –ve test data which is used to test the unhandled condition, unexpected, exceptional input condition.

19. WHAT IS DEFECT LIFE CYCLE?

        Defect Life Cycle or Bug Life Cycle is the specific set of states that a Bug goes through from discovery to
        defect fixation.

        Bug Life Cycle phases/status:- The number of states that a defect goes through varies from project to
        project. Below lifecycle diagram, covers all possible states =>

          o New: When a new defect is logged and posted for the first time. It is assigned a status as NEW.
          o Assigned: Once the bug is posted by the tester, the lead of the tester approves the bug and assigns the
            bug to the developer team.
          o Open: The developer starts analyzing and works on the defect fix.
          o Fixed: When a developer makes a necessary code change and verifies the change, he or she can make bug
            status as "Fixed."
          o Pending retest: after fixing the defect the developer gives a particular code for retesting the code to
            the tester. Here the testing is pending on the testers end, the status assigned is "pending request."
          o Retest: Tester does the retesting of the code at, to check whether the defect is fixed by the developer
            or not and changes the status to "Re-test."

          - Verified: The tester re-tests the bug after it got fixed by the developer. If there is no bug detected
            in the software, then the bug is fixed and the status assigned is "verified."
          - Reopen: If the bug persists even after the developer has fixed the bug, the tester changes the status
            to "reopened". Once again the bug goes through the life cycle.
          - Closed: If the bug is no longer exists then tester assigns the status "Closed."
          - Duplicate: If the defect is repeated twice or the defect corresponds to the same concept of the bug,
            the status is changed to "duplicate."
          - Rejected: If the developer feels the defect is not a genuine defect then it changes the defect to
            "rejected."
          - Deferred: If the present bug is not of a prime priority and if it is expected to get fixed in the next
            release, then status "Deferred" is assigned to such bugs.
          - Not a bug: If it does not affect the functionality of the application then the status assign to a bug
            is "Not a bug".


20. WHAT IS SMOKE AND SANITY TESTING?

        SMOKE =>

          o It is a kind of Software Testing performed after software build to ascertain that the critical
            functionalities of the program are working fine.
          o The purpose is to reject a badly broken application so that the QA team does not waste time installing
            and testing the software application.
          o In Smoke Testing, the test cases chose to cover the most important functionality or component of the
            system. The objective is not to perform exhaustive testing, but to verify that the critical
            functionalities of the system are working fine.

        SANITY =>

          o Sanity testing is a kind of Software Testing performed after receiving a software build, with minor
            changes in code, or functionality, to ascertain that the bugs have been fixed and no further issues
            are introduced due to these changes.

        #### Smoke Testing Vs Sanity Testing - Key Differences

      |Smoke Testing                                |      Sanity Testing                                                        |
      |---------------------------------------------|----------------------------------------------------------------------------|
      |Smoke Testing is performed to ascertain that the critical functionalities of the program is working fine| Sanity Testing is done to check the new functionality/bugs have been fixed|
      |The objective of this testing is to verify the "stability" of the system in order to proceed with more rigorous testing | The objective of the testing is to verify the "rationality" of the system in order to proceed with more rigorous testing |
      |This testing is performed by the developers or testers | Sanity testing is usually performed by testers|
      |Smoke testing is usually documented or scripted | Sanity testing is usually not documented and is unscripted|
      |Smoke testing is a subset of Acceptance testing | Sanity testing is a subset of Regression Testing|
      |Smoke testing exercises the entire system from end to end | Sanity testing exercises only the particular component of the entire system |
      |Smoke testing is like General Health Check Up | Sanity Testing is like specialized health check up |


21. WHAT IS EXIT AND ENTRY CRITERIA?

        ENTRY =>
            It describes when to start testing i.e. what we have to test it should be stable enough to test.
            Ex:- if we want to test home page, the SRS/BRS/FRS document & the test cases must be ready and it
             should be stable enough to test.

        EXIT =>
            It describes when to stop testing i.e. once everything mentioned below is fulfilled then s/w release
            is known as exit criteria:-
              a. Followed before actually releasing the s/w to client. Checking computer testing is done or not.
              b. Documents checking:- test matrix (RTM)/summary reports. 
                 SUSPENSION CRITERIA =>  when to stop testing temporarily.

22. WHAT IS BLOCKER?

        Ans. A blocker is a bug of high priority and high severity. It prevents or blocks testing of some other
        major portion of the application as well.

23. WHAT IS REGRESSION TESTING?

        To test whether the changed component has introduced any error to unchanged component or not is called as
        regression testing. It is perform on QA/production site depends.

24. WHAT IS RETESTING?

        To test whether the reported bug has been resolved by the developer team or not, is known as retesting.

25. MONKEY/AD-HOC TESTING?

        It is an informal testing performed without a planning or documentation and without having knowledge of
        the applications/software functionalities. Monkey testing is a type of testing that is performed randomly
        without any predefined test cases or test inputs.
 
26. SEVERITY AND PRIORITY?

        Priority =>
          o "How prior we need to fix the bug is priority."
          o It means the occurrences of defect.
          o Decide by developer team. Types(low, medium, high, critical) 

        SEVERITY =>
          o "How severe the bug is severity."
          o It means how bad the defect is and what impact it can cause in our application.
          o Decide by the testing team. Types(minor, medium, major)

27. What is defect priority?

        Ans. A defect priority is the urgency of the fixing the defect. Normally the defect priority is set on a
        scale of P0 to P3 with P0 defect having the most urgency to fix.

28. What is defect severity?

        Ans. Defect severity is the severity of the defect impacting the functionality. Based on the organisation,
        we can have different levels of defect severity ranging from minor to critical or show stopper.

29. Give an example of Low priority-Low severity, Low priority-High severity, High priority-Low severity, High priority-High severity defects.

        1. Low priority-Low severity - A spelling mistake in a page not frequently navigated by users.
        2. Low priority-High severity - Application crashing in some very corner case.
        3. High priority-Low severity - Slight change in logo color or spelling mistake in company name.
        4. High priority-High severity - Issue with login functionality

30. WHAT IS UNIT TESTING?

        It is also called as module testing /component testing.
        It is done to check whether the individual unit or module of the source code is working properly.
        It is done by the developer.

31. INTEGRATION TESTING?

        It is a process of testing the interface between the two s/w units.
        It is done by 3 ways:- big-bang , top-down, bottom-up approach.
        Process of combining & testing multiple components together.
        Normally done by developer but a tester can also perform if he has the knowledge of coding.

32. SYSTEM TESTING?

        It is a black box testing technique performed to evaluate the computer system. It include both functional
        and non-functional testing. Verifying the completed system to ensure that the application works as intended
        or not.
        "The behaviour of the system is tested as defined by the scope of the development project."
        Carried out by specialist tester/independent tester.

33. USER-ACCEPATANCE TESTING?

        User-requirement testing is done.
        Done by client as well as end user.
        It is a final stage of testing before used.

34. ALPHA-BETA TESTING?

        Alpha =>
          o Developer records all the issues.
          o Done by the end user at dev site. (involves client or tester+dev)

        Beta =>
          o Dev go through all the issues after specific period of time.
          o Done by the end user at the client site. (involves client/user)

35. HOW MONKEY TESTING IS DIFFERENT FROM ADHOC TESTING?

        In case of adhoc testing although there are no predefined or documented test cases still testers have the
        understanding of the application. While in case of monkey testing testers does not have any understanding
        of the application.

36. Explain Agile methodology?

        Agile methodology of software development is based on interative and incremental approach. In this model,
        the application is broken down into smaller build on which different cross functional team work together
        providing rapid delivery along with adapting to changing needs at the same time.

          o Working is done by individual person.
          o There is scrum master, who will be either tester/developer from the team or the person who has the
            knowledge of both testing and coding.
          o Responsibility of scrum master is to narrating the stories to both the team i.e. testing team and
            development team.
          o Scrum meetings can be happen in once a week or in 15 days or once a month. Most of the time client
            is included in scrum meeting.
          o Because of this meeting, if the one person is absent the another person from same team can complete
            his work. So project is not paused and dependency on one person is not happened. This is the main
            advantage of this model.
          o Sprint is dividing the project into modules and distributing these modules among both the team so
            that the team is working parallelly.
          o When to use:- when the project is big/medium and we have to deliver it as soon as possible then we
            will use this model. Quality is maintained.

37. What is scrum?

        A scrum is a process for implementing Agile methodology. In scrum, time is divided into sprints and on
        completion of sprints, a deliverable is shipped.  

38. What are the different roles in scrum?

        The different roles in scrum are -
            1. Product Owner - The product owner owns the whole development of the product, assign tasks to the
               team and act as an interface between the scrum team(development team) and the stakeholders.
            2. Scrum Master - The scrum master monitors that scrum rules get followed in the team and conducts
               scrum meeting.
            3. Scrum Team - A scrum team participate in the scrum meetings and perform the tasks assigned.

39. What is a scrum meeting?

        A scrum meeting is daily meeting in scrum process. This meeting is conducted by scrum master and update
        of previous day's work along with next day's task and context is defined in this meeting.

40. Explain TDD (Test Driven Development).

        Test Driven Development is a software development methodology in which the development of the software
        is driven by test cases created for the functionality to be implemented. In TDD, first the test cases
        are created and then code to pass the tests is written. Later the code is refactored as per the standards.


41. Explain equivalence class partitioning.

        Equivalence class partitioning is a specification based black box testing techniques. ECP means Grouping
        test data into equivalence classes with the assumpation that all the data items lying in the classes will
        have same effect on the application. In simple it means diving any module into equal parts and test each
        part separately.

        E.g. => 

        1 :- for testing a Square program(program that prints the square of a number- the equivalence classes
        can be => Set of Negative numbers, whole numbers, decimal numbers, set of large numbers etc.)

        2 :- suppose we have to test 1-100 no’s. So 1st we will divide this no into 5 equal parts. (Like 1-20,
        21-40,41-60,61-80,81-100). Now we will select random 3 values and multiply these values with the no of
        parts. Whatever the no will be, we will checked for that values from all the module in place of checking
        100 values.

        Purpose:- testing a complete module is exhaustive testing and time consuming thats why we use quivalence
        partioning as it is time saving.

42. What is boundary value analysis?

        Boundary value analysis is a software testing technique for designing test cases wherein the boundary
        values of the classes of the equivalence class partitioning are taken as input to the test cases.
        It is also called as a part of stress and -ve testing. e.g. if the test data lies in the range of
        0-100, the boundary value analysis will include test data - 0,1, 99, 100.


43. WHAT ARE SOME DEFECT REPORTING ATTRIBUTES?

        Ans. Some of the attributes of a Defect resport are => 

          - DefectId - A unique identifier of the defect.
          - Defect Summary - A one line summary of the defect, more like a defect title.
          - Defect Description - A detailed description of the defect.
          - Steps to reproduce - The steps to reproduce the defect.
          - Expected Result - The expected behaviour from which the application is deviating because of the defect.
          - Actual Result- The current erroneous state of the application w.r.t. the defect.
          - Defect Severity - Based on the criticality of the defect, this field can be set to minor, medium, major
            or show stopper.
          - Priority - Based on the urgency of the defect, this field can be set on a scale of P0 to P3.

44. What is stub?

        Ans. In case of top-down integration testing, many a times lower level modules are not developed while
        beginning testing/integration with top level modules. In those cases Stubs or dummy modules are used that
        simulate the working of modules by providing hardcoded or expected output based on the input values.

45. What is driver?

        Ans. In case of bottom-up integration testing, drivers are used to simulate the working of top level modules
        in order to test the related modules lower in the hierarchy.

46. What are some advantages of automation testing?

        Ans. Some advantages of automation testing are => 

          - Test execution using automation is fast and saves considerable amount of time.
          - Carefully written test scripts remove the chance of human error during testing.
          - Tests execution can be scheduled for nightly run using CI tools like Jenkins which can also be configured
            to provide daily test results to relevant stakeholders.
          - Automation testing is very less resource intensive. Once the tests are automated, test execution requires
            almost no time of QAs. Saving Qa bandwidth for other explratory tasks.

47. What are some disadvantages of automation testing?

        Ans. Some advantages of automation testing are => 

          - It requries skilled automation testing experts to write test scritps.
          - Additional effort to write scripts is required upfront.
          - Automation scripts are limited to verification of the tests that are coded. These tests may miss some
            error that is very glaring and easily identifiable to human(manual QA).
          - Even with some minor change in application, script updation and maintenance is required.

{!horizontal-ads.md!}

---
<br>

{!footer.md!}
