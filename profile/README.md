# RadishNet

RadishNet is a framework for easily creating multi-user applications. It's purpose is to save you time by providing you with a simple but solid networking architecture that you can easily customize to your needs.

Other multi-user frameworks are typically complex, expensive and/or hard to customize. RadishNet is easy to use, free, and built for customization.

RadishNet is best suited for research, demonstrators, local games or hobby applications, not for online games or enterprise applications. If you're building an online multiplayer game, go for something like Fish-Net, Mirror or Photon. Otherwise, read on.

## RadishNet vs other frameworks

Other multi-user/multiplayer frameworks are typically:

- Complex, which is usually necessary for online multiplayer games but not for other projects
- Expensive
- Closed-source, which makes it harder to customize to your needs
- Not very privacy-friendly by hosting your data on their servers

RadishNet counters that by being:

- Easy to use
- Free
- Open-source
- Local. No data leaves your local network unless you explicitly change it

## How it works

RadishNet is a _client-authorative_ framework with a _client–server architecture_. It consists of several components:

- A [Server](https://github.com/radishnet/radishnet-server) which functions as the connection hub between clients. It holds the most recent world state and is required for RadishNet to work
- A [Unity Package](https://github.com/radishnet/radishnet-client-unity) that transforms your project into a RadishNet client. It can then send and receive data from- and to other clients (via the server)
- A [Management GUI](https://github.com/radishnet/radishnet-management-gui) which is optional but can be used to visually display and manage connected clients in your web browser

## Getting started

### Prerequisites

- Node.js is required for the Server and Management GUI. It can be installed from [their website](https://nodejs.org/)
- Unity is required for building the client application. It can be installed from [their website](https://unity.com/)
- You should also have a Unity project that you want to use as a client

### Installation

1. Install the RadishNet Server. See the [Server instructions](https://github.com/radishnet/radishnet-server/blob/main/README.md)
1. Install the RadishNet Client Unity Package into your project. See the [Unity Client instructions](https://github.com/radishnet/radishnet-client-unity/blob/main/README.md)
1. _(optional)_ Install the RadishNet Management GUI. See the [Management GUI instructions](https://github.com/radishnet/radishnet-management-gui/blob/main/README.md)

### Usage

1. Start the RadishNet Server. See the [Server instructions](https://github.com/radishnet/radishnet-server/blob/main/README.md)
1. Start your Client application. See the [Unity Client instructions](https://github.com/radishnet/radishnet-client-unity/blob/main/README.md)
1. (optional) Start the RadishNet Management GUI. See the [Management GUI instructions](https://github.com/radishnet/radishnet-management-gui/blob/main/README.md)

## Limitations

- RadishNet is _client-authorative_, which means that the server blindly trusts the clients, making it easy for clients to cheat. This is the main reason why you probably shouldn't use this framework for online multiplayer games. I chose client-authorative instead of server-authorative because it removes a lot of complexity (making the framework easier to customize) and it likely isn't necessary for the recommended use cases.
- Currently I only maintain a Unity plugin. You can also connect Unreal Engine or Godot clients to RadishNet but I just haven't built plugins for them. I may do that in the future though (see the Roadmap section).

## Roadmap

- Besides co-located users (i.e. users in the same physical location), I'm planning on adding support for distributed users (i.e. users in different physical locations) soon.
- I currently only maintain a Unity plugin but I'm thinking about building an Unreal Engine plugin too.

## Contact

- If you experience any issues, please use the Issues tab in the corresponding repository on GitHub.
- If you have ideas or suggestions, please use the Discussions tab on GitHub.
