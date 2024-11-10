# StreamingData

## Architecture diagram:

![alt text](Architecture.drawio.png)

Project connects to YouTube API and listens to changes in selected videos' statistics. The architecture includes:
- Connection to YouTube's API via Google Cloud Platform. 
- Python code to control the streaming of data from YouTube's API and send it to Kafka for realtime streaming processing via KSQL. 
- KSQL listens to YouTube's videos' statistics and records the latest likes, views and comment counts and the new counts. 
- Based on code by Yusuf airscholar


- Missing the connection to external system, but the idea would be to connect the KSQL data to an external apps that lets the user know when a change in a YouTube statistic has been made (for example: new comment, new likes, new views).

