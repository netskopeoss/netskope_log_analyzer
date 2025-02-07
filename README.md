# About Netskope Log Analyzer

![Log Analyzer image](static/Dashboard.PNG)

We've received feedback that Netskope logs are primarily written for developers, making them challenging for users and support teams to interpret. To address this, this tool provides a clear visualisation of key information—such as configured settings, the PoP the client connected to, and how traffic was handled—through intuitive graphs and tables. We hope this will be helpful for troubleshooting.

## Getting Started

This add-on works on both Linux and Mac. For Mac users, please download the Intel version of the Splunk installer and run it using Rosetta. Follow the installation instructions provided by macOS and Splunk.

### Note:

This add-on creates the following indexes on the Splunk server and stores log data in them.
We recommend setting up and using a separate Splunk server from the production environment.

* netskope_client1
* netskope_json1
* netskope_publisher1
* netskope_csv1

### Installation

 1. Please create a folder at the following location. Splunk will monitor this folder and start indexing logs as soon as it detects client log folder.

    ```sh
    mkdir -p  /var/log/splunk/logs
    chmod 777 /var/log/splunk/logs
    ```

 2. Place the Add-on folder in the Splunk apps directory.

    For Linux user:
    ```sh
    cd /opt/splunk/etc/apps/
    git clone https://github.com/netskopeoss/netskope_log_analyzer.git
    ```

    For Mac user:
    ```sh
    cd /Applications/Splunk/etc/apps
    git clone https://github.com/netskopeoss/netskope_log_analyzer.git
    ```

 3. Please restart Splunk to enable the add-on.


 4. Extract the Netskope log bundle and upload it to /var/log/splunk/logs. Splunk will detect the logs and start indexing them.
    

 5. Access the dashboard(http:// Your Splunk server's IP address:8000/en-GB/app/netskope_log_analyzer/) and select the log folder name from the dropdown menu.
    The data will be displayed on the dashboard.Tabs are organized by functionality. Open each tab in a new browser tab and repeat the steps above.

    ![Log Analyzer image](static/Dashboard2.PNG)

## License

See LICENSE for more information
