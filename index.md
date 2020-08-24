How-to DECT: Setting up a Mitel SIP-DECT RFP for home/enthusiast use
====================================================================

DECT telephony, courtesy of Eventphone, has been a staple of hacker conferences
for [years][ep-history].  
Recently, Eventphone has [improved their registration and management
system][newsys] and [presented more information on its inner workings][mifail].

[ep-history]: https://media.ccc.de/v/35c3oio-70-eventphone-frher-heute-morgen-
[newsys]: https://media.ccc.de/v/eh19-179-das-neue-eventphone-poc-telefonsystem
[mifail]: https://media.ccc.de/v/36c3-10576-mifail_oder_mit_gigaset_ware_das_nicht_passiert

With all this information at the ready, one might decide to try and replicate
the familiar DECT setup at home.  
Even with these excellent (and entertaining!) resources, however, SIP-DECT is
very much an enterprise solution and can be a bit daunting to set up for your
own personal use.  
Think for a few moments whether you really want to go through with this, or if
you already have plenty of other side-projects to occupy your time. Then,
probably, read on. ;)

## Glossary: What is SIP-DECT?

Just to recap:

- **DECT** is a wireless communication standard that is, among other things, used
  for cordless telephones.
- **SIP** is technically only a "signalling protocol" (it does say "Session
  Initiation" in the name), but is colloquially used to refer to network-based
  telephony ("Voice-over-IP") in general.
- **SIP-DECT** is a line of products by *Mitel* (see below) that combines the
  two: SIP-DECT devices act as DECT base stations and SIP clients, allowing
  DECT phones to make calls via a SIP server.
- **Mitel** purchased Aastra in 2013, who had in turn purchased DeTeWe in 2005, so
  you'll find all three company names mentioned somewhat interchangeably when
  it comes to SIP-DECT equipment.

The SIP-DECT setup uses several more terms and abbreviations. You'll primarily
come across:

- **RFP** (Radio Fixed Part):  
  Simply put, a DECT base station.  
  *You can have one or multiple of these.*
- **PP** (Portable Part):  
  A DECT phone handset.  
  *You can have one or multiple of these.*
- **OMM** (Open Mobility Manager):  
  A piece of software (running as a permanent service) that accepts your
  configuration settings and coordinates communication across all *RFP*s. The
  *OMM* has a web interface that allows you to configure most (but not all)
  settings.  
  *You will usually have one instance of this, possibly with a second instance
  as fallback. You might use the web interface for the inital installation, and
  occasionally for administrative tasks afterwards.*
- **OM Configurator**:  
  A piece of software (an administrative GUI) that allows you to configure
  Mitel *RFP*s' basic settings: IP address, network boot paths, *OMM* addresses
  they should use.  
  *You might need to use this once for the initial installation, then not need
  it anymore.*
- **OMP** (OM Management Portal):  
  A piece of software (an administrative GUI) that allows to configure your
  *OMM*. Similar features to the *OMM*'s own web interface, but some options
  are available only in the web interface, or only in the *OMP*.  
  *You might use this for the inital installation, and occasionally for
  administrative tasks afterwards.*

## Hardware: RFP generations

The SIP-DECT RFP hardware exists in several feature classes and has gone
through several years of development. The model numbers that arise from this
are, shall we say, *creative*.

The naming follows the schema "RFP <number> <IP|WLAN>".  
"IP" models can only act as a DECT base station; "WLAN" models can provide both
DECT base station and WiFi access point service at the same time. Both DECT and
WiFi functionality can be enabled/disabled in the configuration.

RFPs exist in indoor and outdoor variants (easily distinguished by their smooth
vs rugged case).  
Do not use an indoor variant outdoors; its circuit board will corrode, which is
generally a bad thing.

### Model overview

Let's look at an overview (as of the release of SIP-DECT v8.0):

|                | indoor, 4 speech channels | indoor, 8 speech channels                  | outdoor, 8 speech channels        | identification characteristic      |
|----------------|---------------------------|--------------------------------------------|-----------------------------------|------------------------------------|
| 2nd generation |                           | 32 IP, 42 WLAN                             | 34 IP                             | smooth edges, no USB port          |
| 3rd generation |                           | [35 IP][rfp35ip], 43 WLAN                  | 36 IP (PoE-only), 37 IP (ext-ant) | smooth edges, has a USB port       |
| 4th generation | 44 IP                     | [45 IP][rfp45ip], 47 IP (ext-ant), 48 WLAN | 47 IP DRC (ext-ant)               | "modern" angular look, no USB port |

(PoE-only): power only via PoE, no RJ11 power input  
(ext-any): external antenna connector, no internal DECT antenna

[rfp35ip]: https://www.telefonanlage-shop.de/Aastra-EOL-END-OF-LIFE-TK-Systeme-DECT-Systeme-244/Aastra-RFP-35-IP-indoor-709#link_3
[rfp45ip]: https://www.telefonanlage-shop.de/Aastra-DECT-Systeme-SIP-DECT-RFP-62/Mitel-RFP-45-IP-indoor-2221#link_3

### Power

Gen 2 and 3 RFP can be powered via Power-over-Ethernet or via an RJ11 power connector.
Gen 4 only supports Power-over-Ethernet.

### Buying an RFP

RFPs can cost upwards of 450€ per piece when new.  
Much to Mitel's surprise, there is a second-hand market for used devices
(though even those are not exactly "cheap").  
You will usually find several offers for RFPs on common auction sites, but it
may take some patience to find ones in the 100€ range. (The Eventphone
presentation mentions offers around 50€, but those mostly applied to bundles of
multiple RFPs and have become a rare exception now that documentation for
SIP-DECT setups is becoming more accessible.)

## Plugging it in: Getting your RFP(s) up and running

## Software: Configuring the RFP

## Telepho-now: Registering a handset and making a call

## More: Larger deployments, SIP servers, and other shenanigans
