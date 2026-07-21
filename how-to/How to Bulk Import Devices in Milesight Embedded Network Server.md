How to Bulk Import Devices in Milesight Embedded Network Server

<figure>
<img src="./images/media/image4.jpeg"
style="width:8.27431in;height:11.70625in"
alt="C:\Users\Iris\Desktop\完整word\word模板竖版_英文.jpgword模板竖版_英文" />
</figure>

# Description

Milesight LoRaWAN Gateway supports to download template and import
multiple devices conveniently.

This article describes how to bulk import devices in Milesight Embedded
Network Server. If you need to add single device, please refer to [How
to Connect LoRaWAN Nodes to Milesight
Gateway](http://support.milesight-iot.com/en/support/solutions/articles/73000514280).

# Requirement

- Milesight LoRaWAN Gateway

- LoRaWAN end-devices

# Configuration

1.Make sure there has been at least 1 application and profile
on **Network Server \> Applications** and **Network Server \>
Profiles**. Please refer to this article:  [How to Connect LoRaWAN Nodes
to Milesight
Gateway](http://support.milesight-iot.com/en/support/solutions/articles/73000514280).
In this article, we use **cloud** in the application,
and **ClassA-OTAA** in the profile.

2.Go to **Network Server \> Device**, click **Bulk Import** and download
the template.<img src="./images/media/image5.png"
style="width:5.76667in;height:1.79861in" alt="IMG_256" /><img src="./images/media/image6.png"
style="width:5.76458in;height:1.425in" alt="IMG_257" />

3.Fill in the information of device in template.csv. Attributes needed:\
If the **Join Type** is select as **OTAA**,\
input: name, description, deveui, deviceprofile,application,
payloadcodec,fport, appkey,timeout, isdefaultabp(leave FALSE).\
if **ABP**:\
input: name, description, deveui, deviceprofile,application,
payloadcodec,fport, timeout, isdefaultabp(If "isdefaultabp" is TRUE, you
do not need to fill in devaddr, appskey, and nwkskey. If "isdefaultabp"
is FALSE, you need to fill in devaddr, appskey, and nwkskey.)

<img src="./images/media/image7.png"
style="width:6.50556in;height:0.33681in" alt="IMG_256" />

4.Take WT201 as an example.

<img src="./images/media/image8.png"
style="width:6.05347in;height:0.40764in" alt="IMG_256" />

5.Click **Browse** to locate the .csv file and import
it.<img src="./images/media/image9.png"
style="width:5.76181in;height:1.34583in" alt="IMG_260" />

6.After bulk import is done successfully, you will see all the sensor
that you fill in the .CSV file.<img src="./images/media/image10.png"
style="width:6.30139in;height:3.12431in" alt="IMG_256" /><img src="./images/media/image11.png"
style="width:6.30764in;height:3.12778in" alt="IMG_256" />

 

**--END--**
