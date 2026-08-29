# GamingRoomSoftwareDesign


# CS 230 – The Gaming Room Software Design

## Briefly summarize The Gaming Room client and their software requirements. Who was the client? What type of software did they want you to design?

The client for this project was The Gaming Room. They already had an Android game called *Draw It or Lose It* and wanted to expand the application so that users could play it on multiple platforms. The goal was to redesign the game as a web-based application that could be accessed from Windows, macOS, Linux, Android, and iOS devices through a web browser.

The application needed to support multiple games, teams, and players. Each game could have one or more teams, and each team could contain multiple players. Game and team names needed to be unique, and games, teams, and players needed unique identifiers. The application also needed to maintain a single GameService instance to manage the games and prevent inconsistent game information.

## What did you do particularly well in developing this documentation?

I believe I did particularly well at connecting the client's requirements to specific software design decisions. Instead of only describing what the application needed to do, I considered how the requirements would affect the structure of the software, the operating platform, storage, memory, networking, and security.

I also compared Windows, Linux, macOS, and mobile platforms before recommending Linux for the server environment. This helped me understand that selecting a platform should be based on the requirements of the application rather than simply choosing the operating system I am most familiar with.

## What about the process of working through a design document did you find helpful when developing the code?

Working through the software design document helped me organize the requirements before making changes to the code. The UML diagram was especially useful because it showed the relationships between GameService, Game, Team, Player, and Entity.

Having the design established first made it easier to understand where inheritance and design patterns should be used. For example, creating Entity as a base class prevented the same `id` and `name` attributes from being repeated in Game, Team, and Player. The design document also made the purpose of the Singleton and Iterator patterns easier to understand before implementing them.

## If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

If I were to revise one part of the design document, I would expand the system architecture portion. I would create a more detailed architecture diagram showing how the browser clients, web server, application server, database, image storage, and network connections interact.

This would make the document easier for both developers and nontechnical stakeholders to understand. It would also provide a clearer picture of how the application could eventually be deployed in a real cloud environment and scaled as the number of users increases.

## How did you interpret the user's needs and implement them into your software design? Why is it so important to consider the user's needs when designing?

I interpreted the client's needs by translating each requirement into a technical design decision. Because The Gaming Room wanted the game available on several operating systems, I recommended a responsive browser-based client rather than maintaining separate native applications for each platform. The server maintains the important game logic and shared state so users receive consistent information regardless of the device they use.

The requirement for unique games, teams, and players was addressed by assigning identifiers and checking names before creating new objects. The Singleton pattern was used for GameService so that a single service manages the active games, while Iterator-based searches were used to locate existing objects and prevent duplicate names.

Considering user needs is important because the software ultimately exists to solve the client's problem. A technically impressive design would not be successful if it were too expensive, difficult to use, incompatible with the user's devices, or unable to satisfy the application's requirements.

## How did you approach designing software? What techniques or strategies would you use in the future to analyze and design a similar software application?

My approach was to begin by identifying the client's business and technical requirements and then break those requirements into smaller design problems. I used object-oriented programming principles, UML modeling, and established design patterns to determine how different parts of the application should interact. I also evaluated different operating platforms and considered scalability, storage, memory management, networking, security, cost, and maintainability before making a recommendation.

For future projects, I would continue beginning with requirements before writing the implementation. I would use UML diagrams and other architecture diagrams to visualize relationships between components, identify reusable classes, and look for design patterns only when they solve a specific problem. I would also consider scalability and security earlier in the design process and create prototypes or tests for the most important requirements before developing the entire application.
