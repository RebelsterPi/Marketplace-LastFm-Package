# LastFm Package
* Credentials: apiKey, secretKey

## How to get credentials: 
0. Create new API account [here](http://www.last.fm/api/account/create).
1. Copy and save your API key.

Use **API key**	as `apiKey` and **Shared secret** as `secretKey`.

## LastFm.tagAlbum
Tag an album using a list of user supplied tags.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| artist    | String     | The artist name.
| album     | String     | The album name
| tags      | String     | A comma delimited list of user supplied tags to apply to this album. Accepts a maximum of 10 tags.

## LastFm.getAlbumInfo
Get the metadata and tracklist for an album on Last.fm using the album name or a musicbrainz id.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name.
| album      | String     | The album name
| mbid       | String     | The musicbrainz id for the album
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| username   | String     | The username for the context of the request. If supplied, the user's playcount for this album is included in the response.
| lang       | String     | The language to return the biography in, expressed as an ISO 639 alpha-2 code.

## LastFm.getAlbumTags
Get the tags applied by an individual user to an album on Last.fm. To retrieve the list of top tags applied to an album by all users use album.getTopTags.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| album      | String     | The album name
| mbid       | String     | The musicbrainz id for the album
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| user       | String     | If called in non-authenticated mode you must specify the user to look up.

## LastFm.getTopAlbumTags
Get the top tags for an album on Last.fm, ordered by popularity.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| album      | String     | The album name
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| mbid       | String     | The musicbrainz id for the album

## LastFm.untagAlbum
Remove a user's tag from an album.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| artist    | String     | The artist name.
| album     | String     | The album name
| tag       | String     | A single user tag to remove from this album.

## LastFm.searchAlbum
Search for an album by name. Returns album matches sorted by relevance.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| album     | String     | The album name
| limit     | String     | The number of results to fetch per page. Defaults to 30.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.tagArtist
Tag an artist with one or more user supplied tags.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| artist    | String     | The artist name.
| tags      | String     | A comma delimited list of user supplied tags to apply to this artist. Accepts a maximum of 10 tags.

## LastFm.getArtistCorrection
Use the last.fm corrections data to check whether the supplied artist has a correction to a canonical artist

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| artist    | String     | The artist name to correct.

## LastFm.getArtistInfo
Get the metadata for an artist. Includes biography, truncated at 300 characters.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the artist
| lang       | String     | The language to return the biography in, expressed as an ISO 639 alpha-2 code.
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| username   | String     | The username for the context of the request. If supplied, the user's playcount for this artist is included in the response.

## LastFm.getSimilarArtists
Get all the artists similar to this artist.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| limit      | String     | Limit the number of similar artists returned
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| mbid       | String     | The musicbrainz id for the artist

## LastFm.getArtistTags
Get the tags applied by an individual user to an artist on Last.fm. If accessed as an authenticated service /and/ you don't supply a user parameter then this service will return tags for the authenticated user. To retrieve the list of top tags applied to an artist by all users use artist.getTopTags.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the artist
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.

## LastFm.getTopArtistAlbums
Get the top albums for an artist on Last.fm, ordered by popularity.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the artist
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| page       | String     | The page number to fetch. Defaults to first page.
| limit      | String     | The number of results to fetch per page. Defaults to 50.

## LastFm.getTopArtistTags
Get the top tags for an artist on Last.fm, ordered by popularity.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the artist
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.

## LastFm.getTopArtistTracks
Get the top trags for an artist on Last.fm, ordered by popularity.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the artist
| autocorrect| String     | Transform misspelled artist names into correct artist names, returning the correct version instead. The corrected artist name will be returned in the response.
| limit      | String     | The number of results to fetch per page. Defaults to 50.
| page       | String     | The page number to fetch. Defaults to first page.

## LastFm.untagArtist
Remove a user's tag from an artist.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| artist    | String     | The artist name.
| tag       | String     | A single user tag to remove from this artist.

## LastFm.searchArtist
Search for an artist by name. Returns artist matches sorted by relevance.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| artist    | String     | The artist name
| limit     | String     | The number of results to fetch per page. Defaults to 30.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getMobileSession
Create a web service session for a user. Used for authenticating a user when the password can be inputted by the user. Accepts email address as well, so please use the username supplied in the output. Only suitable for standalone mobile devices. See the authentication how-to for more. You must use HTTPS and POST in order to use this method.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| secretKey | credentials| A Last.fm shared secret key.
| username  | String     | The last.fm username or email address.
| password  | String     | The password in plain text.

## LastFm.getSession
Fetch a session key for a user. The third step in the authentication process. See the authentication how-to for more information.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| token     | String     | The authentication token received at your callback url as a GET variable.
| secretKey | credentials| A Last.fm shared secret key from dashboard.

## LastFm.getTopArtistsChart
Get the top artists chart

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| page      | String     | The page number to fetch. Defaults to first page.
| limit     | String     | The number of results to fetch per page. Defaults to 50.

## LastFm.getTopTagsChart
Get the top artists chart

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| page      | String     | The page number to fetch. Defaults to first page.
| limit     | String     | The number of results to fetch per page. Defaults to 50.

## LastFm.getTopTracksChart
Get the top tracks chart

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| page      | String     | The page number to fetch. Defaults to first page.
| limit     | String     | The number of results to fetch per page. Defaults to 50.

## LastFm.getTopArtistsByCountry
Get the most popular artists on Last.fm by country

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| country   | String     | A country name, as defined by the ISO 3166-1 country names standard
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getTopTracksByCountry
Get the most popular tracks on Last.fm last week by country

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| country   | String     | A country name, as defined by the ISO 3166-1 country names standard
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserArtists
A paginated list of all the artists in a user's library, with play counts and tag counts.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user whose library you want to fetch.
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number you wish to scan to.

## LastFm.getTagInfo
Get the metadata for a tag

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| lang      | String     | The language to return the wiki in, expressed as an ISO 639 alpha-2 code.

## LastFm.getSimilarTags
Search for tags similar to this one. Returns tags ranked by similarity, based on listening data.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name

## LastFm.getTagTopAlbums
Get the top albums tagged by this tag, ordered by tag count.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getTagTopArtists
Get the top artists tagged by this tag, ordered by tag count.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getTopTags
Fetches the top global tags on Last.fm, sorted by popularity (number of times used)

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getTopTagTracks
Get the top tracks tagged by this tag, ordered by tag count.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getWeeklyTagChartList
Get a list of available charts for this tag, expressed as date ranges which can be sent to the chart services.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| tag       | String     | The tag name
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.tagTrack
Tag an album using a list of user supplied tags.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| artist    | String     | The artist name.
| track     | String     | The track name
| tags      | String     | A comma delimited list of user supplied tags to apply to this album. Accepts a maximum of 10 tags.

## LastFm.getTrackCorrection
Use the last.fm corrections data to check whether the supplied track has a correction to a canonical track

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| artist    | String     | The artist name to correct.
| track     | String     | The track name to correct.

## LastFm.getTrackInfo
Get the metadata for a track on Last.fm using the artist/track name or a musicbrainz id.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| mbid       | String     | The musicbrainz id for the track
| track      | String     | The track name
| artist     | String     | The artist name
| username   | String     | The username for the context of the request. If supplied, the user's playcount for this track and whether they have loved the track is included in the response.
| autocorrect| String     | Transform misspelled artist and track names into correct artist and track names, returning the correct version instead. The corrected artist and track name will be returned in the response.

## LastFm.getSimilarTracks
Get the similar tracks for this track on Last.fm, based on listening data.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| track      | String     | The track name
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the track
| autocorrect| String     | Transform misspelled artist and track names into correct artist and track names, returning the correct version instead. The corrected artist and track name will be returned in the response.
| limit      | String     | Maximum number of similar tracks to return

## LastFm.getTrackTags
Get the tags applied by an individual user to a track on Last.fm. To retrieve the list of top tags applied to a track by all users use getTopTrackTags.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| track      | String     | The track name
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the track
| autocorrect| String     | Transform misspelled artist and track names into correct artist and track names, returning the correct version instead. The corrected artist and track name will be returned in the response.
| user       | String     | If called in non-authenticated mode you must specify the user to look up

## LastFm.getTopTrackTags
Get the top tags for this track on Last.fm, ordered by tag count. Supply either track & artist name or mbid.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| track      | String     | The track name
| artist     | String     | The artist name
| mbid       | String     | The musicbrainz id for the track
| autocorrect| String     | Transform misspelled artist and track names into correct artist and track names, returning the correct version instead. The corrected artist and track name will be returned in the response.

## LastFm.loveTrack
Love a track for a user profile.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| track     | String     | A track name (utf8 encoded)
| artist    | String     | An artist name (utf8 encoded)

## LastFm.untagTrack
Remove a user's tag from a track.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| track     | String     | A track name (utf8 encoded)
| artist    | String     | An artist name (utf8 encoded)
| tag       | String     | A single user tag to remove from this track.

## LastFm.scrobbleTracks
Scrobble a batch of tracks.

| Field           | Type       | Description
|-----------------|------------|----------
| apiKey          | credentials| A Last.fm API key.
| apiSecret       | credentials| A Last.fm API secret.
| scrobbleData    | Array      | Scrobble data.

#### `scrobbleData` field example:
```json
"scrobbleData": [{
	"artist": "Test artist",
	"track": "Test track",
	"timestamp": 1484833491
}, {
	"artist": "Test artist #2",
	"track": "Test track #2",
	"timestamp": 1484833500
}]
```

See ScrobbleItem object description in `scrobbleSingleTrack` method.

## LastFm.scrobbleSingleTrack
Scrobble a track.

| Field       | Type       | Description
|-------------|------------|----------
| apiKey      | credentials| A Last.fm API key.
| sessionKey  | String     | A session key generated by authenticating a user via the authentication protocol.
| artist      | String     | The artist name.
| track       | String     | The track name.
| timestamp   | String     | The time the track started playing, in UNIX timestamp format (integer number of seconds since 00:00:00, January 1st 1970 UTC). This must be in the UTC time zone.
| sessionKey  | String     | A session key generated by authenticating a user via the authentication protocol.
| album       | String     | The album name.
| context     | String     | Sub-client version (not public, only enabled for certain API keys)
| streamId    | String     | The stream id for this track received from the radio.getPlaylist service, if scrobbling Last.fm radio
| chosenByUser| String     | Set to 1 if the user chose this song, or 0 if the song was chosen by someone else (such as a radio station or recommendation service). Assumes 1 if not specified
| trackNumber | String     | The track number of the track on the album.
| mbid        | String     | The MusicBrainz Track ID.
| albumArtist | String     | The album artist - if this differs from the track artist.
| duration    | String     | The length of the track in seconds.

## LastFm.searchTracks
Search for a track by track name. Returns track matches sorted by relevance.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| track     | String     | The track name
| artist    | String     | Narrow your search by specifying an artist.
| limit     | String     | The number of results to fetch per page. Defaults to 30.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.unloveTrack
UnLove a track for a user profile.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| sessionKey| String     | A session key generated by authenticating a user via the authentication protocol.
| track     | String     | A track name (utf8 encoded)
| artist    | String     | An artist name (utf8 encoded)

## LastFm.updateNowPlayingTrack
Used to notify Last.fm that a user has started listening to a track. Parameter names are case sensitive.

| Field      | Type       | Description
|------------|------------|----------
| apiKey     | credentials| A Last.fm API key.
| artist     | String     | The artist name.
| track      | String     | The track name.
| sessionKey | String     | A session key generated by authenticating a user via the authentication protocol.
| album      | String     | The album name.
| context    | String     | Sub-client version (not public, only enabled for certain API keys)
| mbid       | String     | The MusicBrainz Track ID.
| albumArtist| String     | The album artist - if this differs from the track artist.
| duration   | String     | The length of the track in seconds.

## LastFm.getUserArtistTracks
Get a list of tracks by a given artist scrobbled by this user, including scrobble time. Can be limited to specific timeranges, defaults to all time.

| Field         | Type       | Description
|---------------|------------|----------
| apiKey        | credentials| A Last.fm API key.
| user          | String     | The last.fm username to fetch the recent tracks of.
| artist        | String     | The artist name you are interested in
| startTimestamp| String     | An unix timestamp to start at.
| page          | String     | The page number to fetch. Defaults to first page.
| endTimestamp  | String     | An unix timestamp to end at.

## LastFm.getUserFriends
Get a list of the user's friends on Last.fm.

| Field       | Type       | Description
|-------------|------------|----------
| apiKey      | credentials| A Last.fm API key.
| user        | String     | The last.fm username to fetch the friends of.
| recenttracks| String     | Whether or not to include information about friends' recent listening in the response.
| limit       | String     | The number of results to fetch per page. Defaults to 50.
| page        | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserInfo
Get information about a user profile.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user to fetch info for.

## LastFm.getUserLovedTracks
Get the last 50 tracks loved by a user.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user name to fetch the loved tracks for.
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserPersonalTags
Get the user's personal tags.

| Field          | Type       | Description
|----------------|------------|----------
| apiKey         | credentials| A Last.fm API key.
| user           | String     | The user who performed the taggings.
| tag            | String     | The tag you're interested in.
| taggingtype    | String     | The type of items which have been tagged. Valid values: `artist`, `album`, `track`.
| limit          | String     | The number of results to fetch per page. Defaults to 50.
| page           | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserRecentTracks
Get a list of the recent tracks listened to by this user. Also includes the currently playing track with the nowplaying=`true` attribute if the user is currently listening.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The last.fm username to fetch the recent tracks of.
| page      | String     | The page number to fetch. Defaults to first page.
| from      | String     | Beginning timestamp of a range - only display scrobbles after this time, in UNIX timestamp format (integer number of seconds since 00:00:00, January 1st 1970 UTC). This must be in the UTC time zone.
| extended  | String     | Includes extended data in each artist, and whether or not the user has loved each track. Valid values `0` or `1`.
| to        | String     | End timestamp of a range - only display scrobbles before this time, in UNIX timestamp format (integer number of seconds since 00:00:00, January 1st 1970 UTC). This must be in the UTC time zone.

## LastFm.getUserTopAlbums
Get the top albums listened to by a user. You can stipulate a time period. Sends the overall chart by default.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user name to fetch top albums for.
| period    | String     | overall | 7day | 1month | 3month | 6month | 12month - The time period over which to retrieve top albums for.
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserTopArtists
Get the top artists listened to by a user. You can stipulate a time period. Sends the overall chart by default.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user name to fetch top albums for.
| period    | String     | overall | 7day | 1month | 3month | 6month | 12month - The time period over which to retrieve top albums for.
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserTopTags
Get the top tags used by this user.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user name
| limit     | String     | Limit the number of tags returned

## LastFm.getUserTopTracks
Get the top tracks listened to by a user. You can stipulate a time period. Sends the overall chart by default.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The user name to fetch top tracks for.
| period    | String     | overall | 7day | 1month | 3month | 6month | 12month - The time period over which to retrieve top tracks for.
| limit     | String     | The number of results to fetch per page. Defaults to 50.
| page      | String     | The page number to fetch. Defaults to first page.

## LastFm.getUserWeeklyAlbumChart
Get an album chart for a user profile, for a given date range. If no date range is supplied, it will return the most recent album chart for this user.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The last.fm username to fetch the charts of.
| from      | String     | The date at which the chart should start from.
| to        | String     | The date at which the chart should end on.

## LastFm.getUserWeeklyArtistChart
Get an artist chart for a user profile, for a given date range. If no date range is supplied, it will return the most recent artist chart for this user.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The last.fm username to fetch the charts of.
| from      | String     | The date at which the chart should start from.
| to        | String     | The date at which the chart should end on.

## LastFm.getUserWeeklyChartList
Get a list of available charts for this user, expressed as date ranges which can be sent to the chart services.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The last.fm username to fetch the charts list for.

## LastFm.getUserWeeklyTrackChart
Get a track chart for a user profile, for a given date range. If no date range is supplied, it will return the most recent track chart for this user.

| Field     | Type       | Description
|-----------|------------|----------
| apiKey    | credentials| A Last.fm API key.
| user      | String     | The last.fm username to fetch the charts of.
| from      | String     | The date at which the chart should start from. See User.getWeeklyChartList for more.
| to        | String     | The date at which the chart should end on.

