Fill out the Variables in the samplejovivariables.txt to your proper answers. You can rename the variables file to pretty much anything as long as you remember to include it in the fileTriggers.txt

Add whatever modules you want to use to the fileTriggers.txt in the Kruiz-Control-master folder.
SOME OF THE MODULES ARE DEPENDENT ON OTHER MODULES! I'll add more information in the readme over time to help make sure you know what's what.

Add sounds you want into the sounds folder (.wav, .mp3,, .ogg only please. .ogg seems to run poorly though)

I strongly recommend using Kruiz-Control-Configurator, if nothing else, to keep your Kruiz Control up to date.

There are two main pieces to my code:

The Lib Folder:
  This is primarily a TON of stuff that I use to make other functions work and not have to re-write code over and over again. This isn't really meant to be plug and play stuff, but is mostly here for you to read and make stuff with it if you want to. I'm not currently planning on making real documents for these, but maybe I will later.

Everything Else:
  These are the core triggers! These are explained in the documents below. These will have semi-friendly ways of setting them up that works for you best, mostly done through chat commands or setting up samplejovivariables.txt with your own info.



<hr>


<h2>Changing Backgrounds</h2>
<h6>file: backgrounds.txt</h6> <h6>Dependencies: lib_globallist.txt</h6><br>


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
    <td>!currentBG,<br> !BGCurrent</td>
    <td>Everyone</td>
    <td>15 Second Cooldown. Sends the Current Background name to chat.</td>
  </tr>
  <tr>
    <td>!changebg [background name],<br> !bgset [background name]</td>
    <td>Broadcaster<br> Moderator<br> VIP</td>
    <td>Sets the current background to [background name].</td>
  </tr>
  <tr>
    <td>!randomBG, <br>!bgrandom</td>
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

<h2>Media Controller</h2>
<h6>file: pcmediacontrols.txt</h6> <h6>Dependencies: None</h6><br>

  Uses strm.tool to allow mods to play/pause my music, and skipping of music with channel points. Requires some setup with Crash Koek's strm.tools, filling out the strmtool variables.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!playmusic,<br> !pausemusic</td>
      <td>Broadcaster<br> Moderator<br> VIP</td>
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
      <td>skip<br> back</td>
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

<h2>Pets</h2>
<h6>file: pets.txt </h6> <h6>Dependencies: lib_globallist.txt</h6><br>

Functionally the same as the Backgrounds, but just another seperate list! I use this for pets that I keep on my screen.

<table>
<tr>
  <th>Command</th>
  <th>Permissions</th>
  <th>Output</th>
</tr>
<tr>
  <td>!petadd [source name] </td>
  <td>Broadcaster</td>
  <td>This adds [source name] as a source that can be chosen for a random pet.</td>
</tr>
<tr>
  <td>!petremove [source name]</td>
  <td>Broadcaster</td>
  <td>This removes [source name] from the pets list.</td>
</tr>
<tr>
  <td>!petsclear</td>
  <td>Broadcaster</td>
  <td>This entirely clears the pets list.</td>
</tr>
<tr>
  <td>!pets</td>
  <td>Everyone</td>
  <td>15 Second Cooldown. This Command shows the list of all pets.</td>
</tr>
<tr>
  <td>!currentPet,<br> !PetCurrent</td>
  <td>Everyone</td>
  <td>15 Second Cooldown. Sends the Current Pet name to chat.</td>
</tr>
<tr>
  <td>!changepet [source name],<br> !petset [source name]</td>
  <td>Broadcaster<br> Moderator<br> VIP</td>
  <td>Sets the current pet to [source name].</td>
</tr>
<tr>
  <td>!randompet,<br> !petrandom</td>
  <td>Broadcaster</td>
  <td>Sets the pet to a random choice.</td>
</tr>
</table>

<table>
<tr>
  <th>Channel Point Rewards</th>
  <th>Options</th>
  <th>Output</th>
</tr>
<tr>
  <td>Pick Pet</td>
  <td>[Source Name]</td>
  <td>Changes the pet to whatever source is in the Message.</td>
</tr>
<tr>
  <td>Random Pet</td>
  <td>None</td>
  <td>Randomly Selects a Pet</td>
</tr>
</table>

<hr>

<h2>StreamElements Add Quotes</h2>
<h6>file:quotes.txt </h6> <h6>Dependencies:</h6><br>

  You can't change permissions for who can add quotes in StreamElements, so I went ahead and added this so my VIPs can add quotes.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!quoteadd [Quote],<br> !addquote [Quote]</td>
      <td>VIP</td>
      <td>Sends "!quote add [Quote]" in chat, activating Stream Element's quote function.</td>
    </tr>
  </table>

<hr>

<h2>Raffle/Scratch Cards</h2>
<h6>file: raffle.txt</h6> <h6>Dependencies: None, but reccomended to have streamelements.txt, sfx.txt, jukebox.txt</h6><br>

This Module requires setting up variables : RaffleRarities and creating all the Prize lists for the rarities (Ex: Common_Prizelist).
This module allows for creating a ChannelPoint reward that does any action. I reccomend actions like:
streamelements_AddPoints [user] [amount]
streamelements_AddPoints all [amount]
playSFX [sfxname]

Rarities scale based on what you set the var_BaseRaffleOdds and var_IncrementRaffleOdds. Default is 1 for the base, and 9 for the increment. For the standard rarities, this makes Legendary 1%, Epic 10%, Rare 20%, Uncommon 30%, and Common 40%.

The more you want to customize this, the more you have to get into Kruiz Control.

<table>
  <tr>
    <th>Channel Point Redemption</th>
    <th>Options</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>Raffle,<br> Scratch Card,<br> More Aliases in Description</td>
    <td>None</td>
    <td>Randomly selects a prize from your prize list, allowing for rarities. All Aliases: "Rafflecard" "Raffle" "Raffle Card" "Buy Raffle" "Buy Raffle Card" "Scratch Card" "ScratchCard" "Buy Scratchcard" "Buy Scratch Card"</td>
  </tr>
</table>

<table>
  <tr>
    <th>Command</th>
    <th>Permissions</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>!raffleprizes [rarity],<br> !scratchprizes [rarity],<br> !prizes [rarity]</td>
    <td>Everyone</td>
    <td>Posts the [rarity] pool of prizes to chat. Directly Exports the list of prizes.</td>
  </tr>

</table>

<hr>

<h2>Sound Effects</h2>
<h6>file: sfx.txt </h6> <h6>Dependencies: lib_soundeffects.txt</h6><br>

  Plays sfx when users pay channel points. I have a seperate folder for first fanfares, and I also include a limited "Budget" option that comes up every hour. Additionally, this is a seperate Kruiz Control thread if I want to play SFX from other modules.
  Additionally, gives the option to play a sound from the sounds folder upon the first chat of specific chatters. This does require a bit of diving into the variable setup.

  The Variables for entry SFX are broken down like this:<br>
    <code>list add [username]Enter "[filename]"</code><br>
  [username] is the username checked on entry.
  [filename] is the name of the file to play that the Sound Effect is. NO FILE EXTENSION.


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
<h6>file: speedrun.txt </h6> <h6>Dependencies: lib_globallist.txt</h6><br>

  I have a list of quickruns I offer as a points reward. This really essentially functions as a list I can easily mess with using KC commands, rather than making a ton in Stream Elements.

  <table>
    <tr>
      <th>Command</th>
      <th>Permissions</th>
      <th>Output</th>
    </tr>
    <tr>
      <td>!quickruns,<br> !quickrunslist</td>
      <td>Everyone</td>
      <td>30 Second Cooldown. Posts the Quickruns list to chat.</td>
    </tr>
    <tr>
      <td>!quickrunadd [quickrun],<br> !quickrunsadd [quickrun]</td>
      <td>Broadcaster<br> Moderator<br> VIP</td>
      <td>Adds [quickrun] to the Quickruns List.</td>
    </tr>
    <tr>
      <td>!quickrunremove [quickrun],<br> !quickrunsremove [quickrun]</td>
      <td>Broadcaster<br> Moderator<br> VIP</td>
      <td>Removes [quickrun] to the Quickruns List.</td>
    </tr>
    <tr>
      <td>!quickrunrandom,<br> !quickrunsraundom</td>
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
