
![Presentation](https://user-images.githubusercontent.com/77804552/130754445-ffb03b3b-553f-4a75-a693-3222b6fb5bab.gif)




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
I ensured all services are up-and-running also the application (desktop).

![Docker_desktop](screenshots/5.Docker_desktop.png)

Lastly I tried to the sample application on *http://localhost:8081*,

![Try.localhost_8081](screenshots/6.Try.localhost_8081.png)
I added a like and voted it.

![Grafana News_add link](screenshots/7.Add_link.png)
![Added link and voted](screenshots/8.Voted.png)

## Second, Log in to Grafana
I checked into docker and browsed to *http://localhost:3000*,

![Browse to localhost3000](screenshots/9.Host3000.png)
![Login to Grafana](screenshots/10.LoginGrafana.png)

consequently I entered inside,

![Welcome to Grafana dashboard](screenshots/11.WelcomeGrafanadashboard.png)

## Third, metrics and data source 

I visualized the metrics from Prometheus, however I needed to add it as a data source (into the corfiguration) in Grafana.

![Add Prometheus in the dashboard](screenshots/12.Prometheus.png)

After a few simple steps, I had to fill up the boxs.Then saved and tested.

![Filled up Url box](screenshots/13.Url_box.png)
![Save and Test](screenshots/14.Save&Test.png)

## Forth, explore metrics 
I uses Explore to create specific queries to understand the metrics exposed. Anyway in the side bar, I clicked the **Explore** bottom, in the **Query editor** wrote (close the **Metrics** bottom), and changed the _time picker_. 

![Explore the Query (tns)](screenshots/15.ExploreQuery(tns).png)

Hence, I added the **rate** function to the query to visualize the rate of requests per second, and I saw the legend below the graph.

![Rate and Legend of the PromQL](screenshots/16.LegendPromQL.png)

Moreover I Added the **sum** function to the query to group time series by route,

![Sum to group time series](screenshots/17.sum_group.png)

I went back to the *http://localhost:8081/* then generated some traffic, and I checked what happened in the last 5 minutes.

<img width="875" alt="Click the time picker, and select Last 5 minutes." src="https://user-images.githubusercontent.com/77804552/130475984-d883ee38-9bfd-48f3-9a8d-cfabf6f97725.png">

After that, I tried to change the **group by** with another label like status_code and istance .

<img width="849" alt="Try other labels" src="https://user-images.githubusercontent.com/77804552/130477087-8ab0915f-6eb7-4410-99b3-0bfa6c851782.png">
<img width="889" alt="Try other labels again" src="https://user-images.githubusercontent.com/77804552/130477099-4a7652e6-e649-4a00-94be-e7bd76920f2b.png">

## Fifth, logging data source 

I needed to add data source **Loki** to Grafana. Always in the configuration like earlier, but into the url box I filled up with *http://loki:3100/*.

<img width="884" alt="21 Logging(Loki)" src="https://user-images.githubusercontent.com/77804552/130477878-df725636-b65f-4f79-bb20-95205689d2c4.png">

## Sixth, Explore logs

In order to explore the logs, I had to use **Loki** date source. Thus In the **Query editor**, I entered,

<img width="929" alt="Explore your logs" src="https://user-images.githubusercontent.com/77804552/130478868-73a22400-8051-46fe-89f0-27f1b9d8ecb9.png">

and it displayed all logs within the log file of the sample application.

<img width="935" alt="Grafana displays all logs" src="https://user-images.githubusercontent.com/77804552/130479253-e16efa1f-0f41-49dd-8b06-3fa13d7f7c69.png">

I clicked and dragged the bars to filter the logs by specific occurrences (like **error**).

![Filter the graph to explore](https://user-images.githubusercontent.com/77804552/130621718-ecab64e1-8b84-4cd1-9848-598041aad1a2.jpg)

For that reason, I generated an error and analyzed it. So I opened the application (*http://localhost:8081* again), and posted a new link **without a URL** (as in beginning but without URL), besides I went back and entered the query,

<img width="755" alt="25 Generate an error andCheck " src="https://user-images.githubusercontent.com/77804552/130623637-fce9171b-cbe2-461a-8b5c-26b2d2867e7c.png">

then I clicked on the log line for more information.

<img width="895" alt="Generate an error and Check 2" src="https://user-images.githubusercontent.com/77804552/130623991-76e87591-7b41-4e25-b9fa-cb18d70c94b2.png">

## Seventh, Build a dashboard
To build a dashboard which helps me with intuitive queries and metrics, I had to set the dashboard (in the **create** icon),

<img width="793" alt="To Build a dashboard" src="https://user-images.githubusercontent.com/77804552/130625679-ab46a3d6-0b32-4494-bb2c-b8fabac2e127.png">

afterwards I filled up the **Query editor** with the previous query,

<img width="948" alt="Enter the previous Query" src="https://user-images.githubusercontent.com/77804552/130628837-ef5364d5-541a-4f95-8f92-f4c8eb779d05.png">

I renamed the Legend, the label of the graph and saved, in order to have my first panel.

<img width="956" alt="Setting the Dashboard" src="https://user-images.githubusercontent.com/77804552/130629046-da289edf-365f-4262-bf08-2273033a1fbc.png">

## Eighth, annotate events
It is often important note you some changes, obviously automatically is much better. In other words I needed to set the annotations to allow me to represent events in my dashboard. I was able to do by clicking into the graph,

<img width="762" alt="Manual Annotation" src="https://user-images.githubusercontent.com/77804552/130633042-fbc9f36a-0566-4b03-98f2-b1f9258186a8.png">

and in description I wrote and then saved.

<img width="769" alt=" Annotation done" src="https://user-images.githubusercontent.com/77804552/130633345-d3d828cf-478d-473c-9796-cb3d36093fe3.png">

However an interesting things is I was able to annotate a time interval (**region annotations**), by pressing *Ctrl*, then click and drag across the graph.

<img width="806" alt="the Region annotations" src="https://user-images.githubusercontent.com/77804552/130634017-4ce2988d-6d44-45b4-b99f-3fd335bee4f9.png">

Not only, for regularly occurring events this has to do automatically, so I had to use a querying annotations from data sources.
I made an annotation using the **loki**, I clicked **Dashboard settings** icon,

<img width="940" alt="Annotation with Loki" src="https://user-images.githubusercontent.com/77804552/130635538-559e8cde-db93-4edf-b63d-bba33ddba4aa.png">

then I setted it up (with **Loki**) and entered the query, in the end clicked **Add**.

<img width="694" alt="Annotation using Loki " src="https://user-images.githubusercontent.com/77804552/130636132-8429d9b1-8a90-4caa-9600-dddcd9f5071c.png">

Going back, the log lines returned a new type of annotation (this help you to correlate information from **Prometheus** and **Loki**).

<img width="555" alt="Check querying annotations" src="https://user-images.githubusercontent.com/77804552/130636533-bfff14f4-4b8d-4cee-9128-f7e4c8e89565.png">

## Nineth, Set up an alert

Alerts is made in two parts:
1. _Notification channel_ - How the alert is delivered;
1. _Alert rules_ - When the alert is triggered.

### 1. Configure a notification channel
I used **web hooks** to send alerts, especially to test them. Thus I browsed to *https://requestbin.com/*,

![Configure a channel ](https://user-images.githubusercontent.com/77804552/130639587-335fb94f-c930-4669-9fba-1535390957ea.jpg)

I created a Request Bin (**public bin**) and copied my **endpoint** URL.

<img width="931" alt="36 Myendpoint" src="https://user-images.githubusercontent.com/77804552/130640101-0c5f53dd-3f1b-458d-b8c0-9e9719fb4908.png">

Subsequently, I configured a notification channel for web hooks to send notification to my Request Bin.

![Notification channels set](https://user-images.githubusercontent.com/77804552/130640675-7e57b07a-06a7-40cd-81c9-c741c49c0a92.jpg)

<img width="854" alt="Click and Send to Test" src="https://user-images.githubusercontent.com/77804552/130641033-27393745-dca2-4787-966a-e7e8f8929908.png">

After that I browsed back to the request bin, and checked **POST/** entry, so that I saved.

<img width="953" alt="Check request bin" src="https://user-images.githubusercontent.com/77804552/130641837-d0a0fe37-2ffb-47ee-8ddf-034572493cfc.png">

### 2. Configure an alert rule

In addition, I had to set up an alert rule, so I went to **Dashboard** (Manage) and I took my previous panel (edit into it),

<img width="919" alt="Configure an alert rule" src="https://user-images.githubusercontent.com/77804552/130642277-a6ab91d2-8f55-433b-a1db-8185fc36cc14.png">

I cliked **Alert**, **Create Alert**, I put the parameters (like Evaluate every **5s**; **0m**; **conditions**),

<img width="869" alt="Configure an alert rule 2" src="https://user-images.githubusercontent.com/77804552/130642915-a57f27bb-a6f6-4f74-bd55-d42600a95988.png">

<img width="927" alt="Configure an alert rule 3" src="https://user-images.githubusercontent.com/77804552/130643254-c1b8e7bb-ae99-4722-964e-4aec190d8c85.png">

then I put where I wanted to receive the notifications.

<img width="739" alt="Insert where I want to sent" src="https://user-images.githubusercontent.com/77804552/130644261-08b724fa-a909-433e-81d5-ef6c1eef51a9.png">

After saving the dashboard, I entered a note to tell me what I did.  As a result (since I had an alert rule), I tried to generate some traffic to verify what was happening in the usually application (**http://localhost:8081/**), therefore I went back to check the dashboard and the Request Bin, particuarly if it was working.

<img width="620" alt="Check the alert" src="https://user-images.githubusercontent.com/77804552/130645250-97649b91-b71d-4111-b664-2ee3b6890871.png">

<img width="938" alt="46 Checkrequestbin" src="https://user-images.githubusercontent.com/77804552/130645521-6f5424a2-dd62-4c5e-8e44-53e0c6bc8f35.png">

### The last but not the least; pause an alert

Once I got an alert, I needed to pause it (to avoid continuous repetitions). For that reason I clicked **Alert Rules**,

<img width="847" alt="Pause an alert" src="https://user-images.githubusercontent.com/77804552/130660151-e59ebcaa-2767-4d15-8f81-da615033ea28.png">

then I found my previous alert in the list, and clicked **Pause**.

<img width="800" alt="Pause icon" src="https://user-images.githubusercontent.com/77804552/130660357-f83ee7c5-e6b1-4269-b327-76218230478e.png">

That’s it on … for now. To summarize, I covered how to use Grafana to set up a monitoring solution for some sample application.


   ![The end loading](https://user-images.githubusercontent.com/77804552/130759505-56f889ff-b582-4117-8861-53ad56bac34f.gif)




