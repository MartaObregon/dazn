# Watch Party data model (events)
## DAZN - Case Study

## Description
The new feature allows up to 4 DAZN customers to watch a sport event from the same “watch room”, which offers synchronized streaming and allows users to interact with each other through a live chat functionality as well as through camera and microphone. This feature is implemented to revolutionize the way users watch our content and make the streaming experience more fun and interactive, which should contribute to increased engagement and retention on the platform.






## Event Schema and samples

For a better understa

### Initiation of the Watch Party streaming through CTA click
|              |                   |  
| -------------| ------------------|
| event        | watchPartyStart   |
| category     | watch party       | 
| action       | start             |
| label        | {{itemId}}        | 




```json
{
    "event": "watchPartyStart",
    "watchParty": {
        "itemType": "article",
        "itemId": "17vb4ds80aga7916d0dc6gvbn",
        "itemName": "Abierto de Eastbourne | Día 2",
    },
    "playback": {
        "articleName": "AWS GP de Canadá | Carrera",
        "articleId": "n6rmhypv1xke1d9e4icohclab",
        "competitionId": "2slaywwom6tyirsmaukgu5mty",
        "competitionName": "Torneo de Eastbourne",
        "sportId": "4rheplujt9zryv3fqvtu1jpah",
        "sportname": "Tenis",
        "type": "live", 
        
    },
    "player": {
        "playbackSessionId": "1655736158523-1afc44bd767b-n6rmhypv1xke1d9e4icohclab-532bc9", 
         "liveEdge":true,
         "playerState":"start",
         "videoType": "watch party",
         
    },
    "application": {
        "type": "web.hybrid.2",
        "version": "9.13.0-hotfix.1.130",
        "device": {
            "platform": "web"
        }
    },
    "clientId": "007c53c0f6",
    "customerId": "1afc44bd767b",
    "User Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Safari/537.36",
    "gtm.uniqueEventId": 99
}
```


|              |                   |
| -------------| ------------------|
| event    | watchPartyJoined     |
| category     | watch party      | 
| action       | join|
| label        | {{watchRoomId}}        | 


```json
{
    "event": "watchPartyStart",
    "watchParty": {
        "itemType": "article",
        "itemId": "17vb4ds80aga7916d0dc6gvbn",
        "itemName": "Abierto de Eastbourne | Día 2",
        "watchRoomId": "23094yjhwkjh29343298n",
        "watchRoomName": "MuguruzaFANCLUB!!",
        "hostId": "1afc44bd767b",
        "guestIds": ["892731jbm", "9d92jd73"],
        "watchPartyStatus" : "started",
        "liveChatStarted" : false,
        
    },
    "playback": {
        "articleName": "Abierto de Eastbourne | Día 2",
        "articleId": "n6rmhypv1xke1d9e4icohclab",
        "competitionId": "2slaywwom6tyirsmaukgu5mty",
        "competitionName": "Torneo de Eastbourne",
        "sportId": "4rheplujt9zryv3fqvtu1jpah",
        "sportname": "Tenis",
        "type": "live", 
        
    },
    "player": {
        "playbackSessionId": "1655736158523-1afc44bd767b-n6rmhypv1xke1d9e4icohclab-532bc9", 
         "liveEdge":true,
         "playerState":"start",
         "videoType": "watch party",
         
    },
    "application": {
        "type": "web.hybrid.2",
        "version": "9.13.0-hotfix.1.130",
        "device": {
            "platform": "web"
        }
    },
    "clientId": "007c53c0f6",
    "customerId": "1afc44bd767b",
    "User Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Safari/537.36",
    "gtm.uniqueEventId": 102,
}
```

|              |                   |
| -------------| ------------------|
| event    | error            |
| category     | watch party error | 
| action       | modal error shown|
| label        | true              | 

|              |                   |
| -------------| ------------------|
| event    | error            |
| category     | watch party error | 
| action       | modal error closed|
| label        | true              | 

```json

{
    "event": "error",
    "error": {
        "category": "Watch Party Initialization Error",
        "code": "API_SERVICE_PLAYBACK_RESUMEPOINTS_UNAVAILABLE"
    },
        "playback": {
        "articleName": "Abierto de Eastbourne | Día 2",
        "articleId": "n6rmhypv1xke1d9e4icohclab",
        "competitionId": "2slaywwom6tyirsmaukgu5mty",
        "competitionName": "Torneo de Eastbourne",
        "sportId": "4rheplujt9zryv3fqvtu1jpah",
        "sportname": "Tenis",
        "type": "live", 
        
    },
    "player": {
        "playbackSessionId": "1655738645337-1afc44bd767b-n6rmhypv1xke1d9e4icohclab-ff723b"
    },
    "application": {
        "type": "web.hybrid.2",
        "version": "9.13.0-hotfix.1.130",
        "device": {
            "platform": "web"
        }
    },
    "clientId": "007c53c0f6",
    "customerId": "1afc44bd767b",
    "User Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Safari/537.36",
    "gtm.uniqueEventId": 34,
}
```


|   Event Parameters    |       Type        | Sample         |
| -------------    | ------------------|----------------|
| error          | Object            |   {}             |
| playback       | Object            |   {}             |
| player         | Object            |   {}             |
| application    | Object            |   {}             | 
| watchParty     | Object            |   {}             | 
| clientId       | String            | "07c53c0f6"    | 
| customerId       | String          | "1afc44bd767b" |
| User Agent      | String          | "Mozilla/5.0 (Windows NT 10.0; Win64; x64) " |

|Nested objects{}| Parameters         |  Type | Sample|
|--------------|-------------------|-------| -----|
|error        | category       | String| "Video Player Error" |
|       | code       | String| "API_SERVICE_PLAYBACK_RESUMEPOINTS_UNAVAILABLE" |
|playback      | articleName       | String| "AWS GP de Canadá | Carrera" |
|              | articleId         | String| "4ipwu1ze6b7a1az4ztflqyluw"|
|              | competitionId     | String| "6rqw7bnjivfrz93gae0lboea4"|
|              | competitionName     | String| "DAZN Linear"|
|              | sportId     | String| "11qbnjiv23frz93gae1234a4"|
|              | sportname     | String| "Motor"|
|              | type     | String| "vod"|
|player              | playbackSessionId | String| "1655716256365-1afc44bd767b-y44drrjcqtxa18g3arxjz58ge-e91811"|
|          | liveEdge | Boolean| true|
|          | playerState | String| "start"|
|          | videoType | String| "watch party"|
|application              | type | String| "web.hybrid.2"|
|                   | version | String| "9.13.0"|
|                   | device | object| {}|
|device                  | platform | String| "web"|
|                   | platform | String| "web"|
|watchParty         | itemId | String| "17vb4ds80aga7916d0dc6gvbn"|
|         | itemType | String| "article"|
|         | itemName | String| "Abierto de Eastbourne | Día 2"|
|         | watchRoomId | String| "1655716256365-1afc44bd767b-y44drrjc"|
|         | watchRoomName | String| "ForzaFerrari!!"|
|         | hostId | String| "07c53c0f6"|
|         | guestIds | Array| ["2233c0f6", "123450f6", "12346876p"]|
|         | watchPartyStatus | String| "started"|
|         | liveChatStarted | Boolean| true |




