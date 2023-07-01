# Metro_APP
If you are confused between two stations how to minimize your amount use this app

The provided code is written in C++ and contains a few functions and declarations. Let's go through them one by one:

int mindistance(float distance[], bool stat[]):

This function is used to find the index of the minimum distance value from the source node.
It takes an array of distances and a boolean array indicating the status (visited or not) of nodes.
It iterates through the distance array and checks for the minimum value that has not been visited.
It returns the index of the node with the minimum distance.

void dijkstra(float graph[25][25], int source, string stations[24]):
This function implements Dijkstra's algorithm to find the shortest path from a given source node to all other nodes in a weighted graph.
It takes a 2D array representing the graph, the source node, and an array of station names as input.
It initializes distance array and status array.
It iteratively selects the node with the minimum distance (using mindistance() function) and updates the distances of its adjacent nodes if a shorter path is found.
After the algorithm finishes, it prints the minimum number of stations from the source node to every other station, and allows the user to check the distance between the source and any other station.

int login():
This function handles the login functionality.
It prompts the user to enter a username and password.
It reads usernames and passwords from a file named "user_logins.txt" and compares them with the entered credentials.
If a match is found, it displays a success message and returns a flag indicating successful login.
If the username matches but the password doesn't, it prompts the user to re-enter the password until a match is found.
If no match is found, it displays an error message and returns a flag indicating failed login.

void signup():
This function handles the signup functionality.
It prompts the user to enter a username and password.
It checks if the entered username already exists in the "user_logins.txt" file.
If the username doesn't exist, it asks the user to re-enter the password for confirmation.
If the password matches the confirmation password, it appends the username and password to the file.
If the password doesn't match, it prompts the user to re-enter the password until a match is found.

int main():
This is the main function of the program.
It declares a 2D array representing the weighted graph.
It initializes the graph with distances between different stations.
It provides a menu for either login or signup.
If the login is successful, it calls the dijkstra() function to find the shortest paths from the selected source node to all other nodes.
If the signup is chosen, it calls the signup() function to create a new user account.
The main function acts as the entry point of the program, executing the desired functionality based on user input.


Overall, the code combines Dijkstra's algorithm for finding the shortest path in a weighted graph with login/signup functionality using file operations.
 
