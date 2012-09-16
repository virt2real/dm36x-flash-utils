all:
		$(MAKE) -C build TYPE=dm365sdmmc
		$(MAKE) -C build TYPE=dm368sdmmc
clean:
		$(MAKE) -C build TYPE=dm365sdmmc clean
		$(MAKE) -C build TYPE=dm368sdmmc clean
%::
		$(MAKE) -C build TYPE=dm365sdmmc $@
		$(MAKE) -C build TYPE=dm368sdmmc $@
		
