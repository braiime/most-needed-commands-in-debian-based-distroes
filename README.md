# most-needed-commands-in-debian-based-distroes

# vs code install
1- pre:
sudo apt update
sudo apt install -y wget gpg software-properties-common apt-transport-https
2- Microsoft GPG key:
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/packages.microsoft.gpg
3- download VS Code repository:
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list
4- install it:
sudo apt update
sudo apt install -y code
note: vs code in not officialy supported on debian

a lot will be here soon
