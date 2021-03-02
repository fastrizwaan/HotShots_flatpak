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

#### Build a flatpak bundle file from the above built repo:
```
flatpak-builder --repo="repo" --force-clean "build" io.github.HotShots.yml
flatpak --user remote-add --no-gpg-verify "io.github.HotShots" "repo"
flatpak build-bundle "repo" "io.github.HotShots.flatpak" io.github.HotShots  --runtime-repo="https://flathub.org/repo/flathub.flatpakrepo"

flatpak --user install io.github.HotShots.flatpak
flatpak run io.github.HotShots
```
