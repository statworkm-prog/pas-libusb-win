EXECUTABLES = test1library test2controlsync test3controlasync testfirmware
#when running on windows, add "-Px86_64 -Twin64"
FPC_OPTS = -Fu..
ifeq ($(OS), Windows_NT)
	FPC_OPTS += -Fu.. -Px86_64 -Twin64
endif

all: $(EXECUTABLES)

%: %.pas
	fpc $(FPC_OPTS) $<

clean:
	rm -f *.o *.ppu *~ *.bak $(EXECUTABLES)
