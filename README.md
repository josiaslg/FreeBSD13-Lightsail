Files to compile FreeBSD 13-stable on Lightsail-512MB RAM. 
Before start, create the swap file (ram memory is to low for buildworld)

dd if=/dev/zero of=/usr/swap0 bs=256M count=8 && chmod 0600 /usr/swap0  && mdconfig -a -t vnode -f /usr/swap0 -u 0 && swapon /dev/md0
