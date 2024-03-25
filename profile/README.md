# Open MUX

Open MUX is a framework for creating multi-user XR applications.

Building multi-user applications is hard, especially for XR. Using a well-thought-out framework can save you a lot of development time. Other frameworks are typically complex, expensive and/or hard to customize. Open MUX is easy to use, free, and built for customization.

Open MUX is best suited for research, demonstrators or hobby applications, not for online games or enterprise applications.

## Purpose

I believe that we don't see a lot of multi-user XR research because multi-user experiments are hard to build and therefore expensive. With Open MUX my goal is to significantly reduce that cost.

## How it works

Open MUX is a _client-authorative_ framework with a _client–server architecture_. It consists of several components:

- A [Server](https://github.com/open-mux/open-mux-server) which functions as the main connection hub between clients and GUIs. It holds the most recent world state and is required for Open MUX to work.
- A [Unity Package](https://github.com/open-mux/open-mux-client-unity) which can be installed in your project to transform it into an Open MUX client. It can then send and receive data from- and to other clients (via the server).
- A [Management GUI](https://github.com/open-mux/open-mux-management-gui) which is optional but can be used to visually display and manage connected clients.

## Open MUX vs other frameworks

Other frameworks are typically:

- Unnecessarily complex for your project, costing you a lot of time to learn and implement it
- Closed-source, which makes it harder to customize it to your needs
- Expensive, which makes it harder to use in research- and hobby projects
- Not very privacy-friendly by hosting your data on their servers

Open MUX counters that by being:

- Easy-to-use (e.g. the server downloads, installs or runs with just one command)
- Open-source, which gives you the flexibility to customize any part of it
- Free
- Local by default. Data stays in your local network unless you explicitly change it

Oh, and it's also performant and reliable.

## Getting started

### Prerequisites

- Node.js is required for the Server and Management GUI. It can be installed from [their website](https://nodejs.org/)
- Unity is required for building the client application. It can be installed from [their website](https://unity.com/)

### Installation

1. Install the Open MUX Server (see [the installation instructions](https://github.com/open-mux/open-mux-server/blob/main/README.md))
1. Install the Open MUX Unity Package into your project (see [the installation instructions](https://github.com/open-mux/open-mux-client-unity/blob/main/README.md))
1. _(optional)_ Install the Open MUX Management GUI (see [the installation instructions](https://github.com/open-mux/open-mux-management-gui/blob/main/README.md))

### Usage

1. Start the Open MUX Server (see [the starting instructions](https://github.com/open-mux/open-mux-server/blob/main/README.md))
1. (optional) Start the Open MUX Management GUI (see [the starting instructions](https://github.com/open-mux/open-mux-management-gui/blob/main/README.md))
1. Start your Client application (see [the starting instructions](https://github.com/open-mux/open-mux-client-unity/blob/main/README.md))

## Limitations

- Open MUX is _client-authorative_, which means that the server blindly trusts the clients, making it easy for clients to cheat. This is the main reason why you probably shouldn't use this framework for online multiplayer games. I chose client-authorative instead of server-authorative because it removes a lot of complexity (making the framework easier to customize) and it likely isn't necessary for the recommended use cases.
- Currently I only maintain a Unity plugin. You can also connect Unreal Engine or Godot clients to Open MUX but I just haven't built plugins for them. I may do that in the future though (see the Roadmap section).

## Roadmap

- Besides co-located users (i.e. users in the same physical location), I'm planning on adding support for distributed users (i.e. users in different physical locations) soon.
- I currently only maintain a Unity plugin but I'm thinking about building an Unreal Engine plugin too.

## Contact

See the Discussions tab on GitHub.
