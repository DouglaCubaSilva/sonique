# Uses Cases #

## ==Music Service==

#### US-101
 **Name:** Music playback
 **Description** Allow the User select and play one song
 **Actor(s):** User
 **Precondition:** User must be logged and have an active subscription (If it is a premium plan )
 **Main Flow:**
 > **1.** The user selects a song to play
 > **2.** The Frontend request the Playback Service to start playback
 > **3.** The Playback Service verifies the user's subscription with the Subscription Service.
 > **4.** If the subscription is valid, the service requests the song file from the Music Library Service.
 > **5.** The song is uploaded and streamed to the user.
 
 **Alternative Flow:** (User without Premium Subscription):
 > **1.** If the user has a free plan, there may be restrictions, such as ads or skip limits.
 > **2.** If the subscription is inactive, the system informs the user and offers the option to subscribe to a plan.

 **Business Rules:**
 > **1.** Free plan users can only listen in shuffle mode and with ads.
 > **2.** Premium users can select songs and skip as many times as they want.

 **Postconditions:**
 > **1.** The song starts playing.
 > **2.** The system records the user's playback history

#### US-102
 **Name:** Playlist Creation
 **Description:** Allows the user to create a custom playlist.
 **Actor(s):** User
 **Preconditions:** The user must be logged in.
 **Main Flow:**
 > **1.** The user accesses the playlists area and clicks on "Create New Playlist".
 > **2.** The frontend requests the Playlist Service to create the playlist.
 > **3.** The Playlist Service saves the new playlist in the database
 > **4.** The system confirms the creation of the playlist to the user.

 **Alternative Flow:**
 > **1.** If the playlist name already exists, the system can suggest an alternative name.

 **Business Rules:**
 > **1.** Each user can have a limited number of playlists (example: 10 on the free plan, unlimited on the premium plan).
 > **2.** The playlist name cannot be empty.

 **Postconditions:**
 > **1.** The playlist is created and appears in the user's list.

#### US-103
 **Name:** Add Music to Playlist
 **Description:** Allows the user to add a song to an existing playlist.
 **Actor(s):** User
 **Preconditions:** The user must be logged in and have at least one playlist created.
 **Main Flow:**
 > **1.** The user opens a playlist and chooses "Add Music".
 > **2.** The frontend sends the request to the Playlist Service.
 > **3.** The Playlist Service checks if the song is already in the playlist.
 > **4.** If it is not, it adds the song and confirms to the user.

 **Alternative Flow:**
 > **1.** If the song is already in the playlist, the system displays a message informing that it has already been added.

 **Business Rules:**
 > **1.** There cannot be duplicate songs in the same playlist.
 > **2.** The limit of songs per playlist may depend on the subscription plan.

 **Postconditions:**
 > **1.** The song is added to the playlist.