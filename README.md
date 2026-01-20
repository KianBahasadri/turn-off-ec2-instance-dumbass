# turn-off-ec2-instance-dumbass

## What this does

Sends a Twilio SMS every hour from a systemd service. The installer pulls your
Twilio creds from `twilio_hourly_sms.env` and generates a standalone script in
`~/.local/bin/` (or `/usr/local/bin/` with sudo).

This allows you to safely delete this repository after installation.

If `twilio_hourly_sms.env` is missing or any required values are empty, the
installer exits with an error and the service will not be installed.

## Setup

1. Fill out `twilio_hourly_sms.env` with your Twilio values.
2. Run `./install_twilio_hourly_sms_service.sh` (use sudo for a system service).
3. (Optional) Delete this repository.

Re-run the install script any time you update `twilio_hourly_sms.env`.