# Unoriginal-Rice-Patty

*"Unoriginal-Rice-Patty" is my personal title for the Replay-based attack on Honda and Acura vehicles*

This attack seems to affect EVERY Honda/Acura vehicle with remote/wireless radio entry. Honda does *NOT* ever institue a rolling code system and *ONLY* manufactures systems with static keys meaning there is NO layer of security.

## Summary:
A hacker can gain complete and unlimited access to locking, unlocking, controlling the windows, opening the trunk, and starting the engine of the target vehicle where the only way to prevent the attack is to either never use your keys or, after being compromised (which would be difficult to realize), resetting your keys at a
dealership.

## The Attack:
Simply capturing the signal sent from a FOB is enough to gain at least *some* control of the vehicle. If the target locks their vehicle, all it takes is
receiving it and saving it for me to gain the ability to replay the same command and have the vehicle respond accordingly.

Recording the "unlock" command from the target and replaying will allow me to unlock the vehicle whenever I'd like to, and it doesn't stop there *at all*
On top of being able to start the vehicle's *ENGINE* *Whenever I wished* through recording the "remote start" command, it seems possible to actually (through Honda's "Smart Key") demodulate any command, edit it, and retransmit in order to make the target vehicle do whatever you wish.

For Example:
Recording a "lock" command and flipping the following bits: 

```653-656, 667-668, 77-680, 683-684, 823-826, 837-838, 847-850, 853-854```

will tell the vehicle to unlock (These numbers include the preamble)

## *CONFIRMED* Vehicles:

• 2009 Acura TSX

• 2016 Honda Accord V6 Touring Sedan

• 2017 Honda HR-V (CVE-2019-20626)

• 2018 Honda Civic Hatchback

• 2020 Honda Civic LX


## The Interesting Part
Honda seemingly ignored CVE-2019-20626 (cited above in the list of confirmed, affected vehicles). They continued to implement 0 security measures against
this very simple "replay/replay and edit" attack. This CVE interestingly only cites one vehicle and I only discovered this much later in my pursuit for
research. 

## How Honda Can Fix This
Honda must implement a "rolling code" system into their vehicles' list of security measures. Rolling code systems have been around since 1995 and
work very well against hackers. Honda has seemingly never implemented this security measure, leaving them very far behind in the race toward a secure
technological future. As far as I can tell, this isn't easily "patchable". Honda can begin to implement security measures in future vehicles, however
it doesn't seem likely that they will go back and fix this security issue in older models.
