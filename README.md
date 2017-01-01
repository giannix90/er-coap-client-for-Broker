# er-coap-client-for-Broker

This is a simple CoAP client implemented ith Erbium that send a request to aaaa::1/16 interface created by tunslip6
and can be used for test the Broker server with cooja.

-We have to use also the border router with code /home/contiki/examples/ipv6/rpl-border-router/border-router.c

## Instruction

1. Create a simple network in cooja with only 2 motes: the border router and this CoAP client.
2. Add a serial socket to the border router (cooja->Tools->Serial Socket(SERVER)) and start the listen
3. Run tunslip with this commands:
    $ cd contiki/tools
    $ sudo ./tunslip6 -a 127.0.0.1 aaaa::1/64
4. Start the Broker server in java
5. Interact with the broker with this client and with Copper together

N.B. Copper must send request to coap://[aaaa::0:0:0:1]:5683
