# Lightstreamer JMS Gateway Chat Demo Client for JavaScript #

This project includes a front-end example based on the Chat demo for Lighstreamer JMS gateway.

## Basic Chat Demo ##

The Basic Chat Demo implements an extremely simple chat application, where all the users connected to the page can exchange messages. Each message reports the originating IP address, together with the user-agent string of the originating client, instead of leveraging a nick name.<br>

Launch multiple instances of the demo, possibly on different machines, to appreciate the message broadcast capability.<br>

This page uses the <b>JMS JS Client API for Lightstreamer</b> on top of <b>JavaScript Client API for Lightstreamer</b> to handle the communications with Lightstreamer Server.<br>
Check out the sources for further explanations. 

# Deploy #

Before you can run the demo of this project some dependencies need to be solved:

-  Get the lightstreamer.js file from the [latest Lightstreamer distribution](http://www.lightstreamer.com/download) and put it in the root folder of this project.
-  Get the require.js file form [requirejs.org](http://requirejs.org/docs/download.html) and put it in the root folder of this project.
-  Get the lightstreamer-jms.js file from the [Lightstreamer JMS Gateway preview](http://www.lightstreamer.com/download) (please click the "From the Labs" section) and put it in the root folder of this project.

Now, you need to configure the index.html of this example by specifying the name of the data adapter you are going to use. By default the demo will look for the <b>HornetQ</b> data adapter, please refer to the related [Service project]() for more details on the choice of a JMS broker to be used. 
To set the data adapter name and the connection name look where the connection is created:

```js
  ConnectionFactory.createConnection(function(conn) {
    ...
    ...
    ...
  }, "http://localhost:8080/", "JMS", "HornetQ", // Change data adapter here
    ...
    ...
    ...
  });
```

To access the demo from a web browser copy it somewhere under you root webserver directory. You can also add it to the standard Lightstreamer demo pages under "LightstreamerHome/pages/demos" directory and access it as: <i>http://<your lightstreamer http address>/demos/StockListDemo_JMS/</i>.

You can also simply start by opening the index.html file with your browser.


# See Also #

## Lightstreamer back-end Service needed by these demo clients ##

* To be add: [Lightstreamer JMS Gateway Chat Demo Service]()

## Similar demo clients that may interest you ##

* [Lightstreamer JMS Gateway StockList Demo Client for JavaScript](https://github.com/Weswit/Lightstreamer-JMS-example-StockList-client-javascript)
* To be add: [Lightstreamer JMS Gateway Portfolio Demo Client for JavaScript]()
* [Lightstreamer StockList Demo Client for javascript](https://github.com/Weswit/Lightstreamer-example-StockList-client-javascript)

# Lightstreamer Compatibility Notes #

- Compatible with Lightstreamer JavaScript Client library version 6.0 or newer.
- Compatible with Lightstreamer JMS Gateway Adapter since version 1.0 or newer.