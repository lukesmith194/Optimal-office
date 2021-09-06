# Optimal-office

The main purpose of this project is to find the optimal place to set up a new office for a company that is based in the gaming industry. The data was downloaded from the foursquare API. [here] "https://api.foursquare.com/v2/venues/explore"


## Data
There were various conditions considered when choosing the correct place, the places were:
- Dublin, IE [53.33925763762811, -6.234433274297044]
- Manchester, GB [53.476555291009824, -2.245396280521493]
- Las Palmas, ES [28.139050810737494, -15.431441251599868]

The conditions were:
- Being close to a school or various activities for children, as 30% of the current workforce has children. 
- A Starbucks being close by, as many of the executives like Starbucks, as well as coffee being one the motor for many companies.
- Travel facilities also being close by. These include airport, train stations and tram services.
- Being close by to other developing companies to be able to share knowledge and also have a close eye on competitors.

As all the conditions don´t have the same value to the company, we used a weighing system depending on importanceto finally choose our correct destination.This weighing system was considered between 0-1 with the results being the following:

- Children’s Activities = 0.3/1
	- This is very important for both parties, company, and employee as it facilitates the people with children to be close to their children in case of emergency as well as it being easy for parents to get to work on time as the activities are usually on the way to work or very close by. This is important for the company for punctuality reasons as well as keeping their parenting employees happy. Only 0.3 out of 1 was considered due to only 30% of the employees having children, meaning it would not be applicable to all employees.
- Starbucks = 0.2/1
    - Coffee in general is considered a "necessity" nowadays for efficiency and effectiveness in the workplace as its caffeine contents are powerful and its well known that it better the output of workers. It wasn´t considered so important in this case, being given 0.2/1 on the bases that coffee can be found in most places, it doesn´t have to be Starbucks. Also, if efficiency is a key factor in the workplace, the best option would be to buy a good café machine with branded Starbucks coffee, this would keep the workers in the office as well as satisfy their caffeine needs!
- Close to other developing companies = 0.7/1
    - The external influence of other companies is always beneficial for competition as well as the possibility to share knowledge. Also, being in an area where your competitors are based is good for business, as if they are clients are not happy with the service of others, you will be easy to find! For these reasons as well as the mutual objective of bettering the sector, in our case as a games developer we have given it 0.7/1 in importance.
- Travel = 0.8/1
    - Travel is one of the most important factors when deciding in where to place our office. Its importance comes from the ease for employees to reach the workplace in many ways Also this will be an important factor for the higher ranked employees in the business, as usually, people in the sector must travel to different countries and different parts of the city for meetings, courses etc. Another of the benefits of having good transportation routes is that the workers arrive fresh and on time to work, bettering the work ethic and efficiency

## Conclusion:
The conclusion we have reached from this study is that Las Palmas seems to be the best place to set up our new business. We got to this conclusion by first doing a geo-query to find out the distance from the location choosen. The maximum distance chosen was around 6km. From here we have taken the closest 8 places from each condition set and then we calculated the mean of these distances. We have choosen 8 due to their being less data for some of the cities, making the evaluation more equal. We used our weighing system on the mean that was calculated to get the best place. This can all be found in the geoqueries notebook.



## Libraries:
-	Geopandas [here] (https://geopandas.org/docs.html)
-	PyMongo [here] (https://pymongo.readthedocs.io/en/stable/)
-	Pandas [here] (https://pandas.pydata.org/docs/)
-	Requests [here] (https://docs.python-requests.org/en/master/)
-	Json [here] (https://docs.python.org/3/library/json.html)

