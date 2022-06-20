|              |                   |
| -------------| ------------------|
| event        | watchPartyStart   |
| category     | watch party       | 
| action       | start             |
| label        | {{itemId}}        | 

|              |                   |
| -------------| ------------------|
| event    | watchPartyJoined     |
| category     | watch party      | 
| action       | join|
| label        | {{watchRoomId}}        | 

|              |                   |
| -------------| ------------------|
| event    | error            |
| category     | watch party error | 
| action       | modal popup shown|
| label        | true              | 

|              |                   |
| -------------| ------------------|
| event    | error            |
| category     | watch party error | 
| action       | modal popup closed|
| label        | true              | 

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
|                   | platform | String| "web"|
|watchParty         | itemId | String| "17vb4ds80aga7916d0dc6gvbn"|
|         | itemType | String| "article"|
|         | itemName | String| "Abierto de Eastbourne | Día 2"|
|         | watchRoomId | String| "1655716256365-1afc44bd767b-y44drrjc"|
|         | watchRoomName | String| "ForzaFerrari!!"|
|         | hostId | String| "07c53c0f6"|
|         | guestIds | Array| ["2233c0f6", "123450f6", "12346876p"]|
|         | watchRoomStatus | String| "started"|
|         | liveChatStarted | Boolean| true |




