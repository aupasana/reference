# VPN

The following zsh functions are useful for starting and stopping the PIA VPN

```zsh
function pia-helper-ip() {
    pubip=$("/Applications/Private Internet Access.app/Contents/MacOS/piactl" get pubip)
    vpnip=$("/Applications/Private Internet Access.app/Contents/MacOS/piactl" get vpnip)
    pia_ip_string=$(echo "pubip: $pubip vpnip : $vpnip")
    echo $pia_ip_string
}

function pia-inner() {
    pia-helper-ip
    pia_start_ip=$pia_ip_string
    echo "Performing action $1"
    "/Applications/Private Internet Access.app/Contents/MacOS/piactl" $1
    repeat 5 { 
        sleep 1
        pia-helper-ip
        if [[ $pia_start_ip != $pia_ip_string ]]
        then
            return
        fi
    }
}

function pia() {
    pia-inner connect
}

function pia-stop() {
    pia-inner disconnect
}

function pia-status() {
    region=$("/Applications/Private Internet Access.app/Contents/MacOS/piactl" get region)
    state=$("/Applications/Private Internet Access.app/Contents/MacOS/piactl" get connectionstate)
    echo "PIA Status: $state in $region"
}
```
