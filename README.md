# Home SIEM Lab

### Project Overview

This project sets up a home lab for Elastic Stack Security Information and Event Management (SIEM) lab using the Elastic Web Portal and a Kali Linux VM. It aims to learn generating security events on Kali VM ,setting up an agent to forward data to the SIEM, and query and analyze the logs in the SIEM.

### Setup Essentials I Used
- Oracle VM Virtual Box
- Kali VM
- NMap tool
- Chrome Browser
  
### Overview of the tasks

- Setting up a free Elastic account.
- Configuring the Elastic Agent on the Linux VM to collect and forward logs to the SIEM.
- Generating security events on the Kali VM.
- Querying and analyzing security events in the Elastic SIEM.
- Creating a dashboard to visualize security events.
- Setting up alerts for security events.

## Setting up an Elastic Account
After registering, log in to the Elastic Cloud console at https://cloud.elastic.co. Click on "Start your free trial" to kick off the process.

## Setting up the Elastic Agent on the Linux VM 

#### Purpose of Elastic Agent

In order to effectively monitor security events on your Kali VM and ensure they're sent to your Elastic SIEM instance, we need to set up an agent. Agents play a crucial role in collecting and transmitting data from devices to a centralized system for analysis and monitoring.

#### Steps for Configuring the Elastic Agent on the Kali Linux to Collect and Forward Logs to the SIEM
1. In the Elastic Cloud console , Click "Add Integration" button in the bottom of the main Menu Bar.
2. Search for "Elastic Defend" and click on it to open the integration page.
3. Next, click on "Install Elastic Defend" and carefully follow the instructions provided on the integration page to install the agent on your Kali VM.
   - Make sure to select "Linux" and copy the provided command to your clipboard.
   - Paste the copied command into the terminal of your Kali VM and run it.
4. Once the installation process is complete, which may take a few minutes, you'll receive a confirmation message stating "Elastic Agent has been successfully installed." The agent will automatically start collecting and forwarding logs to your Elastic SIEM instance. However, it might take a few minutes for the logs to appear in the SIEM.
- Verify that the agent has been installed correctly, run the following command in your Kali terminal:
  
   sudo systemctl status elastic-agent.service
  



