# Sample Makefile using Atdgen.mk and OCamlMakefile.

.PHONY: default
default: opt all

ATDGEN_SOURCES = hello.atd
ATDGEN_FLAGS = -j-std
include ../Atdgen.mk

SOURCES = hello_t.mli hello_t.ml hello_j.mli hello_j.ml hello.ml
RESULT = hello
PACKS = atdgen
# "include OCamlMakefile" must come after defs for SOURCES, RESULT, PACKS, etc.
include OCamlMakefile

.PHONY: sources opt all
sources: $(SOURCES)
opt: sources
	$(MAKE) native-code
all: sources
	$(MAKE) byte-code
