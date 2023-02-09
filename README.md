# View historical messages/ last n messages in a topic on the Confluent Cloud UI

In the Confluent Cloud Console, you can use the Messages page to view the data being produced to a topic. Browse message data, seek to a specific offset or timestamp by partition, and select messages you want to download.

There is a full documentation on how to inspect mesages in a topic, produce message from UI, jump to specific messages based on offsets, timestamps and downloading messages.
Documentation link: https://docs.confluent.io/cloud/current/client-apps/topics/messages.html#use-the-message-browser-in-ccloud

By default, when "Messages" tab of topic is opened, it shows the messages in real-time which are being produced into the topic at that moment.
![image](https://user-images.githubusercontent.com/73946498/217837339-969d9331-4cc6-401d-b58d-4b1a55280558.png)

![image](https://user-images.githubusercontent.com/73946498/217837436-84cde332-f5c8-439c-b1d8-10ba875bcc06.png)


Sometimes, there is a need to check historical messages - such as last 'n' messages instead of a specific offset or timestamp.

A customer reached out as they wanted to see the messages that landed into DLQ topic. https://docs.confluent.io/cloud/current/connectors/dead-letter-queue.html#ccloud-dead-letter-queue

You can do this from the same console. here is the process.

## Step-1: Pause the live Stream
![image](https://user-images.githubusercontent.com/73946498/217837805-7f2f7237-3ef5-433c-96ed-c55c57619d83.png)

## Step-2: Use the 'Jump to offset' option on the top pane and enter a negative number and choose the parition.
For Eg: -10 to view last 10 messages.
![image](https://user-images.githubusercontent.com/73946498/217838290-a79675e0-9d0e-4bff-b80c-cd3d3da78e1a.png)


![image](https://user-images.githubusercontent.com/73946498/217838490-02fc4e49-1ba1-45bc-bddd-b5d324a78bfd.png)

There you go !!!
