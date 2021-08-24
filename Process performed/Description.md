# Challenge Grafana fundamentals 
I have been doing this challenge following the instructions provided from: *https://grafana.com/tutorials/grafana-fundamentals*.

## First, setup
  
I had to setup a sample application, so I started with clone *github.com/grafana/tutorial-environment* repository,

![Setup](screenshots/1.Setup.png)

then started the sample application.

![Start a sample app](screenshots/2.Start_sample_app.png)

![Start_sample_application2](screenshots/3.Start_sample_application2.png)

I made sure the docker was working,

<img width="738" alt="4 Docker" src="https://user-images.githubusercontent.com/77804552/130590255-089ac0de-df1e-4dad-98a6-9220b15fd089.png">
I Ensured all services are up-and-running also the application (desktop).

![Docker_desktop](screenshots/5.Docker_desktop.png)

Lastly tried to the sample application on *http://localhost:8081*,

![Try.localhost_8081](screenshots/6.Try.localhost_8081.png)
I added a like and voted it.
![Grafana News_add link](screenshots/7.Add_link.png)
![Added link and voted](screenshots/8.Voted.png)

## Second, Log in to Granafa
I checked into docker and browsed to *http://localhost:3000*,

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

I went back to the *http://localhost:8081/* and generated some traffic, and I checked what happened in the last 5 minutes.

<img width="875" alt="Click the time picker, and select Last 5 minutes." src="https://user-images.githubusercontent.com/77804552/130475984-d883ee38-9bfd-48f3-9a8d-cfabf6f97725.png">

After that I tried to change the **group by** with another label like status_code and istance .

<img width="849" alt="Try other labels" src="https://user-images.githubusercontent.com/77804552/130477087-8ab0915f-6eb7-4410-99b3-0bfa6c851782.png">
<img width="889" alt="Try other labels again" src="https://user-images.githubusercontent.com/77804552/130477099-4a7652e6-e649-4a00-94be-e7bd76920f2b.png">

## Fifth, logging data source 

I needed to add data source **Loki** to Grafana. Always in the configuration like earlier, but into the url box I filled up with *http://loki:3100/*.

<img width="884" alt="21 Logging(Loki)" src="https://user-images.githubusercontent.com/77804552/130477878-df725636-b65f-4f79-bb20-95205689d2c4.png">

<h5> Sixth, Explore logs </h5>

In order to explore the logs, I had to use **Loki** date source. Thus In the **Query editor**, I entered,

<img width="929" alt="Explore your logs" src="https://user-images.githubusercontent.com/77804552/130478868-73a22400-8051-46fe-89f0-27f1b9d8ecb9.png">

and it displayed all logs within the log file of the sample application.

<img width="935" alt="Grafana displays all logs" src="https://user-images.githubusercontent.com/77804552/130479253-e16efa1f-0f41-49dd-8b06-3fa13d7f7c69.png">

I clicked and dragged the bars to filter the logs by specific occurrences (like **error**).

![Filter the graph to explore](https://user-images.githubusercontent.com/77804552/130621718-ecab64e1-8b84-4cd1-9848-598041aad1a2.jpg)

For that reason, I generated an error and analyzed it. So I opened the application (*http://localhost:8081* again), and posted a new link **without a URL** (as in beginning but without URL),besides I went back and entered the query,

<img width="755" alt="25 Generate an error andCheck " src="https://user-images.githubusercontent.com/77804552/130623637-fce9171b-cbe2-461a-8b5c-26b2d2867e7c.png">

then I clicked on the log line for more information.

<img width="895" alt="Generate an error and Check 2" src="https://user-images.githubusercontent.com/77804552/130623991-76e87591-7b41-4e25-b9fa-cb18d70c94b2.png">

## Seventh, Build a dashboard
To build a dashboard which heps me with intuitive queries and metrics, I had to set the dashboard (in the **create** icon),

<img width="793" alt="Build a dashboard" src="https://user-images.githubusercontent.com/77804552/130625679-ab46a3d6-0b32-4494-bb2c-b8fabac2e127.png">

afterwards I filled up the **Query editor** with the previous query.

<img width="956" alt=" for Setting a Dashboard" src="https://user-images.githubusercontent.com/77804552/130626125-588d8fc1-7b51-4e01-9d39-69ede8cd4fd9.png">


