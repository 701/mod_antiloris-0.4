# mod_antiloris-0.4

#### BUG
 ```
/apxs -aic mod_antiloris.c
/opt/lampp/build/libtool --silent --mode=compile gcc -std=gnu99 -prefer-pic -I/opt/lampp/include/c-client -I/opt/lampp/include/libpng -I/opt/lampp/include/freetype2 -O3 -fPIC -L/opt/lampp/lib -I/opt/lampp/include -I/opt/lampp/include/ncurses  -DLINUX -D_REENTRANT -D_GNU_SOURCE -pthread -I/opt/lampp/include  -I/opt/lampp/include/apr-1   -I/opt/lampp/include/apr-1 -I/opt/lampp/include  -c -o mod_antiloris.lo mod_antiloris.c && touch mod_antiloris.slo
			mod_antiloris.c: In function 'pre_connection':
			mod_antiloris.c:126: error: 'conn_rec' has no member named 'remote_ip'
			mod_antiloris.c:133: warning: passing argument 1 of 'ap_get_scoreboard_worker' makes pointer from integer without a cast
			/opt/lampp/include/scoreboard.h:193: note: expected 'struct ap_sb_handle_t *' but argument is of type 'int'
			mod_antiloris.c:133: error: too many arguments to function 'ap_get_scoreboard_worker'
			mod_antiloris.c:146: error: 'conn_rec' has no member named 'remote_ip'
			apxs:Error: Command failed with rc=65536
```

#### FIX 

> Edit by 701 from https://www.apachelounge.com/viewtopic.php?p=20543
