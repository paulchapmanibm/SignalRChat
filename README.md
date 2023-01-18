# SignalRChat ReadMe

https://github.com/paulchapmanibm/SignalRChat

Get in touch if you'd like help, or have feedback regards running .Net workloads on IBM Power Systems
You can email me at PaulChapman@uk.ibm.com

The project is stored in the GitHub repository and can be deployed on 64-bit
Intel (`x64` or `x86_64`) or IBM Power (`ppc64le`) platforms.

# Demo

See this LinkedIn article for a demonstration of this ASP.NET Core with SignalR
application. The demo shows how to deploy via 2 different strategies:

1. Locally built dockerfiles via the command line
2. Source-to-image (s2i) builds via the OpenShift Web UI

(It's also possible to mix and match, and for example, to do s2i builds via the
command line)

https://www.linkedin.com/pulse/net-7-aspnet-core-signalr-demonstration-paul-chapman/?trackingId=WNo3ysBrlUO9GYrRH1pJLA%3D%3D

Also available on YouTube https://youtu.be/N--JQMaquxc

- I demonstrate deploying a .NET 7 application using ASP.NET Core with SignalR library on IBM Power Systems with OpenShift.
- I created this demonstration as an Italian ISV required ASP.NET Core with SignalR support to port their application to IBM Power Systems.
- I created the application on my x64 laptop using Visual Studio.
- The project is stored in this GitHub repository and can be deployed on x64 or IBM Power ppc64le platform
- There are two demonstrations in the recording
  - The first is created from my GitHub repository using the command line on a Bastion Server.
  - The second (7:45) is deployed using the OpenShift GUI User Interface Source to Image functionality.

# Prerequisites

Make sure to install the .NET imagestream into your OpenShift instance before
running this demo yourself.

- For IBM Power Systems with OpenShift:

      oc apply -f https://raw.githubusercontent.com/redhat-developer/s2i-dotnetcore/master/dotnet_imagestreams_ppc64le.json

- For OpenShift running on 64-bit Intel:

      oc apply -f https://raw.githubusercontent.com/redhat-developer/s2i-dotnetcore/master/dotnet_imagestreams.json
