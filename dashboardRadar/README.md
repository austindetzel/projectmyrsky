# Project Myrsky Dashboard Radar

Simple yet very useful, non interactive, weather radar dashboard.

Usage:

URL: https://projectmyrsky.com/dashboardRadar

Params:

debug=0 ; [optional] default setting is 0, will enable debug features such as more update information and memory information (will be improved in future releases)

service=0 ; [optional] default setting is 0. 0 = NOAA data source scrapped by 814server, gives faster updates but only available in US. 1 = Rainviewer, a highly rated source but often has a fair amount of delay between radar sweeps (covers Europe visit https://www.rainviewer.com/ for more coverage information)

locations=[] ; [required] a json string of all the locations and settings per location (see example jsons below)

JSON format:

lat: latitude of the location
lon: longitude of the location
zoom: how for to zoom in 1-12 1 being global and 12 being a street
time: how much time to spend at this point in seconds

Example JSON zooming in and out every 30 seconds:
[{"lat":42.110664, "lon":-80.070024, "zoom": 10, "time": 30}, {"lat":42.110664, "lon":-80.070024, "zoom": 10, "time": 30}]

Example JSON traveling from New York, to Miami, to London and Back
[{"lat":40.712776, "lon":-74.005974, "zoom": 5, "time": 10}, {"lat":25.761681, "lon":-80.191788, "zoom": 10, "time": 10}, {"lat":51.507351, "lon":-0.127758, "zoom": 7, "time": 10}]

Full Example URL:
https://projectmyrsky.com/dashboardRadar?debug=0&service=0&locations=[{"lat":42.110664,"lon":-80.070024,"zoom":10,"time":30},{"lat":42.110664,"lon":-80.070024,"zoom":10,"time":30}]

Please Note it is recommended to remove spaces in URLs
