---
title: Model
position: 2
content_markdown: |-
  In traditional music organizing software which are based on ID3-like tags
  there are several design issues. I am not aware of software that doesn't have
  at least one of these issues:
  * Splitting a song into two parts, the artist and title.
    Consider "_Tchami – World To Me (feat. Luke James)_".
    The dash splits the parts and makes "_Luke James_" part of the song title.
  * Bad support for multiple artists: The program gets either of these wrong:
     * "_Case & Point – Savage_" is by one artist.
     * "_Tristam & Braken – Far Away_" is by two artists.
  * If multiple artists are supported, the _x_ delimiting the
    two artists in "Jauz x San Holo - OK!" gets lost because it is not that common
    (e.g. replaced by an ampersand)
  
  terorify fixes them by using a much simpler data model.
  There are currently 4 distinct data types:
  * Song: String with a title links to artists
  * Artist: String
  * Playlist: List of songs with a type (Album/EP/Compilation/…)
  * Resource: Bulk data associated with any of the other data types
    (Track files of a song, pictures of an artist, CD cover of a playlist…)
---