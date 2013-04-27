install: coldstart

coldstart: .FORCED
ifdef ANTELOPE
	CNSN_LOCAL=/opt/cnsn_local/`getid id`; export CNSN_LOCAL; \
	CNSN_LOCALMAKE=/opt/cnsn_local/`getid id`/include/cnsn_localmake; export CNSN_LOCALMAKE; \
	( cd ../setup; make install ) ; \
	( cd ../../lib/makerules; make install ) ; \
	( cd ../..; make Include ) ; \
	mkdir /opt/cnsn_local/`getid id`/man ; \
	( cd ../..; make install )
else
	@echo ""
	@echo "The ANTELOPE environment variable is not set." 
	@echo "Please run setup.csh or setup.sh according to the"
	@echo "setup.csh(1) man-page for BRTT Antelope software."
	@echo ""
	@exit 1
endif

.FORCED:
