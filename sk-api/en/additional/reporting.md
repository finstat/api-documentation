# Intelligent Reporting API 
This version of the FinStat API is used to request generated reports within the FinStat [Intelligent Reporting service.](https://www.finstat.sk/inteligentny-reporting)

## List of Topics 
Listing all the topics [`ReportingTopic`](#ReportingTopic), provided by the **Intelligent Reporting** service.  
> **Requested URL**: ```https://www.finstat.sk/api/getreportingtopics```<br />
> **Hash parameter**: reporting-topics

### Parameters 
[](../../../common/parameters/parameters-sk.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getreportingtopics?apikey=YourAPIKey&hash=af2214dd6e123923b19308a1ef02f5f75a2ed4f0c2ed8e7a477b6612fb18c4f5&StationId=YourStationID&StationName=Your+Station+Name`

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## Topic Output
Listing all stored reports [`ReportOutput`](#ReportOutput) from a specific reporting topic.
> **Note:** Reports older than retention period 90 days are automatically deleted.

The request requires the *topic* parameter. Its value is obtained through the [List of Topics request](#list-of-topics)
> **Requested URL**: ```https://www.finstat.sk/api/getreportinglist```<br />
> **Hash parameter**: reporting-list|*{topic}*

### Parameters
| Parameter | Description  |
| ----------- | ----------- |
| **topic**<br />*[mandatory]*| Reporting topic ID as listed in the list of topics |

[](../../../common/parameters/parameters-sk.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getreportinglist?topic=topic1&apikey=YourAPIKey&hash=bbcab20d6a0730a5fc4a3bcc87199e4a213dba6d330ed748c00bde4df58be45d&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en.md ':include')

## Download Report  
Download an **Excel(.xlsx)** file containing records that match your defined scenario.
Returns the data of the requested **.xlsx** file.

The request requires the *filename* parameter. Its value is obtained through the [Topic Output request](#topic-output)
> **Requested URL**: ```https://www.finstat.sk/api/getreportingoutput```<br />
> **Hash parameter**: *{filename}*
### Parameters
| Parameter | Description |
| ----------- | ----------- |
| **filename**<br />*[mandatory]*| Output identifier from the topic output |

[](../../../common/parameters/parameters-en.md ':include')

> **Example call:** ```https://www.finstat.sk/api/getreportingoutput?filename=topic1_file&apikey=YourAPIKey&hash=058683cd75e1486a0dc84fa59ea682c27a99ffd73518979e9a2afebb6694b49c&StationId=YourStationID&StationName=Your+Station+Name```

#### HTTP return error codes:
[](../../../common/http/errorcodes-en-file.md ':include')

[](../../../common/http/errorcodes-en.md ':include')

# Responses structures

[](../../../common/responses/reportingtopic-en.md ':include')

[](../../../common/responses/reportoutput-en.md ':include')

> **Note:** order of parameters can be different from list above

# Examples XML structures
[](../../../common/examples/reporting-topics.md ':include')

[](../../../common/examples/reporting-list.md ':include')