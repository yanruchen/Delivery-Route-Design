# Delivery-Route-Design
I designed the most efficient delivery route base on the addresses of the customer. 
Google API is being used to create the best route.

One example:
![image](https://user-images.githubusercontent.com/36490909/167242869-3ebea71d-9568-4b7e-a02f-bda1643d344a.png)

Steps to reproduce:
1. Register Google API on [Google Cloud Platform](https://cloud.google.com/)
2. Copy api key and paste in the R code where it says `api <- "paste API key here"`
3. I have two csv files, one for address, the other for delivery schedule. The files are not included here for private reason, but you can swap with whatever location you are interested in.
4. If your source code does not include longitude and altitute, you will need to uncomment the R chunk with `geocoded <- df %>% mutate_geocode(Address)` this line of code generates the longitute and altitude, which are needed for the following plot.

Some possible modifications:
1. In get_googlemap, you can customize the basemap in [style](https://developers.google.com/maps/documentation/maps-static/styling#style-syntax)
2. In google_directions, you may specify the mode as driving, walking etc, and set up departure time. A good reference can be found [here](https://mran.microsoft.com/snapshot/2017-02-04/web/packages/googleway/googleway.pdf)
