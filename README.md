![Logo](https://github.com/lontivero/Open.Nat/raw/gh-pages/images/logos/128.jpg)
Open.Nat
======

Open.Nat is a lightweight and easy-to-use class library to allow port forwarding in NAT devices that support  UPNP (Universal Plug & Play) and/or PMP (Port Mapping Protocol). 


Goals
-----
NATed computers cannot be reached from outside and this is particularly painful for peer-to-peer or friend-to-friend software.
The main goal is to simplify communication amoung computers behind NAT devices that support UPNP and/or PMP providing a clean and easy interface to get the external IP address and map ports and helping you to achieve peer-to-peer communication. 


Example
--------


```c#
NatUtility.DeviceFound += (sender, args) => {
  Console.WriteLine("It got it!!");
  var ip = await device.GetExternalIPAsync();
  Console.WriteLine("The external IP Address is: " + ip);
};

NatUtility.Initialize();
NatUtility.StartDiscovery();
```

For more info please check the [Wiki](https://github.com/lontivero/Open.Nat/wiki)

Development
-----------
Open.Nat is been developed by [Lucas Ontivero](http://geeks.ms/blogs/lontivero) ([@lontivero](http://twitter.com/lontivero)). You are welcome to contribute code. You can send code both as a patch or a GitHub pull request. 

Build Status
------------

[![Build status](https://ci.appveyor.com/api/projects/status/dadcbt26mrlri8cg)](https://ci.appveyor.com/project/lontivero/open-nat)

[![NuGet version](https://badge.fury.io/nu/open.nat.png)](http://badge.fury.io/nu/open.nat)

### Version 1.0.15.0
  *  Discovery performance and bandwidth improved
  *  Tracing improved
  *  Cleaner code


