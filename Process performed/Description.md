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

