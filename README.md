# Implementing a git server on the Raspberry Pi 4

Project members:
Alexandra Chambers
Alexander Dao
Turhan Kimbrough
Vince Lepatan

Secure Shell (SSH), ngrok, and git are used to implement the git
server on the Raspberry Pi 4 device.

(On local machine)
    • flash the latest version of an ARM-based Operating System on a microSD card
    • place an empty file called ‘ssh’ in the root of the microSD card
    • Place a file into the boot directory called wpa_supplicant.conf and place the contents below inside the file:
	ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
	update_config=1
	country=US

	network={
 	    ssid="<Wireless LAN info here>"
 	    psk="<Wireless LAN password here>"
	}

(On Raspberry Pi)
    • Place the microSD card into the Raspberry Pi and connect it to a power source

(Back to local host)
    • Make a free ngrok account at https://ngrok.com/
    • Create a remote terminal session via ssh by typing ssh pi@XX.XX.XX.XXXX
    • Type in credentials (Username: Pi, Password: Raspberry)

(On Raspberry Pi remotely)
    • Install git with sudo apt-get install git
    • Install ngrok with:
	sudo wget https://dl.ngrok.com/ngrok_2.0.19_linux_arm.zip (download zip)
	sudo unzip ngrok_2.0.19_linux_arm.zip (unzip folder)
	Login to website and get authentication token
	./ngrok authtoken <authentication token>

