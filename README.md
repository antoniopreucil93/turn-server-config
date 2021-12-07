# Turn server




## Realm

The value of the Realm attribute SHOULD be the domain name of the provider of the TURN server. This protocol uses the attribute in the digest. If the protocol client includes this attribute, the TURN server SHOULD use the specified Realm value in the digest challenge extension. If the protocol client does not include this attribute in the request message, the TURN server uses a default Realm value. The TURN server MUST include this attribute in the associated response and the Realm value MUST be the value that the TURN server used in the digest challenge extension.

## Listening ip

Listener IP address of relay server.

## External IP (-X)

TURN Server public/private address mapping, if the server is behind NAT. In that situation, if a -X is used in form "-X <ip>" then that ip will be reported as relay IP address of all allocations. This scenario works only in a simple case when one single relay address is be used, and no CHANGE_REQUEST functionality is required. That single relay address must be mapped by NAT to the 'external' IP.

## Fingerprint

Use fingerprints in the TURN messages. If an incoming request contains a fingerprint, then TURN server will always add fingerprints to the messages in this session, regardless of the per-server setting.

## Listening Port

TURN listener port for UDP and TCP listeners (Default: 3478). Note: actually, TLS & DTLS sessions can connect to the "plain" TCP & UDP port(s), too - if allowed by configuration.

## Min Port and Max Port

Upper and lower bound of the UDP port range for relay.

## lt-cred-mech

Use long-term credentials mechanism (this one you need for WebRTC usage).