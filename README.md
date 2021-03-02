# HotShots_flatpak
Screen capture and add annotations and graphical data to it


### Build
```
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
sudo flatpak install flathub org.kde.Sdk/x86_64/5.15 org.kde.Platform/x86_64/5.15

git clone https://github.com/fastrizwaan/HotShots_flatpak.git
cd HotShots_flatpak/
flatpak-builder --force-clean build-dir io.github.HotShots.yml
flatpak-builder --install --user --force-clean build-dir io.github.HotShots.yml
```
#### Run
`flatpak run io.github.HotShots.yml`
