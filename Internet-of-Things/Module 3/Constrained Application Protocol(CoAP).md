# Constrained Application Protocol (CoAP)


> CoAP defines simple flexible ways to manipulate sensors and actuators for data or device management.


CoAP message format

| CoAP Message Field | Description |
| ----- | ----- |
| Ver(Version) | Identifies the CoAP Version |
| T(Type) | Defines one of the four message types: - Confirmable (CON) Non-Confirmable (NON) Acknowledgement (ACK) Reset (RST) |
| TKL(Token Length) | Specifies the size (0-8 Bytes) of the Token Field |
| Code | Indicates the request method for a request message and a response code for a response message |
| Message ID | Detects message duplication and used to match ACK and RST message types to CON and NON message types |
| Token | With a length specified by TKL correlated requests and responses |
| Payload | Carries the CoAP application data. Optional field, but when it is present, a single byte of all 1s(0xFF) precedes the payload |
