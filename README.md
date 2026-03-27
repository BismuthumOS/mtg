1. GENERATE TOKEN:
docker run --rm nineseconds/mtg:2 generate-secret --hex google.com

2. START MTG VIA DOCKER:
docker compose up -d

3. MONITOR YOUR SNI FAKE-TLS CONNECTIONS:
tshark -i any -f "tcp port 443" -Y "tls.handshake.extensions_server_name contains google.com"

