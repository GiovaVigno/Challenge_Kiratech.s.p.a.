# To beginning with 
I have been doing this challenge following the instructions provided from: https://grafana.com/tutorials/grafana-fundamentals.

## First, setup
I had to setup a sample application, so I started with clone github.com/grafana/tutorial-environment repository,

![Setup](screenshots/1.Setup.png)

then started the sample application.

![Start a sample app](screenshots/2.Start_sample_app.png)

![Start_sample_application2](screenshots/3.Start_sample_application2.png)

I made sure the docker was working,

![Make sure the docker is working](screenshots/Docker.jpg)

I Ensured all services are up-and-running also the application (desktop).

![Docker_desktop](screenshots/5.Docker_desktop.png)

Lastly tried to the sample application on http://localhost:8081/,

![Try.localhost_8081](screenshots/6.Try.localhost_8081.png)
I added a like and voted it.
![Grafana News_add link](screenshots/7.Add_link.png)
![Added link and voted](screenshots/8.Voted.png)

## Second, Log in to Granafa 
I checked into docker and browsed to http://localhost:3000/,

![Browse to localhost3000](screenshots/9.Host3000.png)
![Login to Grafana](screenshots/10.LoginGrafana.png)

consequently I entered inside,

![Welcome to Grafana dashboard](screenshots/11.WelcomeGrafanadashboard.png)

## Third, metrics and data source

I visualized the metrics from Prometheus , however I needed to add it as a data source (into the corfiguration) in Grafana.

![Add Prometheus in the dashboard](screenshots/12.Prometheus.png)

After a few simple steps, I had to fill up the boxs.Then saved and tested.

![Filled up Url box](screenshots/13.Url_box.png)
![Save and Test](screenshots/14.Save&Test.png)

## Forth, explore metrics 
I uses Explore to create speficif queries to understand the metrics exposed. By the way in the side bar,I clicked the **Explore** bottom and in the **Query editor** wrote close the **Metrics** bottom, and change the time picker. 

![Explore the Query (tns)](screenshots/15.ExploreQuery(tns).png)

Hence, I Added the **rate** function to the query to visualize the rate of requests per second, and I saw the legend below the graph.

![Rate and Legend of the PromQL](screenshots/16.LegendPromQL.png)

Moreover I Added the **sum** function to the query to group time series by route,

![Sum to group time series](screenshots/17.sum_group.png)

I went back to the http://localhost:8081/ and generated some traffic, and I checked what happened in the last 5 minutes.

<img width="875" alt="Click the time picker, and select Last 5 minutes." src="https://user-images.githubusercontent.com/77804552/130475984-d883ee38-9bfd-48f3-9a8d-cfabf6f97725.png">

After that I tried to change the **group by** with another label like status_code and istance .

<img width="849" alt="Try other labels" src="https://user-images.githubusercontent.com/77804552/130477087-8ab0915f-6eb7-4410-99b3-0bfa6c851782.png">
<img width="889" alt="Try other labels again" src="https://user-images.githubusercontent.com/77804552/130477099-4a7652e6-e649-4a00-94be-e7bd76920f2b.png">

## Fifth, logging data source

I needed to add data source **Loki** to Grafana. Always in the configuration like earlier, but into the url box I filled up with http://loki:3100/.

<img width="884" alt="21 Logging(Loki)" src="https://user-images.githubusercontent.com/77804552/130477878-df725636-b65f-4f79-bb20-95205689d2c4.png">

## Sixth, Explore logs

In order to explore the logs, I had to use **Loki** date source. Thus In the **Query editor**, I entered,

<img width="929" alt="Explore your logs" src="https://user-images.githubusercontent.com/77804552/130478868-73a22400-8051-46fe-89f0-27f1b9d8ecb9.png">

and it displayed all logs within the log file of the sample application.

<img width="935" alt="23 Grafanadisplayalllogs" src="https://user-images.githubusercontent.com/77804552/130479253-e16efa1f-0f41-49dd-8b06-3fa13d7f7c69.png">



