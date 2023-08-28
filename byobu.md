___
# BYOBU
Links: [[Linux]]
Status: #🌳 
Tags: [[]]

<!--- Created on: 2023.08.28, 18:24 --->

- text-based terminal multiplexer for Linux systems
- built on top of the GNU Screen or Tmux
- providing features like session management, split windows, and customizable status bars
- sessions remain active even if disconnected or logged out

___

| What                               | How                                   | Shortcut      |
| ---------------------------------- | ------------------------------------- | ------------- |
| List all running sessions          | `byobu list-session`                  |               |
| Select a running session from list | `byobu-select-session `               |               |
| Create a new session               | `byobu new -s <sessionname>`          | CTRL+SHIFT+F2 |
| Rename a running session           |                                       | CTRL+F8       |
| Open a running session             | `byobu attach -t <sessionname>`       |               |
| Close running session              | `byobu detach –t <sessionname>`       | F6            |
| Kill a running session             | `byobu kill-session –t <sessionname>` |               |
| Enable Scrolling                   |                                       | F7            |