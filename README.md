# How to install yabai for fast space shift

##**Step 1: Sip Disable**

Shut your mac down, turn it back on holding power button until you see, startup options text on screen.

Then type in your password and proceed with opening up a terminal session.
type in:
!!! warning 
	csrutil disable

type your password in then reboot.

Once booted into the Operating System check system integrity status by
!!! warning 
	csrutil status

Should return 
!!! warning 
	System Integrity Protection status: disabled.


##**Step 2: Installation**

> !~orange;default;default;7; %black% **Install brew if missing.** %% ~!

!!! warning 
	brew install koekeishiya/formulae/yabai

	sudo yabai --load-sa

	brew install jq

	brew install koekeishiya/formulae/skhd

##**Step 3: Configuration**

!!! warning 
 
	mkdir $HOME/.config/yabai/

	mkdir $HOME/.config/skhd/

	touch $HOME/.config/yabai/yabairc

	touch $HOME/.config/skhd/skhdrc

	chmod +x $HOME/.config/yabai/yabairc

	chmod +x $HOME/.config/skhd/skhdrc

!!! warning 

	nano $HOME/.config/skhd/skhdrc

	alt - right : yabai -m space --focus next
	alt - left : yabai -m space --focus prev
 

Reboot

##**Step 4: Finalizing**
!!! warning 
	sudo yabai --load-sa

	yabai --start-service

	skhd --start-service