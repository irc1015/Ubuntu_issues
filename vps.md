1. run `Hysteria2` client 

   ```log
   ./hysteria-linux-amd64 -c v.yaml
   ```

2. install `deb` application

   ```log
   sudo dpkg -i 软件包名.deb
   ```

   uninstall `deb` application

   ```
   sudo apt-get remove 软件包名称
   ```

3. VPS

   ```log
   systemctl restart hysteria-server.service
   systemctl start hysteria-server.service
   systemctl enable hysteria-server.service
   systemctl status hysteria-server.service
   systemctl enable --now hysteria-server.service
   ip6tables -t nat -A PREROUTING -i enp1s0 -p udp --dport 20000:50000 -j REDIRECT --to-ports 7892
   iptables -t nat -A PREROUTING -i enp1s0 -p udp --dport 20000:50000 -j REDIRECT --to-ports 7892
   ifconfig
   sudo ufw allow 20000:50000/tcp
   sudo ufw reload
   sudo ufw status numbered
   
   ```

   

4. 