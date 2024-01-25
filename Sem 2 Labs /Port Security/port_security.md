### Port security:

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/e806a204-71cb-4b40-9d61-0c6fc76e6d7d)

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/a1b0790b-a726-4870-a7f7-cb5f55d02338)

In the above screenshot we can see that the port-security is disabled by default. To enable port
security we must configure the interface and allow switchport access.


![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/a652ce07-68ae-41cf-95a1-bd21f1987452)

Shutdown: When a port security violation occurs, the switch can be configured to shut down the
port. This means the port is effectively disabled, preventing any further communication through that
port. This helps in containing potential security threats.

Restrict: In this mode, the port still forwards traffic, but it limits the number of MAC addresses that
can access the port. Any additional MAC addresses beyond the configured limit will trigger a
violation.

Protect: In this mode, the port still forwards traffic, but it does not learn new MAC addresses. This
means that only the initially learned MAC address is allowed on the port, and any new MAC
addresses are ignored.

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/d4c2c9c4-bff9-424b-b326-7b3569e8a3e2)

Maximum MAC Addresses: This option allows us to set the maximum number of allowed MAC
addresses on a port.

Sticky MAC Addresses: This option allows the switch to dynamically learn and retain the MAC
addresses of devices connected to the port.

Aging Time: This option sets the time for which dynamically learned MAC addresses are retained in
the port security table. When the aging time expires, the MAC address is removed from the table.

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/0c9eb3be-2b54-4721-92e8-ca10fdc55364)


![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/69bead0f-9926-4642-8abd-f0622b0acd96)

We’ve configured the port security
To test the port security I have modified the existing topology, assign the respective IP’s for the end
devices and check the connectivity.

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/a99c525a-27ea-4c2b-b988-0898d74035cf)

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/e4b10767-2ca1-48dd-98d5-fd709a04b7e4)

![image](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/aeddbb8d-472b-4652-845d-39244694189e)

We’ve set the max mac address as 1 which means that when we try to ping from different end
device, the connection will be timed out.


![port_security violated restrictions](https://github.com/jayshah17/Packet-Tracer-Labs/assets/76842630/3e03873f-9c48-4202-b531-f290dd42fbae)

