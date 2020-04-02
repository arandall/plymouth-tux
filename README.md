# Plymouth Tux

A small penguin adaptation of https://github.com/nilotpalbiswas/MacOS-Boot-Plymouth

Found out about this thing called plymouth, went on a voyage of discovery and had to make some tweaks.

## Installing

1. Download and copy to plymouth theme directory (eg. `/usr/share/plymouth/themes/tux`)
2. Set the default theme (eg. `sudo plymouth-set-default-theme tux`)
3. Update initial RAM disk `sudo update-initramfs -u`

**Note:** Paths are assuming that you're using Ubuntu/Mate, if your plymouth theme path is different then you'll need to
copy to a different location and update `tux.plymouth` to the correct location.

## Testing
1. Run plymouthd `sudo plymouthd --no-daemon --debug`
2. Test commands
    * `sudo plymouth show-splash`
    * `sudo plymouth ask-for-password --prompt "enter password"`
3. View output in first console (Ctl + Alt + F1), switch back to GUI console (likely Ctl + Alt +  F7)