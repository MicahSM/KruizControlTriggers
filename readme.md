Fill out the Variables in the samplejovivariables.txt to your proper answers. You can rename the variables file to pretty much anything as long as you remember to include it in the fileTriggers.txt

Add whatever modules you want to use to the fileTriggers.txt in the Kruiz-Control-master folder.
SOME OF THE MODULES ARE DEPENDENT ON OTHER MODULES! I'll add more information in the readme over time to help make sure you know what's what.

Add sounds you want into the sounds folder (.wav, .mp3,, .ogg only please. .ogg seems to run poorly though)

I strongly recommend using Kruiz-Control-Configurator, if nothing else, to keep your Kruiz Control up to date.

<hr>


<h2>Changing Backgrounds</h2>
<h6>file: backgrounds.txt</h6> <h6>Dependencies: None</h6><br>


  If you have a scene with multiple backgrounds, this module will allow you to randomly pick them using a chat Command,, as a Channel Point reward! It does require setting up the list in chat, using the !bgadd command.

<table>
  <tr>
    <th>Command</th>
    <th>Permissions</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>!bgadd [background name] </td>
    <td>Broadcaster</td>
    <td>This adds [background name] as a source that can be chosen for a random background.</td>
  </tr>
  <tr>
    <td>!bgremove [background name]</td>
    <td>Broadcaster</td>
    <td>This removes [background name] from the backgrounds list.</td>
  </tr>
  <tr>
    <td>!bgclear</td>
    <td>Broadcaster</td>
    <td>This entirely clears the backgrounds list.</td>
  </tr>
  <tr>
    <td>!backgrounds</td>
    <td>Everyone</td>
    <td>15 Second Cooldown. This Command shows the list of all backgrounds.</td>
  </tr>
  <tr>
    <td>!currentBG, !BGCurrent</td>
    <td>Everyone</td>
    <td>15 Second Cooldown. Sends the Current Background name to chat.</td>
  </tr>
  <tr>
    <td>!changebg [background name], !bgset [background name]</td>
    <td>Broadcaster, Moderator, VIP</td>
    <td>Sets the current background to [background name].</td>
  </tr>
  <tr>
    <td>!randomBG, !bgrandom</td>
    <td>Broadcaster</td>
    <td>Sets the Background to a random Background.</td>
  </tr>
</table>

<table>
  <tr>
    <th>Channel Point Rewards</th>
    <th>Options</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>Pick BG</td>
    <td>[Background Name]</td>
    <td>Changes the Background to whatever background is in the Message.</td>
  </tr>
  <tr>
    <td>Random BG</td>
    <td>None</td>
    <td>Randomly Selects a Background</td>
  </tr>
</table>

<hr>

<h2>Stream Elements Points Management</h2>
<h6>file: bankofjovine.txt</h6> <h6>Dependencies: streamelements.txt</h6><br>

  I personally have 2 points systems, so I can have 1 that I have more direct control over. This allows people to get a bonus for that secondary point system once a day. (I use Twitch points and Stream Elements points)

<hr>

<h2>Rolling Dice</h2>
<h6>file: dice.txt</h6> <h6>Dependencies: None</h6><br>

<table>
  <tr>
    <th>Command</th>
    <th>Permissions</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>!roll [die count]d[die size]</td>
    <td>Everyone</td>
    <td>This rolls multiple dice and adds them together. [die count] is the number of dice rolled, and [die size] is the size of the die. <br>ex: !roll 1d20</td>
  </tr>
  <tr>
    <td>!rollsplit [die count]d[die size]</td>
    <td>Everyone</td>
    <td>This rolls multiple dice and displays them individually. [die count] is the number of dice rolled, [die size] is the size of the die. <br>ex: !roll 3d10</td>
  </tr>
</table>

<hr>

<h2>Sound Effects on Entry</h2>
<h6>file: entrysounds.txt</h6> <h6>Dependencies: SFX.txt</h6><br>

  Plays a sound from the sounds folder upon the first chat of specific chatters. This does require a bit of diving into the variable setup.

  The Variables for this are broken down like this:<br>
    <code>list add [username]Enter "[filename]"</code><br>
  [username] is the username checked on entry.
  [filename] is the name of the file to play that the Sound Effect is. NO FILE EXTENSION.

<hr>

<h2>Music Player</h2>
<h6>file: jukebox.txt</h6> <h6>Dependencies: None</h6><br>

  Allows for music to be played in a seperate Kruiz Control thread. Dependency for music based modules. Does nothing on it's own.

<hr>

<h2>Media Controller</h2>
<h6>file: mediacontrols.txt</h6> <h6>Dependencies: None</h6><br>

  Uses strm.tool to allow mods to play/pause my music, and skipping of music with channel points. Requires some setup with Crash Koek's strm.tools, filling out the strmtool variables.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!playmusic, !pausemusic</td>
      <td>Broadcaster, Moderator, VIP</td>
      <td>This command pauses/plays the music.</td>
    </tr>
  </table>

  <table>
    <tr>
      <th>Channel Point Redemption</th>
      <th>Options</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>Media Controls</td>
      <td>skip, back</td>
      <td>Channel Point redemption that Skips, Goes Back a song based on the filled out message.</td>
    </tr>
  </table>

<hr>

<h2>Miscellanous</h2>
<h6>file: misc.txt </h6> <h6>Dependencies: None</h6><br>

  This is really a catch all for my random stuff. Right now it makes monika dab on my screen, and has commands to show off your FFZ/BTTV emotes.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!bttvEmotes</td>
      <td>Everyone</td>
      <td>60 Second Cooldown. Posts all your BTTV Emotes in Chat.</td>
    </tr>
    <tr>
      <td>!ffzEmotes</td>
      <td>Everyone</td>
      <td>60 Second Cooldown. Posts all your FFZ Emotes in Chat.</td>
    </tr>
    <tr>
      <td>!latestvideo</td>
      <td>Everyone</td>
      <td>60 Second Cooldown. Posts a link to your most recent video. Requires {YoutubeID} variable filled out.</td>
    </tr>
  </table>

<hr>

<h2>Mode Changer</h2>
<h6>file: modes.txt </h6> <h6>Dependencies: None</h6><br>

Dependency for other modules to change chat to Subscriber, Slow Mode, and Emote Only chat on the fly, with a timer. No Outward Facing Commands.

<hr>

<h2>Pets</h2>
<h6>file: pets.txt </h6> <h6>Dependencies: None</h6><br>

  I have some pets on my stream that I toggle between with channel points. It's actually a super simple setup, but it does require editing the actual trigger if you wanted to use it for something.

  <table>
    <tr>
      <th>Channel Points Reward</th>
      <th>Options</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>Swap My Pet</td>
      <td>None</td>
      <td>Swaps Between "TotallyMyPetDog" and "TotallyMyPetCat" in the OBS Scene "pets"</td>
    </tr>
  </table>

<hr>

<h2>quotes</h2>
<h6>file: </h6> <h6>Dependencies:</h6><br>

  You can't change permissions for who can add quotes in StreamElements, so I went ahead and added this so my VIPs can add quotes.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!quoteadd [Quote], !addquote [Quote]</td>
      <td>VIP</td>
      <td>Sends "!quote add [Quote]" in chat, activating Stream Element's quote function.</td>
    </tr>
  </table>

<hr>

<h2>sfx</h2>
<h6>file: </h6> <h6>Dependencies:</h6><br>

  plays sfx when users pay channel points. I have a seperate folder for first fanfares, and I also include a limited "Budget" option that comes up every hour. Additionally, this is a seperate Kruiz Control thread if I want to play SFX from other modules.

  <table>
    <tr>
      <th>Channel Point Redemption</th>
      <th>Options</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>Sound Effects</td>
      <td>[Sound Effect Name]</td>
      <td>Plays [Sound Effect Name] as long as it is in your Kruiz Control Sounds Folder. Do not type file extension in [Sound Effect Name]. Only works for .ogg, .mp3, and .wav</td>
    </tr>
    <tr>
      <td>Budget SFX</td>
      <td>[Sound Effect Name]</td>
      <td>Functions Identically to the Sound Effects redemption, designed to be a lower cost with a cooldown.</td>
    </tr>
    <tr>
      <td>First</td>
      <td>[Sound Effect Name]</td>
      <td>Plays a sound effect inside the fanfare folder in your sounds folder. Functions the same as Sound Effects otherwise. Designed to be 1 time use per stream.</td>
    </tr>
  </table>

<hr>

<h2>Quickrun List</h2>
<h6>file: speedrun.txt </h6> <h6>Dependencies: None</h6><br>

  I have a list of quickruns I offer as a points reward. This really essentially functions as a list I can easily mess with using KC commands, rather than making a ton in Stream Elements.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!quickruns, !quickrunslist</td>
      <td>Everyone</td>
      <td>30 Second Cooldown. Posts the Quickruns list to chat.</td>
    </tr>
    <tr>
      <td>!quickrunadd [quickrun], !quickrunsadd [quickrun]</td>
      <td>Broadcaster, Moderator, VIP</td>
      <td>Adds [quickrun] to the Quickruns List.</td>
    </tr>
    <tr>
      <td>!quickrunremove [quickrun], !quickrunsremove [quickrun]</td>
      <td>Broadcaster, Moderator, VIP</td>
      <td>Removes [quickrun] to the Quickruns List.</td>
    </tr>
    <tr>
      <td>!quickrunrandom, !quickrunsraundom</td>
      <td>Everyone</td>
      <td>30 Second Cooldown. Sends a random Quickrun from the list to chat.</td>
    </tr>
  </table>

<hr>

<h2>Start Up Stuff</h2>
<h6>file: startup.txt</h6> <h6>Dependencies: None</h6><br>

  Posts to Discord when you go live if you type !live. Also is supposed to post if you have StreamElements set to post as yourself, and it automatically types in chat "YourName is Live!".

  You MUST fill out Avatar, TwitchID, and DiscordWebHook.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!live</td>
      <td>Broadcaster</td>
      <td>Posts a live announcement on discord with a link to your channel, your avatar, and your Twitch Title.</td>
    </tr>
  </table>

<hr>

<h2>Steam Cleaning</h2>
<h6>file: steamcleaning.txt </h6> <h6>Dependencies: None</h6><br>

I have streams where we take a list of games and play about 15 minutes of them, and pick at random. This helps me keep track of what's been played, helps me allow people to spend points to impact how they choose games, and I just wanted to see if I could make something like it to practice a bit more. This is here for reference mostly, I don't recommend using it, and I don't have a full breakdown here explaining it.

<hr>

<h2>Stream Elements Actions</h2>
<h6>file: streamelements.txt </h6> <h6>Dependencies: None</h6><br>

Dependency file for Stream Elements Actions. The majority of these are for making it easier to do typical stream elements things, like Giving out points, Dueling, Setting your Game, or Setting your title. No Outward Facing Commands.
