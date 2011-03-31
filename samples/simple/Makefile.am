TARGETS=simple.exe

SOURCES = \
	$(srcdir)/Simple.cs

EXTRA_DIST = $(SOURCES)

ASSEMBLY=$(ASSEMBLY_NAME).dll

CLEANFILES = $(TARGETS) $(DEBUGS) $(assembly)

REFS=-r:../../sources/$(ASSEMBLY) -pkg:gtk-sharp-2.0

all: $(TARGETS)

$(ASSEMBLY): ../../sources/$(ASSEMBLY)
	cp ../../sources/$(ASSEMBLY) $(srcdir)

simple.exe: $(ASSEMBLY) $(SOURCES)
	$(CSC) /out:$@ $(REFS) $(SOURCES)
