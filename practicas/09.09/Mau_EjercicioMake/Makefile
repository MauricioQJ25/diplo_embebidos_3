all: my-thing-python.ipk

my-thing-python.ipk:
	rm -rf ipk
	mkdir -p ipk/opt/my-thing-python
	cp *.p ipk/opt/my-thing.python
	tar czvf control.tar.gz control	
	cd ipk; tar czvf ../data.tar.gz .; cd ..
	echo 2.0 > debian-binary
	ar r my-thing-python.ipk control.tar.gz data.tar.gz debian-binary

clean: FORCE
	rm -rf ipk
	rm -f control.tar.gz
	rm -f data.tar.gz
	rm -f my-thing-python.ipk
