--------------------------------------------
Gotek Adapter Module v1.1
Copyright (c) 2018 RBSC
Portions (c) Talent/Telematica
--------------------------------------------

WARNING! To avoid damage to the adapter and your MSX computer never insert or remove the adapter when a computer is powered on!

IMPORTANT! This adapter is compatible with MSX1, MSX2 and MSX2+ systems. However on MSX1 systems MSX-DOS may not start unless a
memory extension cartridge is inserted into one of the slots. 

IMPORTANT! The Gotek emulator must be secured by at least 2 screws (one from each side) in the adapter's case. Otherwise it will
be detached from the board if pulled by its case.


About
-----

This device is the adapter for the Gotek floppy emulator designed by RBSC based on their own Multicontroller as well as on the
TDC-600 controller that was originally designed by Talent/Telematica. The adapter was specifically made in the form of the side
slot cartidge, that can be used with Yamaha MSX YIS503, CX5M, CX5MII and similar MSX machines. The main idea was to introduce
the possibility to use real floppy disks or their images in the Gotek emulator on these diskless computers.

The adapter can be either used to host the Gotek emulator inside its body or to be used as the controller for the external floppy
disk drives. The Gotek emulator may be also used as the external device.

The adapter may be used with the 50-pin slot on any compatible MSX computer with the special 50-to-60 pin adapter cable or with
the original Yamaha's cartridge-based adapter. Please keep in mind that the Gotek emulator must have the FlashFloppy firmware.
The adapter was tested only with that firmware and the correct functionality is not guaranteed with any other firmware.


Usage with external devices
---------------------------

To be able to use the adapter with external devices, the special cover with holes for the floppy interface connector and for the
power connector must be used. The standard male-to-male 34-pin floppy connector with or without the cable locks should be used to
provide the interface for the external devices. It's recommended to use the connector with the "key" to avoid inserting the
interface cables upside down. As an option, a long floppy cable may be connected directly to the adapter's board (pads marked as
CN2) and stored inside the adapter's case (there's plenty of room there). However it's better to install the through-pin connector
and attach it to the board with wires. Also it may be a good idea to power the floppy drives from external source because certain
MSX computers may not be designed to power floppy drives from their internal power supplies. So if you power older floppy drives
from the adapter's power connector, your MSX's power supply may be loaded beyond its designed capacity. This is a low risk event,
but might still happen.

For the floppy's power connector it's best to use the 4-pin male-to-male audio connector with the lock (those were installed on
the older audio cards to connect them to the audio outputs of the older CD-ROM drives), but other connectors may be used as well.
It's better to use the connectors that can't be connected upside down and, as a result, supply 12v to the 5v circuit - this will
cause severe damage to the Gotek emulator or the floppy drive. This connector must be wired to the PWR pads on the board to provide
both 5v and 12v to the floppy drives. The floppy drives produced in the recent years as well as the Gotek emulator don't need 12v,
but older drives require it.

See the pictures in the PIC subfolder to check the connectors and the wiring of the external devices. Please note that the 720kb
drives must be configured as "A" and the straight floppy cable must be used for them. Those drives must be set as DS0, otherwise
they will not work. For the 1.44mb PC drives with DS1 or DS2 settings a twisted floppy cable must be used. Those PC drives could
be configured as either "A+B" or "B+A". See the "Jumper settings" chapter for more info.


Usage with internal devices
---------------------------

The adapter was originally designed to host the Gotek emulator inside its body. The emulator should be connected to the board
with the 34-pin dual row female connector with long pins. The power could be connected by either using the Molex connector with
its wires soldered to any PWR connector on board or with a single row 4-pin female connector with long pins. It's important to
remember that all internal connectors must have long pins so that they could reach the interface and power connectors of the Gotek
emulator that are located higher than the adapter's board. See the pictures in the PIC subfolder to check the connectors and the
wiring of the inserted Gotek emulator.

Normally the well-soldered power and floppy interface connectors will allow the emulator to be removed from the adapter's case
without too much effort. However inserting the emulator may bend the power connector or get the wrong connection to the floppy
interface pins, so it's highly recommended to open the adapter's case when inserting the emulator to make sure that both power
and interface connectors are properly aligned.


Jumper settings
---------------

The adapter has four 3-pin configuration jumper pins. All 4 of them must have one jumper installed at all times. On the board there
is a CFG table that shows jumper configurations for different drives.

When all 3-pin jumpers are set in the upper position, then a normal 1.44mb PC drive (with default DS1 setting) can be connected to
the board with the standard twisted interface cable. There can be maximum 2 drives connected to the adapter with the same cable. The
drive set as DS1 will be bootable (A:), the drive with DS2 setting will be used as the second drive (B:)

When all 3-pin jumpers are set in the lower position, then a normal 1.44mb PC drive (with default DS1 setting) can be connected to
the board with the standard twisted interface cable. There can be maximum 2 drives connected to the adapter with the same cable. The
drive set as DS2 will be bootable (A:), the drive with DS1 setting will be used as the second drive (B:)

When the 3-pin jumpers are set as shown for the "A" configuration, then a DS/DD 720kb drive set as DS0 or a Gotek emulator set as
DS0 can be connected to the adapter with the straight floppy cable (PC cable with a "twist" won't work). Only one drive may be
connected to the controller in this case. The operating system and certain programs will still allow to use 2 logical drives even if
one drive is connected, but a user will need to change the diskettes or switch the disk images manually when asked.


Selecting BIOS versions
-----------------------

There are 2 versions of disk BIOS available for the adapter - the original one (1.0) and the one translated into English (1.1).
There's a jumper on the board marked as "BIOS VER." that allows to select the desired BIOS version. When the jumper is installed,
the 1.0 version will be used, otherwise the 1.1 version will be used. The version number will be shown when a computer boots into
MSX Basic. Please note that  these BIOSes are capable of working with the 5.25 inch floppy drives, but RBSC was not testing the
adapter with those drives. So if you are using the 5.25 inch drive with the adapter, you are doing this on your own risk.


Notes
-----

The adapter may not load certain games, disk images or boot to certain operating system versions because of the limitations of the
original TDC-600 controller and its firmware. The design of the TDC controller was simplified to have less electronic components,
so its functionality differs from the standard floppy controllers. Certain incompatibility issues will be observed.

The 3D models of the adapter's case, bottom and side cover are provided in the STL format for self-printing. They can be printed on
any 3D printer with PLA or ABS. The recommended settings are 0.2mm layer thickness, supports on, 25% infill, 25% supports, heated
bed and a hood over the printer (to avoid deformations). The case and the bottom cover parts must be printed with their open sides
facing upwards to avoid too many supports and the damage of the screw holders when removing those supports.

The bottom cover should be attached to the body with 3.0mm x 10mm screws with flat heads. It's recommended not to tighten the screws
too much to avoid breaking the threads inside the screw holders. Also keep in mind that the cover is made out of plastic (unlike
the original SFG case's cover), so it needs a bit more gentle handling.

The Gotek emulator needs to be secured inside the adapter's case by two or (better) four 3.0mm x 15mm screws with flat or conical
heads. It's recommended not to tighten the screws too much to avoid breaking the threads inside the Gotek's case.

If you are assembling the adapter with external connectors yourself, please note that it's better to solder the wires between the
board and the connectors. If you use Dupont connectors (like on the images) and jumper pins, you will need to remove the plactic
parts of the pins and cut the 2mm tops of all the pins. Otherwise you won't be able to connect the Dupont connectors to the board. 


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Wierzbowsky, Tnt23, Ptero, Pencioner and DJS3000 can be contacted via the MSX.ORG or ZX-PK.RU forums. Just
send a personal message and state your business.

The RBSC repository can be found here:

https://github.com/rbsc

The MSX-related 3D models published by RBSC can be found here:

https://www.thingiverse.com/groups/rbsc/things


-= ! MSX FOREVER ! =-
