# Network basics

**check response time from a domain or ip address**

```cmd
ping www.bing.com
```

**check machine host name**

```cmd
hostname
```

**check machine MAC address**

```cmd
getmac
```

**get basic info on the network**

```cmd
ipconfig /all
```

**release the current IP address**

```cmd
ipconfig /release
```

**renew the IP address**

```cmd
ipconfig /renew
```

**flush the dns cache**

```cmd
ipconfig/flushdns
```

**show the ARP (address resolution cache)**

```cmd
arp -a
```

**dns lookups**

```cmd
nslookup
```

**manage users, service, shares**

```cmd
net
```

**TCP and UDP connections and ports**

```cmd
netstat
```

**troubleshoot netBIOS**

```cmd
nbtstat
```

# Capture network packets

## Setup

**list network adapters**

```cmd
pktmon comp list
```

**list the current filters**

```cmd
pktmon filter list
```

**add ports to monitor**

```cmd
pktmon filter add -p 80
pktmon filter add -p 81
```

## Run

**start logging packets for the added ports on ALL interfaces**

```cmd
pktmon start --etw
```

**start logging packets for the added ports on ALL interfaces**
*outputs to the console and captures to pktmon.etl file*

```cmd
pktmon start --etw --log-mode real-time
```

**start logging complete packets from the specified interface**

```cmd
pktmon start --etw -p 0 -c 16
```

**stop logging**
    
```cmd
pktmon stop
```

## Output

**format the output file to text**
    
```cmd
pktmon format PktMon.etl -o packets.txt
```

**format the output file to PCAPNG format so you can open it in Wireshark**

```cmd
pktmon pcapng PktMon.etl -o packets.pcapng
```

*Download the [Microsoft Network Monitor](https://docs.microsoft.com/en-us/windows/client-management/troubleshoot-tcpip-netmon) to set up catures in the GUI and open the ETL file directly :-)*