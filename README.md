# Turn server




## Realm

The value of the Realm attribute SHOULD be the domain name of the provider of the TURN server. This protocol uses the attribute in the digest. If the protocol client includes this attribute, the TURN server SHOULD use the specified Realm value in the digest challenge extension. If the protocol client does not include this attribute in the request message, the TURN server uses a default Realm value. The TURN server MUST include this attribute in the associated response and the Realm value MUST be the value that the TURN server used in the digest challenge extension.