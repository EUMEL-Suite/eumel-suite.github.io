
# EUMEL Dj

The EUMEL Dj is part of the EUMEL Suite. The EUMEL Dj is a media player with playlist and voting support. The desktop app shows the playlist and the chat mesages as a "party status". The project page can be found [here](https://github.com/EUMEL-Suite/EUMEL.Dj).


<a href='https://play.google.com/store/apps/details?id=de.eumel.dj.mobile&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1'><img alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png' width='250'/></a>


A preview of all binaries can be found on [Github](https://github.com/EUMEL-Suite/EUMEL.Dj/). [Download latest version](https://github.com/EUMEL-Suite/EUMEL.Dj/releases) in Github releases.




## EUMEL DJ Playlist Voting App (Mobile)

The mobile app uses a QR Code to connect to the application and get a token for communication. After login, the user can see the playlist, vote for songs (and remove a vote) and send messages to the server and other users. The settings page shows information about the user and the user can control the player, if s/he has admin access. 

Login requires a qr-code which is provided by the REST service backend or by the user interface. By default, the uri for the image is e.g. [https://localhost/api/Settings/Init](https://localhost/api/Settings/Init).

![](../Assets/djmobile_login.png?raw=true){:width="250px"}

The `Playlist` tab shows the current song, upcoming songs and previous songs. The votes for each song are counted and shown as well.

![](/Assets/djmobile_playlist.png?raw=true){:width="250px"}

The `Votes` tab shows the top 100 songs and allows a search for more songs. It shows, if the current user has voted for song. By pressing the heard, the song can be upvoted or the vote removed.

![](/Assets/djmobile_votes.png?raw=true){:width="250px"}

The `Chat` is a very simple mesage distribution service which shows all mesages from other user. The aim is showing some kind of public dashboard with comments.

![](/Assets/djmobile_chat.png?raw=true){:width="250px"}

## EUMEL DJ Desktop (Desktop)

The desktop app is the media player which manages the playlist, votes and chat messages. The user interface is still under development and only a alpha preview for testing the mobile app is available. Therefore no screenshots are available. The configuration file must be changes manually in `%localappdata%\Eumel Suite\Eumel.Dj.settings.json`.

## Data Privacy Statement

The EUMEL DJ is designed to work with the minimum of required personal data. Therefore the login name is anonymised and no messages are persistently stored anywhere. Device permissions and data is reduced to a minimum which is required to run the application. See [official data privacy statement](eumel-dj-privacy.md).


## Implementation Details

The technical documentation and implementation details can be found in a separate [marp](https://marpit.marp.app/)-based [presentation](eumel-dj-tech.html).

