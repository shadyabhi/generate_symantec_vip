# generate_symantec_vip

Creating this repo because I always forget how to generate credentials.

## Build Instructions

	git clone https://github.com/shadyabhi/generate_symantec_vip
	sudo docker build -t generate_symantec_vip .

	# Make sure you've tool to generate tokens
	brew install oath-toolkit

## How to use?

NOTE: These credentials are not in use.

To generate a token, execute:-
	
	sudo docker run -it generate_symantec_vip /opt/generate.py

This generates the VIP URL like this:-

	otpauth://totp/VIP%20Access:VSMT42722368?secret=KJBVML75XJBA2MGEZBPYN2222OI7QBSK&issuer=Symantec

It contains the following information for registering on a portal. 

	Credential ID: VSMT42722368
	OTP Secret: KJBVML75XJBA2MGEZBPYN2222OI7QBSK

To generate a OTP:-

	/usr/local/bin/oathtool --totp -b KJBVML75XJBA2MGEZBPYN2222OI7QBSK
