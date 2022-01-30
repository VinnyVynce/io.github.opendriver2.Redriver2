# io.github.opendriver2.Redriver2
A complete flatpak featuring the game and the launcher. Still under testing.

## Build
The following sdks/tools are required:
```
flatpak --user install flathub org.freedesktop.Platform/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Sdk/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Sdk.Compat.i386/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Sdk.Extension.toolchain-i386/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Sdk.Extension.openjdk11/x86_64/21.08 -y
```
Build it with a recent version of `flatpak-builder`
```
flatpak-builder --user --install build io.github.opendriver2.Redriver2.yaml --force-clean --arch=x86_64
```
if you want to create a flatpak for redistribution (unnecessary)
```
flatpak build-bundle ~/.local/share/flatpak/repo io.github.opendriver2.Redriver2.flatpak io.github.opendriver2.Redriver2
```
## Testing
The following runtimes are required:
```
flatpak --user remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak --user install flathub org.freedesktop.Platform/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Platform.Compat.i386/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Platform.GL32/x86_64/21.08 -y
flatpak --user install flathub org.freedesktop.Sdk.Extension.openjdk11/x86_64/21.08 -y
```
now, simply run your build or [install the latest release](https://github.com/VinnyVynce/io.github.opendriver2.Redriver2/releases).
