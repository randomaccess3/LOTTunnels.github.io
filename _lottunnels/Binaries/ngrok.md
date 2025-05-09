---
Name: ngrok
Description: Insiders as well as threat actors can ingress into an environment via ngrok, which functions as a reverse proxy. ngrok is no longer open source but the previous source code is still available (linked below).
Author: Dan O'Day
Created: 2025-01-31
Commands:
  - Command: ngrok authtoken 'AUTHTOKEN_GOES_HERE'
    Description: Initial ngrok configuration.
    Usecase: Configures ngrok to use specified authentication token.
    Category: Install
    Privileges: User
    OperatingSystem: Windows, Mac, Linux

  - Command: ngrok tcp|http <PORT>
    Description: Sends connection to configured upstream service on port.
    Usecase: Establishes reverse proxy via ngrok edge.
    Category: Access
    Privileges: User
    OperatingSystem: Windows, Mac, Linux

Full_Path:
  - Filename: ngrok.exe
  - Path: ngrok
Detection:
  - Domain: "*.ngrok.com"
  - Domain: "*.ngrok.io"
  - Domain: "*.ngrok.dev"
  - Domain: "*.ngrok.app"
  - Domain: "*.ngrok.pro"
  - Domain: "*.ngrok.pizza"
  - Domain: "*.ngrok-agent.com"
  - Domain: "*.ngrok-free.app"
  - Domain: "*.ngrok-cname.com"
  - Domain: "*.equinox.io"
  - Sigma: https://github.com/magicsword-io/LOLRMM/blob/main/detections/sigma/ngrok_network_sigma.yml
  - Sigma: https://github.com/magicsword-io/LOLRMM/blob/main/detections/sigma/ngrok_processes_sigma.yml
Resources:
  - Link: https://ngrok.com
  - Link: https://github.com/ngrok/ngrok
  - Link: https://github.com/inconshreveable/ngrok
  - Link: https://www.logpoint.com/en/blog/a-deep-look-at-the-darkside-ransomware-operators-and-their-affiliates/
Acknowledgement:
  - Person: Dan O'Day
    Handle: '@4n68r'
  - Person: Kirill Magaskin
    Handle: '@k1rpI7ch'
---
