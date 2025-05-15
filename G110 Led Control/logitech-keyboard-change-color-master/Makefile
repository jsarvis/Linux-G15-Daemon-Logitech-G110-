all: Logitech_G110_change_color

Logitech_G110_change_color::
	gcc -o Logitech_G110_change_color Logitech_G110_change_color.c -lusb

install: Logitech_G110_change_color
	cp Logitech_G110_change_color /usr/bin/gcolor
	chmod +x /usr/bin/gcolor

uninstall:
	rm -f /usr/bin/gcolor
