# Enable DNS Server on a specific interface

## Check your current dns forwarders

`show system dns`

## modify your forwarders if needed

```
config system dns
  set primary 1.1.1.1
  set secondary 1.0.0.1
end
```

## Identify the interface you want to listen for client requests on (whether a physical port or aggregate like "internal")

`show system interface` **look for the interface you want to associate with DNS services**

## Change your focus to the dns server

`config system dns-server`

## Switch to the Interface you want to associate

`edit "internal"`

## Enable dns forwarding

`set mode forward-only`

## finish

`end`
