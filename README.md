CIDRUtils
=========

[![CI](https://github.com/felfert/CIDRUtils/actions/workflows/ci.yaml/badge.svg?branch=master&event=push)](https://github.com/felfert/CIDRUtils/actions/workflows/ci.yaml) [![javadoc](https://javadoc.io/badge2/com.github.felfert/cidrutils/javadoc.svg)](https://javadoc.io/doc/com.github.felfert/cidrutils)

This is a mavenized and improved version of the original. See forked link.
CIDRUtils is a Java library that enables you to get an IP range from CIDR specification. It supports both IPv4 and IPv6.
CIDRUtils is also distributed via [![Maven Central](https://img.shields.io/maven-central/v/com.github.felfert/cidrutils.svg?label=Maven%20Central)](https://search.maven.org/search?q=cidrutils)

### IPv4 Example 
<pre>
CIDRUtils cidrUtils = new CIDRUtils("10.77.12.11/18");
String networkAddress = cidrUtils.getNetworkAddress();
String broadcastAddress = cidrUtils.getBroadcastAddress();
</pre>
Evaluating the code above would produce `10.77.0.0` for the `networkAddress` and `10.77.63.255` for the `broadcastAddress`. 

### IPv6 Example
<pre>
CIDRUtils cidrUtils = new CIDRUtils("435:23f::45:23/101");
String networkAddress = cidrUtils.getNetworkAddress();
String broadcastAddress = cidrUtils.getBroadcastAddress();
</pre>

Evaluating the code above would produce `435:23f:0:0:0:0:0:0` for the `networkAddress` and `435:23f:0:0:0:0:7ff:ffff` for the `broadcastAddress`. 

### License
CIDRUtils is released under MIT License.
