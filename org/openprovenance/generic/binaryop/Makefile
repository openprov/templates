
TARGET=target

expansion:
	provconvert -infile $(IN) -bindings $(BIND) -bindver 3 -outfile $(OUT)


test1:
	$(MAKE) IN=1.provn BIND=1/b1.json OUT=$(TARGET)/g1b1.provn expansion
