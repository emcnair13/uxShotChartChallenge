# uxShotChartChallengeUX Design Challenge: 

A primary component of working as a Front End/Full Stack Engineer on the GRACE platform – the Media Technology team’s internal web application that lets users from around the company select, configure, and render 3D data visualizations in real-time – is translating design requirements from conversations with Creative and Production into a workable UX solution. 

To do this, we use React, Redux, and Socket.IO with Material UI to build pages/forms within the web application that request and parse data from external APIs, expose that data to producers as they identify what subset of data they need to render, and configure a render packet to send via WebSocket to 3D Unreal project. 
 
In this interview, your task is to talk through the process you would follow to design the user interface for rendering 3D Shot Charts with basketball data. You’ll need to identify what fields need to be exposed in the UI by talking to your client (in this case, me – I’ll double as a production user), describe the layout you would build with React (please feel free to sketch out your designs as we talk if it is part of your process), and discuss with the user what aspects of the Shot Chart UX request are unreasonable or impractical (e.g. if a requested feature is too specific for a generalized process, or otherwise impossible due to project limitations). 

Challenge: Please design a form in GRACE that will let us select shots per team and player (or all players) by date range or by game. The shots should be aggregated by region on the court (e.g. Paint, Non-Paint, 3-Point Shots, etc.). We need to show which shots were makes, and which were misses. We also need to know the distance from each shot to the net. We will provide you with API endpoint to request team, player, and shot information, along with pseudo-code helper functions: getShotRegion, getShotDistanceFromHoop, and getMakeMiss. It is your job to confirm that you have the necessary information about the shots to use these helper functions. Please ask any question you have about available data and design specifications. 

Point to consider as you outline your design: 

-	The GRACE web application processes script on both its client and server sides, and passes data back and forth between them. How would you divide your Shot Chart solution between the two? 

-	How would you break up the input fields and other UX elements between components? What elements do you think would be useful to designers building shot charts? 

-	React Redux allows us to share information between components in the application’s store, but we can also maintain component specific state variables. What information would you keep in the store, and what information would you keep in state variables? 

-	What question do you need to ask about information exposed in the data to ensure you’re able to generate a shot chart? 


The (mock) API endpoints you’ll be using to request data and to drive your UI are: 
-	Teams by League: https://grace.com/api/basketball/teams/leagueID=${leagueID}
-	Players by Team: https://grace.com/api/basketball/players/teamID=${teamID}
-	Shots by Date Range: https://grace.com/api/basketball/shots/teamID=${teamID}/playerID=${playerID}/startDate=${startDate}/endDate=${endDate}
-	Shot By Game: https://grace.com/api/basketball/shots/teamID=${teamID}/playerID=${playerID}/gameID=${gameID}


