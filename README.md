# PubNub for Atmel's SAM D21 Usage Notes and Client SDK Examples

Pubnub example for Atmel SAM D21 and WINC1500 was a part of ASF, but is _not_ in the latest version of ASF.
Look for code in earlier versions of ASF distribution, path
`common/components/wifi/winc1500/pubnub_demo`. 

There is also an earlier "iteration" of this code in the 
history of this repository, which should work for some older ASF versions.

The Pubnub client is derived from the Contiki OS client, using the winc socket interface.
Its source code is in `Pubnub.c`. In the header (`Pubnub.h`) there are a few (documented) macros that the user can change to suit a particular application. For buffer/message size constraints, look at `PUBNUB_BUF_MAXLEN` and `PUBNUB_REPLY_MAXLEN`.

This Pubnub client support only the basic features: *publish* and *subscribe* to a channel (or a list of channels, but no channel group(s)) and *leave* (a (list of) channel(s)), which is suitable for most embedded applications.

Detailed instructions on how to connect all the HW, compile & upload the SW/FW and run the examples are in `examples/README.md`. Also, take a look at the application note in ASF.
