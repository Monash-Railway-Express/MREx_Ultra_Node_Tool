# About the MREx Ultra Node Tool

The MREx Ultra Node Tool (MUNT) is a stack that facilitates setting parameters of the system remotely while the system is operating. It comprises:
- MUNT server: located within the system, it transmits current parameters from the system and receives requests to set parameters on the system.
- MUNT API: an HTTP interface which remote MUNT clients use to make read and write requests to the MUNT server.
- MUNT client: user interface with which the operator views and modifies parameters on the MUNT server.

This repository contains the code for an implementation of a GUI MUNT client. This document describes the MUNT API. The [MREx CAN Logger](https://github.com/Monash-Railway-Express/MREx_Nodes/tree/main/nodes/node8-logger/CAN_logger) will implement a MUNT server.

## API

The MUNT API is accessed through HTTP. It has one endpoint. All response and request bodies are in JSON.

### GET

Retrieve all accessible parameters and their values.

200 OK response:
```
{
	"key": value,
	...
}
```

### PATCH

Request to set the specified parameters to a specified value. If a parameter specified in a request is not recognised by the MUNT server (that is, does not appear in the GET response), it is silently ignored.

Request:
```
{
	"key": value,
	...
}
```

202 Accepted response:
```
["key", ...]
```

The 202 Accepted response body is an array of all recognised parameters from the request. A 202 Accepted response does not indicate that the parameters were successfully set and does not guarantee that the parameters will be set. To verify that parameters have been set to new values, issue a GET request.