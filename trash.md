*** REVIEW THIS and POSSIBLY TAKE IT OUT as its optional ***
## OPTIONAL - Come back to resolve as bonus
- To start dataikiu as a system-managed service, stop the instance `/home/khun/DATA_DIR/bin/dss stop`. Create a system service using install-boot script `sudo "/home/khun/INSTALL_DIR/dataiku-dss-12.2.3/scripts/install/install-boot.sh" "/home/khun/DATA_DIR" dataiku` and start the system service `sudo systemctl start dataiku`.

Ran into some issue starting the systemctl service: 

```
sudo systemctl start dataiku

Job for dataiku.service failed because the control process exited with error code. See "systemctl status dataiku.service" and "journalctl -xe" for details.

sudo systemctl status dataiku.service

● dataiku.service - LSB: starts the Dataiku DSS
   Loaded: loaded (/etc/rc.d/init.d/dataiku; bad; vendor preset: disabled)
   Active: failed (Result: exit-code) since Sat 2024-09-14 22:09:55 UTC; 14s ago
     Docs: man:systemd-sysv-generator(8)
  Process: 23318 ExecStart=/etc/rc.d/init.d/dataiku start (code=exited, status=1/FAILURE)

Sep 14 22:09:55 candidate-khun-phat-assessment-vm systemd[1]: Starting LSB: starts the Dataiku DSS...
Sep 14 22:09:55 candidate-khun-phat-assessment-vm dataiku[23318]: dataiku : starting Dataiku DSS
Sep 14 22:09:55 candidate-khun-phat-assessment-vm dataiku[23318]: su: user dataiku does not exist
Sep 14 22:09:55 candidate-khun-phat-assessment-vm systemd[1]: dataiku.service: control process exited, code=exited status=1
Sep 14 22:09:55 candidate-khun-phat-assessment-vm systemd[1]: Failed to start LSB: starts the Dataiku DSS.
Sep 14 22:09:55 candidate-khun-phat-assessment-vm systemd[1]: Unit dataiku.service entered failed state.
Sep 14 22:09:55 candidate-khun-phat-assessment-vm systemd[1]: dataiku.service failed.

```
To save time, I will come back to this issue at the at the later time.

*** REVIEW THIS and POSSIBLY TAKE IT OUT as its optional ***