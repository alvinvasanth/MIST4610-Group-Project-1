# MIST4610-Group-Project-1
Team Name: 29704 1

# Team Members
1. Jillian Bolgla 
2. Conor Dillon @cjdillon11
3. Brandon Hopper 
4. Neha Panchal @nehapanchal2001
5. Shrija Ramachandran Ganesh Mohan - [@shrija-27]([https://pages.github.com/](https://github.com/shrija-27))
6. [GitHub Pages](https://pages.github.com/)
7. Alvin Vasanthakumar - @alvinvasanth

# Problem Description
We are tasked with creating a relational database and data model for the owner of a football club. In our model the central entity is the Club. Each club has teams that operate in different divisions and in various locations. The club operates in conjunction with matches, training sessions, ticket sales, etc. that it offers to fans who support the teams.We want to accurately model these relationships, generating sample data, and populating entities and queries with the sample data. Additionally, we are planning on performing functioning queries on this data so that they can provide us with valuable player and coach statistics as well as the overall club performance. 



# Data Model

Explanation of the data model: 

The data model that was created is based on a theoretical football club. The Teams entity is a representation of all of the teams within the club (professional league, 16U, 12U, etc). Within the team, there are several players which are represented with one to many relationships between the Teams and Players entities. Hence, there are several players that belong to a single team. These players also have many stats as a result of the games they participate in. For example, their overall rating, number of goals scored, number of pass attempts, their position rating and so on. Therefore, this is represented with a one to many relationship between the Players and Stats entity. Additionally, Teams also have many coaches but a coach may only instruct one team at a time. For that reason, a one to many relationship between the Teams and Coaches entity was created.  

There are also many matches that a team may play and matches may be played by many teams, which is why there is a many to many relationship between Teams and Matches. As a result we created an associative entity labeled Matchup. This entity stores information when two teams are playing each other within a game. For example, the table allows users to see what teams are playing and the number of goals scored by both the team and opponent. Subsequently, matches require tickets for individuals to attend. A one to many relationship was placed between Matches and Tickets due to the fact that a match has several tickets for individuals to attend. 

There are also many training schedules that a team may have so we established an entity called TrainingSchedules. This is a one to many relationship between Teams and TrainingSchedules. 

On the other end of our data model we have the relationships between the Team and its corresponding fans and sponsors. The first relationship is one between Teams and Fans. This is a many to many relationship due to the fact that teams can have many fans supporting them and fans can support more than one team at a time. As a result, an associative entity was created labeled Fanbase, which stores information regarding who the fan is and what teams they support. Secondly, the relationship between Teams and Sponsors was created as a many to many relationship. Teams can have many sponsors while sponsors can sponsor several teams.  Therefore, another associative entity was created which stores information regarding the team and sponsor which was given the title Funding. 

Lastly, there is a Club entity created that represents the club associated with the respective teams. This entity, Club, stores information about the club name, description, and specific ID. There are 3 relationships associated with the Club entity. First, we created a one to many relationship with the Facilities entity since clubs can have access to several facilities. Secondly, a one to many relationship was created with the Transactions entity. A club can have several transactions such as rent, utilities, supplies, etc. Finally, the relationship between Club and Teams was created as a one to many relationship. There is one club, Georgia United FC, that houses all of the teams associated with the Club. However, a team may only belong to one club, Georgia United FC. 

![Screen Shot 2023-11-01 at 2 20 27 PM](https://github.com/alvinvasanth/MIST4610-Group-Project-1/assets/92402657/97ea47e2-1371-41b3-b8f0-f35bf5aae9ba)

# Data Dictionary 


# SQL Queries
