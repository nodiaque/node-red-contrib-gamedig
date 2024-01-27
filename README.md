# node-red-contrib-gamedig

Query for server information of most game/voice servers using Node-RED.

This package adds the node "Query Game Server" that uses the NPM package [GameDig](https://www.npmjs.com/package/gamedig) to query if a server is online or not and if so returns the data of the server.

You can pass the server type, host, and port on the input message or define them on the node (settings defined on the node will override msg values).

You can also specify manual GameDig options using `msg.options` as an input. This will override any other options. For example: you can set `msg.options.guildId` that is required for querying Discord servers.

Visit the [GameDig GitLab page](https://github.com/gamedig/node-gamedig) if you want more information about what this library parses and standardizes from the server response.

### Usage Examples
- #### Inserting query data into InfluxDB and using Grafana to view results
  ![Flow Preview](https://skylar.tech/content/images/2019/12/image-2.png)
  I created a post on my website about how to use this node to query gameservers and store the results in InfluxDB. I then give a dashboard in Grafana that can be used to display the data. Check it out here:
  https://skylar.tech/tracking-game-server-statistics-using-node-red-influxdb-and-grafana/

  This is a fork of skylar simply because I felt gamedig library wasn't getting updated fast enough


### License
This project is licensed under the MIT License. Check [here](LICENSE) for more information.
