## Usage Examples

### Interface Configuration

Show/dump/import active config
```cmd
    netsh interface ip show config
    netsh interface ip show config <interface>
    
    netsh -c interface dump > config.txt     # dump config
    netsh -f config.txt                      # import config
```
Static IP
```cmd
    netsh interface ip set address local static [ip] [netmask] [gw] 1
 ```   
DHCP 
```cmd
    netsh interface ip set address local dhcp
    netsh interface ip set dns <NIC name> dhcp        # Ensure to get DNS servers via DHCP
  ```  
DNS

Overwrite currrent DNS config with a single static DNS server
```cmd
    netsh interface ipv4 set dns <NIC name> static <dns server> primary
```   
Add DNS servers
```cmd
    netsh interface ipv4 add dnsserver <NIC name> address=<dns server> index=<nr>
  ```  
### Routes
```cmd
    netsh interface ipv4 show route
    
    netsh interface ipv4 add    route x.x.x.x/x <interface name> <gw>
    netsh interface ipv4 delete route x.x.x.x/x <interface name> <gw>
```    
### Firewall

Note "netsh firewall" is deprecated since Vista. Use "netsh advfirewall firewall" instead!

#### Config dumping
```cmd
    netsh advfirewall firewall export c:\temp\wfas.wfw
    netsh advfirewall firewall import c:\temp\wfas.wfw
    
    netsh advfirewall firewall reset [export  c:\temp\wfas.wfw]
```    
#### Toggling states
```cmd
    netsh advfirewall firewall set [profiletype]state on
    netsh advfirewall firewall set [profiletype]state off
```    
#### Changing rules
```cmd
    netsh advfirewall firewall add rule name="newrule" dir=in action=allow program="%ProgramFiles%\some\program.exe"
    
    netsh advfirewall firewall show rule "newrule" verbose
    
    netsh advfirewall firewall set rule group=”Windows Firewall Remote Management” new enable =yes
```    
