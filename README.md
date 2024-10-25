# New macOS Setup for iOS Development

This guide provides a complete setup for a new macOS environment specifically tailored for iOS development. It includes essential applications, tools, and configurations to ensure a smooth and efficient development experience. Follow these steps to quickly set up your development, productivity, and system tools.

## Table of Contents

- [Development](#development)
- [Productivity](#productivity)
- [Tools](#tools)
- [System](#system)
- [Other](#other)
- [Development Environment Setup](#development-environment-setup)
- [Terminal Environment Setup](#terminal-environment-setup)
- [Additional Recommendations](#additional-recommendations)
- [Notes](#notes)

## Development

| Icon | Name           | Description                                                                                 | Link                                                                                      | Brew Installable |
|------|----------------|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|------------------|
| 🛠️   | **Xcode**      | Apple's official IDE for macOS development.                                                | [Xcode on Mac App Store](https://apps.apple.com/us/app/xcode)                             | No               |
| 🐙   | **GitKraken**  | Cross-platform Git GUI client with advanced features.                                      | [GitKraken](https://www.gitkraken.com/)                                                   | No               |
| ⏱️   | **Buildwatch** | Tool to monitor and analyze Xcode build times for performance optimization.                 | [Buildwatch](https://build.watch/)                                                        | No               |
| 🛠️   | **DevUtils**   | Toolbox for developers with utilities accessible directly from your Mac menu bar.          | [DevUtils](https://devutils.app/)                                                         | No               |
| 🌐   | **Proxyman**   | Modern and intuitive HTTP debugging proxy for macOS.                                        | [Proxyman](https://proxyman.io/)                                                          | No               |
| 📥   | **Xcodes**     | Simple app to install and manage multiple versions of Xcode.                                | [Xcodes](https://github.com/RobotsAndPencils/XcodesApp)                                   | Yes              |

## Productivity

| Icon | Name              | Description                                                      | Link                                                                 | Brew Installable |
|------|-------------------|------------------------------------------------------------------|----------------------------------------------------------------------|------------------|
| 📝   | **MacDown**       | Open source Markdown editor for macOS.                           | [MacDown](https://macdown.uranusjr.com)                              | No               |
| 🌞   | **MonitorControl** | Control external monitor brightness & volume on your Mac.        | [MonitorControl](https://github.com/MonitorControl/MonitorControl)   | Yes              |
| 📋   | **Bartender**     | Organize and declutter your Mac's menu bar icons.                | [Bartender](https://www.macbartender.com/)                           | No               |
| 🔄   | **One Switch**    | Access various system settings quickly from your menu bar.       | [One Switch](https://fireball.studio/oneswitch/)                     | No               |
| 🎧   | **AirBuddy**      | Seamlessly connect and manage AirPods and other devices.         | [AirBuddy](https://v2.airbuddy.app/)                                 | No               |
| 🤖   | **ChatGPT**       | Desktop app for interacting with OpenAI's ChatGPT language model. | [ChatGPT](https://chat.openai.com/)                                  | No               |

## Tools

| Icon | Name           | Description                                               | Link                                        | Brew Installable |
|------|----------------|-----------------------------------------------------------|---------------------------------------------|------------------|
| 🍺   | **Homebrew**   | Package manager that simplifies installing software.     | [Homebrew](https://brew.sh/)                | Yes              |
| 🖌️   | **Oh My Zsh**  |Framework for managing Zsh configuration and themes.| [OhMyZsh](https://ohmyz.sh)|No |
| 🤖   | **Powerlevel10k** | A prompt theme for Zsh with many customization options. | [Powerlevel10k](https://github.com/romkatv/powerlevel10k) | Yes (`brew install powerlevel10k`) |

## System

| Icon | Name                          | Description                                              | Link                                                                                                                                             | Brew Installable |
|------|-------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| 🔑   | **SSH Setup**                 | Generate a new SSH key and add it to the ssh-agent.      | [GitHub SSH Guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) | No               |
| 🔓   | **Touch ID and Apple Watch Unlock** | Unlock your Mac using Touch ID or Apple Watch. | Built-in macOS feature (See **System Preferences > Security & Privacy**)                                   | No               |

## Other

| Icon | Name                  | Description                                  | Link                                                                               | Brew Installable |
|------|-----------------------|----------------------------------------------|------------------------------------------------------------------------------------|------------------|
| 🔒   | **Touch ID for sudo** | Enable Touch ID for sudo in Terminal.        | [Instructions](https://gist.github.com/windyinsc/26aaa8783c7734529998062a11d80b96) | No               |

*Feel free to recommend others.*

## Development Environment Setup

1. **Create a Development Directory:**

   ```bash
   mkdir ~/Dev
   ```

2. **Install Homebrew:**

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

3. **Install Git:**

   ```bash
   brew install git
   ```

4. **Set Up SSH Keys:**

   Follow [GitHub's guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) to generate a new SSH key and add it to the ssh-agent.

5. **Install GitKraken, Xcode, Proxyman, DevUtils, Buildwatch, Xcodes** (see links above).

## Terminal Environment Setup

1. **Install iTerm2** (see link above).

2. **Install Oh My Zsh:**

   ```bash
   sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

   After installing Oh My Zsh, install **Powerlevel10k** theme:

   ```bash
   brew install powerlevel10k
   echo "source $(brew --prefix)/share/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc
   ```


3. **Enable Touch ID for sudo in Terminal:**

   Follow the instructions [here](https://gist.github.com/windyinsc/26aaa8783c7734529998062a11d80b96).

4. **Configure iTerm2 with Your JSON Config:**

   - Import your iTerm2 profile JSON file via **iTerm2 > Preferences > Profiles > Other Actions > Import JSON Profiles**.

## Additional Recommendations

- **Slack:** Team communication. [Download](https://slack.com/downloads/mac)

- **Postman:** API development environment. [Download](https://www.postman.com/)

- **Docker Desktop:** Containerize applications. [Download](https://www.docker.com/products/docker-desktop)

- **Visual Studio Code:** A popular code editor. [Download](https://code.visualstudio.com/)

## Notes

- Remember to import your iTerm2 config JSON file.
- Place your Xcode theme files in the appropriate directory:

  ```bash
  mkdir -p ~/Library/Developer/Xcode/UserData/FontAndColorThemes/
  ```

- Enable Touch ID and Apple Watch unlock in **System Preferences > Security & Privacy**.
