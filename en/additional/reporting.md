# API for Intelligent Reporting 
This version of the FinStat API is used to request generated reports within the FinStat [Intelligent Reporting service.](https://www.finstat.sk/inteligentny-reporting)

---
## List of Topics 
Listing all the topics provided by the **Intelligent Reporting** service.  
> **Requested URL**: ```https://www.finstat.sk/api/getreportingtopics```<br />
> **Hash parameter**: reporting-topics
### Parameters 
[](../parts/parameters.md ':include')


> **Example call:** ```https://www.finstat.sk/api/getreportingtopics?apikey=YourAPIKey&hash=af2214dd6e123923b19308a1ef02f5f75a2ed4f0c2ed8e7a477b6612fb18c4f5&StationId=YourStationID&StationName=Your+Station+Name```
### Response Description

The request returns a list of scopes, where each item has the following structure: 

| Parameter | Description  |
| ----------- | ----------- |
| **ID** | Topic identifier |
| **Name** | Full topic name |
| **Group** | Topic group |

#### HTTP return error codes:
[](../parts/httperrorcodes.md ':include')

### Example XML responseShape 
[](../../examples/reporting-topics.md ':include')

---

## Topic Output
Listing all stored reports from a specific reporting topic.
> **Note:** Reports older than retention period 90 days are automatically deleted.

The request requires the *topic* parameter. Its value is obtained through the [List of Topics request](#list-of-topics)
> **Requested URL**: ```https://www.finstat.sk/api/getreportinglist```<br />
> **Hash parameter**: reporting-list|*{topic}*
### Parameters
| Parameter | Description  |
| ----------- | ----------- |
| **topic**<br />*[mandatory]*| Reporting topic ID as listed in the list of topics |

[](../parts/parameters.md ':include')


> **Example call:** ```https://www.finstat.sk/api/getreportinglist?topic=topic1&apikey=YourAPIKey&hash=bbcab20d6a0730a5fc4a3bcc87199e4a213dba6d330ed748c00bde4df58be45d&StationId=YourStationID&StationName=Your+Station+Name```
### Response Description

The request returns a list of saved outputs for download.
Items have the following structure: 

| Parameter | Description |
| ----------- | ----------- |
| **FileName** | Output identifier |
| **Description** | Your description of the scenario |
| **Topic** | Full topic name |
| **Group** | Topic group |
| **Count** | Number of records in the output |
| **Date** | Generation date |

#### HTTP return error codes:
[](../parts/httperrorcodes.md ':include')

### Example XML responseShape 
[](../../examples/reporting-list.md ':include')

---

## Download Report  
Download an **Excel(.xlsx)** file containing records that match your defined scenario.

The request requires the *filename* parameter. Its value is obtained through the [Topic Output request](#topic-output)
> **Requested URL**: ```https://www.finstat.sk/api/getreportingoutput```<br />
> **Hash parameter**: *{filename}*
### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| Output identifier from the topic output |

[](../parts/parameters.md ':include')


> **Example call:** ```https://www.finstat.sk/api/getreportingoutput?filename=topic1_file&apikey=YourAPIKey&hash=058683cd75e1486a0dc84fa59ea682c27a99ffd73518979e9a2afebb6694b49c&StationId=YourStationID&StationName=Your+Station+Name```
### Response Description

The request returns the data of the requested **.xlsx** file.  

#### HTTP return error codes:
| Error Code| Description |
| ----------- | ----------- |
| **404**| Requested file was not found |

[](../parts/httperrorcodes.md ':include')
