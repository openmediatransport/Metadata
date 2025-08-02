# Open Media Transport (OMT) Metadata Specification Document 1.0

This document contains recommended metadata specifications for use with Open Media Transport.

If you have a specification you would like to see listed here, submit a request under this repositories Issues section.

## Web Management

This defines a web management interface for a sender device.

Receivers should implement a way to browse to this address on request.

\<OMTWeb URL="http://x.x.x.x/" />

## PTZ Control

This defines what PTZ protocol is available for a PTZ camera device.
The following supported protocols are currently defined:

### Sony VISCA over IP

This is the standard VISCA over IP udp protocol implemented separately to OMT.

\<OMTPTZ Protocol="VISCAoverIP" URL="visca://x.x.x.x:port"  />

### Sony VISCA (Inband)

This is the standard VISCA over IP protocol encapsulated within OMT metadata.
Sequence is the same sequence number as used in the original protocol messages.

**Command** 

This is a command sent from controller to camera in hexadecimal format. 

\<OMTPTZ Protocol="VISCA" Sequence="22" Command="8101040700FF" />

**Reply**

This is a reply from camera sent back to controller and is in hexadecimal format.

\<OMTPTZ Protocol="VISCA" Sequence="22" Reply="0011AABBCC" />

