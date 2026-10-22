## Setup
1. Set host's ip address as main DNS server in your router DNS setting
2. AdGuardHome Settings
    - Settings 
        - DNS settings
            - Upstream DNS servers
                - Add these to DNS list
                    - https://dns.cloudflare.com/dns-query
                    - https://dns10.quad9.net/dns-query
                - Enable: Parallel requests
        - DNS cache configuration
            - Cache size: 33554432
            - Override minimum TTL: 2400
            - Override maximum TTL: 84600
    - Filters 
        - DNS rewrites
            - *.jackdawmd.duckdns.org - <host's ip address>
        - DNS blocklists
            - Enable: AdAway Default Blocklist
            - Add: VNM ABPVN List
