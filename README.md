# adjust-subtitles

Adjust timings in a 'srt' subtitles file. Just a handy script in case
your subtitles aren't synchronised properly with the video.

## Usage

```
       adjust-subtitles [+-][time][smh]

       Reads an .srt file from STDIN and outputs content to STDOUT with
       times adjusted according to provided parameters.

       There is only ONE argument to this program. But this argument is to
       be of a specific format which denotes three things: (1) whether to
       advance or delay the subtitles (2) by how much (3) units of
       specified delay (whether seconds, minutes or hours).

       Where, 

         The prefix '+' or '-' denotes whether the subtitles must be
         delayed or advanced.

         The [time] number can be an integer or a decimal.

         The suffix [smh] can be one of 's', 'm' or 'h' for seconds, minutes or
         hours respectively.

       Example:
            cat file.srt | adjust-subtitles +12.02s

            To save this:

            cat file.srt | adjust-subtitles +1.5m >new.srt

```
