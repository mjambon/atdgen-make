# Sample Makefile using Atdgen.mk and OCamlMakefile.
# Note that the program does nothing.

include ../Atdgen.mk
.PHONY: default
default: opt all

ATDGEN_SOURCES = hello.atd
ATDGEN_FLAGS = -j-std
TRASH += $(ATDGEN_OUTFILES)

SOURCES = hello_t.mli hello_t.ml hello_j.mli hello_j.ml
RESULT = hello
PACKS = atdgen
include OCamlMakefile

.PHONY: sources opt all
sources: $(SOURCES)
opt: sources
	$(MAKE) native-code
all: sources
	$(MAKE) byte-code
