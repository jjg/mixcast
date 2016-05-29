#Mixcast

##Notes
Tracks are assembled into playlists.  Each playlist generates a podcast where each track is an episode.  Doing it this way avoid any need to process the audio files and it should be possible to implement the entire system in client-side code, so long as a suitable storage back-end is available.

Initial tests will be done with Dropbox but the goal is to make both the input and the output of the system to be generic and modular, allowing any source and destination to be used so long as they support the essential operations.

##Workflow
1.  Authenticate to Dropbox
2.  Get a list of music files
3.  Add files to a playlist
4.  Generate Podcast XML
5.  Upload Podcast XML to dropbox

##Open Questions
*  How should playlists be persisted for editing purposes?  Should we interpret the Podcast XML or store them in something purpose-specific?
*  Do Dropbox links generated with `/shares` expire?
*  Dropbox `/media` links look better, but expiration is a problem with the non-concatinated file approach

