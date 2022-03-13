# Kismet

## Installation

    wget -O - https://www.kismetwireless.net/repos/kismet-release.gpg.key | sudo apt-key add -
    echo 'deb https://www.kismetwireless.net/repos/apt/release/kali kali main' | sudo tee /etc/apt/sources.list.d/kismet.list
    sudo apt update
    sudo apt install kismet

## Launching Kismet

    kismet
    sudo for webserver?

    kismet -c wlan0
