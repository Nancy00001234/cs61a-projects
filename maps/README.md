# Yelp Maps  
This project creates a visualization of restaurant ratings on Google Maps using machine learning and the Yelp academic dataset. In this visualization, Berkeley's restaurants that are close in proximity are grouped into clusters. The Berkeley campus is segmented into regions, where each region is shaded by the predicted rating of the closest restaurant (yellow is 5 stars, blue is 1 star).  Users with different preferences (e.g. a user who likes southside restaurants and another user who likes expensive restaurants) can have a completely different visualization.  

.<img src="https://user-images.githubusercontent.com/104662491/207781143-bd1847dc-71bb-4af0-b90f-ce2adb841aa9.png" width="600" height="400" />

## Description
Implement Yelp Maps visualization using:
- data abstractions
- the k-means clustering algorithm in unsupervised learning
- the least-squares linear regression in supervised learning

## Usage Example 
Clone or download (and unzip) the "maps" folder. Then go to the root and type in the Git Bash:
```
$ python3 recommend.py -u [USER] -k [NUMBER OF CLUSTERS] -p [-q RESTAURANT TYPE]
```
(If you are using Windows, please type in "Python" instead of "Python3".)  
        <br>
For instance, the following command visualizes all restaurants and their predicted ratings for the user who `likes_expensive` restaurants:
```
$ python3 recommend.py -u likes_expensive -k 3 -p
```
.<img src="https://user-images.githubusercontent.com/104662491/207767148-e7782f91-4d03-4095-ad4a-4c2a0d90cfd5.png" width="600" height="500" />  
The predicted rating of the closest restaurant would be displayed if you hover your mouse over the corresponding region.

Sandwich restaurants can be filtered out specfically:
```
$ python3 recommend.py -u likes_expensive -k 3 -p -q Sandwiches
```
.<img src="https://user-images.githubusercontent.com/104662491/207765178-8f1bbfa8-70be-4a9f-8faa-98d727821670.png" width="600" height="400" />

## Directory
```
│  abstractions.py   // Data abstractions used in the project
│  recommend.py  // Machine learning algorithms and data processing
│  ucb.py   // Utility functions for CS 61A 
│  utils.py  // Utility functions for data processing  
│  
├─assets
│      least_squares.gif
│      
├─data  // A directory of Yelp users, restaurants, and reviews 
│  │  jsonl.py
│  │  restaurants.json
│  │  reviews.json
│  │  users.json
│  │  __init__.py
│  │  
│  └─__pycache__
│          jsonl.cpython-310.pyc
│          __init__.cpython-310.pyc
│          
├─tests
│      00.py
│      01.py
│      02.py
│      03.py
│      04.py
│      05.py
│      06.py
│      07.py
│      08.py
│      09.py
│      10.py
│      test_functions.py
│      __init__.py
│      
├─users  // A directory of user files
│      likes_everything.dat
│      likes_expensive.dat
│      likes_southside.dat
│      one_cluster.dat
│      test_user.dat
│      
├─visualize  // A directory of tools for drawing the final visualization
│  │  d3.js
│  │  voronoi.html
│  │  voronoi.js
│  │  voronoi.json
│  │  voronoi.png
│  │  __init__.py
│  │  
│  └─__pycache__
│          __init__.cpython-310.pyc
│          
└─__pycache__
        abstractions.cpython-310.pyc
        ucb.cpython-310.pyc
        utils.cpython-310.pyc
```        
        
