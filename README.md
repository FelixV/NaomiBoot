NaomiBoot
=========

Name: NaomiBoot<br>
Version: 1.0<br>
Date: 24/03/2014<br>
Author: Gumbo<br>
Contact: https://github.com/GumboMcGee<br>


Intro
=====
So, I got sick and tired of having to boot up my pc every-time I wanted to NetBoot a game over to my Naomi. As a result, this project appeared. 
Basically, You go to http://naomiboot or the Raspberry Pi's IP address in any(?) web browser on the same network, and select a game, 
the Pi will then send the game over Ethernet. Pretty simple really. 

Requirements
=====
1. Wifi Adapter, I used an EdiMax adapter, its small, it works. 
2. Ethernet Cable
3. SD card, Images are available for 2GB, 8GB, 16GB and 32GB. If your card is a different size, Then you will need to manually expand the FAT32 "boot" partition.
4. 5V Power Supply, I personally use the 5V CN12 Connector on the Naomi Filterboard, All i did was cut up a Micro USB cable and stick a connector on the end and plugged it in.  (!WARNING!) I do not know how healthy this is for the Naomi, but it works, Just don't hold me accountable if it breaks anything

Things You Need To Do
=====
This does not just work out of the box, There are a couple of things you need to do. 

1. Change the WiFi credentials. <br>
I've made Changing the Wifi information as simply as possible. In the FAT32 Boot partition, Open the "interfaces" file and replace "YOUR WIFI NETWORK NAME" & "YOUR WIFI PASSWORD" with your network information.
Be sure to keep the Quotation marks.
2. Change your Naomi IP Address to 192.168.2.2, The raspberry pi's ethernet runs completly seperatly from the Wifi network. It has a static IP of 192.168.2.1

Removing Games
=====
If you want / need to remove games from the web front-end, you will need to edit the index.html file in the 
/var/www/ folder, open it with your favourite text editor (I recommend notepad++) and you will see plenty of lines like this:

    <figure><a href="javascript:void(0)" class="thumb label inside bottom" data-label="RomName" onclick="RomName();"><img src="roms/RomName/RomName.jpg" alt="RomName" /></a></figure>

All you need to do is either completely remove that line, or I recommend you just comment it out like so:

    <!-- <figure><a href="javascript:void(0)" class="thumb label inside bottom" data-label="RomName" onclick="RomName();"><img src="roms/RomName/RomName.jpg" alt="RomName" /></a></figure> -->

ROMS
=====
Place all your roms in this folder, Its important to use the names below for your roms otherwise they will not boot. 
If you want to have custom named roms then all calls to the roms can be found in /var/www/roms in the ".sh" file. 

ROM Names
=====
18WheelerDX.bin<br>
18WheelerSTD.bin<br>
AirlinePilots.bin<br>
AkatsukiBkAusfAchse.bin<br>
AlienFront.bin<br>
AzumangaDaiohPuzzleBobblev3.bin<br>
BorderDownv3.bin<br>
BurningCasinov3.bin<br>
CannonSpike.bin<br>
CapcomVsSNK2MillionaireFighting2001.bin<br>
CapcomvsSNKMilleniumFight2000.BIN<br>
CapcomvsSNKMilleniumFight2000Pro.bin<br>
ChaosFieldv3.bin<br>
CleopatraFortunePlusv6.bin<br>
ConfidentialMission.bin<br>
CosmicSmash.bin<br>
CrazyTaxi.bin<br>
DeadOrAlive2.bin<br>
DeadOrAlive2Millenium.bin<br>
DeathCrimsonOX.bin<br>
DemolishFist.bin<br>
DokiDokiIdolStarSeeker.bin<br>
dol222.bin<br>
DynamiteDekaEx.bin<br>
FOTNSNaomi2Fixed.bin<br>
ggx15.bin<br>
GiantGram2000.BIN<br>
GiantGramEPR21820PATCHED.bin<br>
GigaWing2.bin<br>
GuiltyGearXX.bin<br>
GuiltyGearXXAccentCorev6.bin<br>
GuiltyGearXXReload.bin<br>
GuiltyGearXXSlashv6.bin<br>
HeavyMetalGeomatrix.bin<br>
Ikarugav3.bin<br>
Illvelov6.bin<br>
JamboSafari.bin<br>
JingyStormTheArcade.bin<br>
karousv3.bin<br>
KnightsofValour.bin<br>
KuruKuruChameleonv3.bin<br>
LaKeyboardxyuv3.bin<br>
Lupin3TheShooting.bin<br>
LupinTheTyping.bin<br>
mamonorov6.bin<br>
MarvelVsCapcom2.bin<br>
MeltyBloodActCadenza(RevA).bin<br>
MeltyBloodActCadenzaVerB2v3.bin<br>
MeltyBloodActCadenzaVerBv3.bin<br>
MeltyBloodActressAgain.bin<br>
MeltyBloodActressAgainv6.bin<br>
MobileSuitGundamFederationVsZeon.bin<br>
MobileSuitGundamFederationVsZeonDX.bin<br>
MonkeyBall.bin<br>
MusapeysChocoMarker.bin<br>
NoukonePuzzleTakoron.bin<br>
Powerstone.bin<br>
PowerStone2.bin<br>
Psyvariar2v6.bin<br>
PuyoPuyoDaEPR22206PATCHED.bin<br>
PuyoPuyoFeverv6.bin<br>
QuizKeitaiQMode.bin<br>
RadirgyNoav6.bin<br>
Radirgyv3.bin<br>
RivalSchools2ProjectJustice.bin<br>
SambaDeAmigoEPR22966BPatched.bin<br>
SegaMarineFishingEPR22221.bin<br>
SegaStrikeFighter.bin<br>
SegaTetris.bin<br>
senkonewv6.bin<br>
SenkoNoRondeSPv3.bin<br>
senkov3.bin<br>
ShikigamiNoShiroIIv6.bin<br>
ShootingLove2007Exzealv6.bin<br>
Slashout.bin<br>
spawn.bin<br>
SpikersBattle.bin<br>
SportsJam.bin<br>
StreetFighterZero3Upper.bin<br>
SuperShanghai2005v6.bin<br>
SuperShanghai2005VerAv6.bin<br>
TetrisKiwamemichiv6.bin<br>
TheMazeOfTheKings.bin<br>
TheRumbleFish.bin<br>
TheTypingOfTheDead.bin<br>
ToyFighter.bin<br>
TriggerHeartExelicav6.bin<br>
Trizealv3.bin<br>
UnderDefeatv3.bin<br>
UsaguiYamashiroMahjongHenv3.bin<br>
VirtuaAthlete.bin<br>
VirtuaGolf.bin<br>
VirtuaNBA.bin<br>
VirtuaStriker22000.bin<br>
VirtuaTennis.bin<br>
VirtuaTennis2.bin<br>
WaveRunnerGP.bin<br>
WorldSeriesBaseball.bin<br>
WWFRoyalRumble.BIN<br>
ZeroGunner2.bin<br>
ZombieRevenge.bin<br>
