# 0 A.D. - Packaging mod

This mod is used to package other mods for 0 A.D. It contains the skeletons from the public mod, as well as the textures.xml files for the textures you might have in your mod. Those files are needed in order to package files that are dependent of the public mod, and to compress textures correctly. Incorrectly packaged textures = crash.

## Usage

- Clone the repository
- Copy the mod to your game installation folder.
- Go to binaries\system\ and open a terminal command.
- Type something like:

```lang=sh
$ pyrogenesis -mod=package_mod -archivebuild="..\data\mods\{yourmod}" -archivebuild-output="{yourmod}.pyromod" -archivebuild-compress
```

- Get your mod from binaries/system.
- Share it.

## Improvements 

- This mod assumes that AO maps do not have transparency. You need to ensure that else your package will be broken.

Reason: → AO maps do not use the transparency, and that makes the compressed version smaller.
