# i8042-reset

i8042-reset is a Bash script for Linux that fixes an issue on Lenovo laptops where i8042-based keyboards stop
responding after the system resumes from suspend.

## Instructions

Depending on your preference, you may remove the `.sh` extension from the script.

1. Copy the `i8042-reset` file to `/usr/lib/systemd/system-sleep`
2. Make the script executable using `sudo chmod +x i8042-reset`

That's it! Your keyboard should now work correctly after resuming from suspend.

## Considerations

Placing the script in the `/usr` directory means it may be removed during system updates. If this happens and your
keyboard stops working, you can plug in an external keyboard to avoid a hard shutdown and restore the script.

## Troubleshooting

If this does not work, your laptop may use a different controller. In that case, consult the Linux community for
further assistance.

## Credits

All credit goes to the people who contributed to the solution in this
[Reddit thread](https://www.reddit.com/r/Fedora/comments/1mdiggp/no_keyboard_after_sleep/).
