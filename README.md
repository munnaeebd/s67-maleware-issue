# s67-maleware-issue

Problem-1: systemctl status S67

Recommend: systemctl stop S67


Problem-2: ls -la /etc/rc.d/init.d/S67

Recommend: rm -rf /etc/rc.d/init.d/S67


Problem-3: crontab -l 
~~~
1 1 */2 * * /tmp/.X25-unix/.rsync/a/upd>/dev/null 2>&1
5 8 * * 0 /tmp/.X25-unix/.rsync/b/sync>/dev/null 2>&1
@reboot /tmp/.X25-unix/.rsync/b/sync>/dev/null 2>&1
0 0 */3 * * /tmp/.X25-unix/.rsync/c/aptitude>/dev/null 2>&1
~~~

Recommend: Remove above mentioned cronjob (crontab -e; and remove one by one). rm -rf /tmp/.X25-unix/

Problem-4: ls /.a/mass2ip/

Recommend: 

rm -rf /.a/mass2ip/

ps -aux | grep mass

kill -9 pid



