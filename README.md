##winconfig - Windows Configuration Modules
###for use with Puppet Enterprise 3.x

The module will provide parameter-based configuration for managing the state of Windows Server with Puppet Enterprise.  While there are excellent modules that currently exist to manage roles and features, this module will focus on configuration the low level system settings, such as SNMP, UAC and more.

### Available Resources

    winconfig::snmp          - Configure SNMP settings
    winconfig::uac           - Configure UAC settings
    winconfig::searchdomains - Configure DNS search domains

### Dependencies

    > puppet module install puppetlabs-registry
    > puppet module install joshcooper-powershell

### Usage

####winconfig::uac

  **Parameters**
  
  `enable => present || absent` - Enable or disable User Account Control (UAC)

####winconfig::snmp

  **Parameters**

  `enable      => present || absent`   - Enable or disable SNMP Service

  `contact     => <contact info>`      - Contact email address

  `location    => <location info>`     - Location information

  `community   => <community string>`  - Community String

  `destination => <trap server>`       - SNMP Trap Destination Server

####winconfig::searchdomains

  **Parameters**

  `domains => 'example.com,example2.com'` - Comma-Seperated list of domain names
