# Architecting for Testing

-   **Communication**: Software architecture establishes a common language between the developers of an app and other members of the team, like managers, QA testers, analysts and designers.
    
	
-   **Reusable abstraction**: Reusability saves time. Later in the chapter, you’ll see that you can reuse patterns within different parts of an app, across different apps as well as on other platforms. You’ll also see that you can use architecture patterns to kick-off new projects.
    
	
-   **Early design decisions**: When you create a new app, one of the first decisions is to decide on the architecture you’re going to use. These early design decisions are important because they’ll set constraints on your implementation, such as the way your classes will interact and their responsibilities. Early decisions will also organize your codebase a specific way and may even organize the members of your team. For example, on a given architecture, you may divide your team between people who only write domain classes and others who only write visually-related code.
    
	
-   **Better testing**: By using good architecture from the start or refactoring an existing one, you’ll enable the creation of tests that would otherwise be impossible or difficult to write. Also, migrating from an existing architecture to a better one — which is a difficult task, but not impossible — will enable you to migrate slower tests, such as UI or integration tests, to unit tests, which are faster.
    

To achieve a robust architecture, it’s important to know and understand **[[Design Patterns]]** and the **[[SOLID]] principles**.