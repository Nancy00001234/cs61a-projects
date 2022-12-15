# Yelp Maps  
This project creates a visualization of restaurant ratings on Google Maps using machine learning and the Yelp academic dataset. In this visualization, Berkeley's restaurants that are close to each other are grouped into clusters. The Berkeley campus is segmented into regions, where each region is shaded by the predicted rating of the closest restaurant (yellow is 5 stars, blue is 1 star).  Users with different preferences(e.g. a user who likes southside restaurants and another user who likes expensive restaurants) can have totally different visualizations.

## Description
Implement Yelp Maps visualization using:
- data abstractions
- the k-means clustering algorithm in supervised learning
- the least-squares linear regression in supervised learning

## Usage Example 
Clone or download (and unzip) the "maps" folder. Then go to the root and type in the Git Bash:
```
$ python3 recommend.py -u [USER] -k [NUMBER OF CLUSTERS] -p [-q RESTAURANT TYPE]
```
(If you are using Windows, please type in "Python" instead of "Python3".)  
        <br>
For instance, the following command visualizes all restaurants and their predicted ratings for the user who likes_expensive restaurants:
```
$ python3 recommend.py -u likes_expensive -k 3 -p
```
![all restaurants](https://user-images.githubusercontent.com/104662491/207767148-e7782f91-4d03-4095-ad4a-4c2a0d90cfd5.png)
The predicted rating of the closest restaurant would be displayed by placing your mouse over the corresponding region.

Sandwich restaurants can be selected out:
```
$ python3 recommend.py -u likes_expensive -k 3 -p -q Sandwiches
```
![image](https://user-images.githubusercontent.com/104662491/207765178-8f1bbfa8-70be-4a9f-8faa-98d727821670.png)


