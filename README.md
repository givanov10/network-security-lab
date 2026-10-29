Network Security and Connection Verification

1. External Connection Verification:
   - Command executed: ping -c 4 8.8.8.8
   - Result: Successful connection, 0% packet loss.

2. Audit of Open Ports:
   - Command executed: sudo ss -tuln
   - Result: Confirmed that the SSH service is listening on 0.0.0.0:22 (LISTEN).

3. Server Protection with ufw:
   - Initial status check: inactive
   - Rule added: sudo ufw allow 22/tcp
   - Firewall activated: sudo ufw enable
   - Control check (sudo ufw status verbose): Status is active, port 22/tcp is ALLOW IN.
