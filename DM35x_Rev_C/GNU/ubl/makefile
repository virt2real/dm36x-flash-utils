all:
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216_LEGACY
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270_LEGACY
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_216
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_270
clean:
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216 clean
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270 clean
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216_LEGACY clean
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270_LEGACY clean
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_216 clean
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_270 clean
%::
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216 $@
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270 $@
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_216_LEGACY $@
		$(MAKE) -C build TYPE=NAND DEVICE=DM355_270_LEGACY $@ 
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_216 $@
		$(MAKE) -C build TYPE=NOR DEVICE=DM355_270 $@
		
