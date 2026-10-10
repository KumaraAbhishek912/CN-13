# Wireshark Lab Experiment

## Aim
Study Wireshark for packet capture, filtering, protocol analysis, and network troubleshooting.

## Procedure
1. Open Wireshark and select the active Wi-Fi or Ethernet interface.
2. Start capturing and generate ordinary network traffic.
3. Stop and save the capture as `wireshark_capture.pcapng`.
4. Apply display filters: `tcp`, `udp`, `dns`, `tls`.
5. Inspect packet source, destination, protocol, and length.
6. Open Statistics → Protocol Hierarchy, Endpoints, and Conversations.
7. Save your actual screenshots in the `outputs` folder.

## Useful filters
- `tcp` — TCP packets
- `udp` — UDP packets
- `dns` — DNS traffic
- `tls` — TLS traffic
- `tcp.port == 443` — TCP traffic using port 443
- `ip.addr == 192.168.1.10` — replace with an IP from your capture

## Command line
List interfaces:
```bash
tshark -D
```

Capture for 20 seconds (replace `1` with your interface number):
```bash
tshark -i 1 -a duration:20 -w wireshark_capture.pcapng
```

Open a saved capture:
```bash
wireshark -r wireshark_capture.pcapng
```

## Files to add after running the experiment
- `wireshark_capture.pcapng`
- `outputs/output_1_packet_capture.png`
- `outputs/output_2_display_filter.png`
- `outputs/output_3_protocol_hierarchy.png`
- `outputs/output_4_endpoints.png`

## Result
Complete this section after performing the experiment and verifying your actual results.

**Safety:** Capture only traffic you are authorized to inspect. Review captures for sensitive information before publishing them publicly.
