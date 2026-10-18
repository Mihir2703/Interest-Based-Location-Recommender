Project: Interest-Based Location Recommendation System

Overview
This project presents an Interest-Based Location Recommendation System that supports users in discovering suitable venues based on their preferences, historical check-in behavior, and geographic information. The system is implemented in Python and executed within a Jupyter Notebook environment.

The system provides the following core functionalities:
	• Venue recommendations based on category similarity and user history
	• Identification of users with similar check-in patterns
	• Recommendation of a common meeting venue for a group of users

Technical Environment
	Programming Language: Python
	Execution Environment: Jupyter Notebook
	Required Libraries:
	• pandas
	• numpy
	• scipy
	• scikit-learn
	• matplotlib
	• geopy

Usage Instructions
1. Running the Project
	• Open the Jupyter Notebook file included in the project.
	• Ensure that all required Python libraries are installed.
	• Execute all notebook cells to load the datasets and initialize the functions.

2. System Functionalities

2.1 Recommending Venues for a UserID & CategoryID
	Function: recommend_venue(checkIn, category)
	Description: Recommends venues based on a selected category and previous user check-ins.
	Input Parameters:
	 • checkIn: DataFrame containing user check-in history
	 • category: DataFrame containing venue category information

2.2 Finding Most Similar Users
	Function: find10mostSimUsers(checkIn)
	Description: Determines users with similar check-in behavior based on historical data.
	Input Parameters:
	• checkIn: DataFrame containing user check-in information
	• userID: Identifier of the target user
	• n_neighbors: Number of similar users to be returned
	Approach: Similarity is computed using KNN to compute nearest neighbors in high-dimensional space.

2.3 Group Meeting Venue Recommendation
	Function: common_nearest_venue(checkIn)
	Description: Identifies the venue that is geographically closest to all users within a group.
	Input Parameters:
	• checkIn: DataFrame containing geographic check-in data


Category Information
The project includes a category reference dataset that maps category identifiers to category names and labels. This dataset can be used to select valid categories when testing the recommendation functionality.