PACKAGE_STY = $(wildcard source/*.sty)
DEMO_PDF = demo/demo.pdf
DEMO_SRC = demo/demo.tex

DESTDIR     ?= $(shell kpsewhich -var-value=TEXMFHOME)
INSTALL_DIR = $(DESTDIR)/tex/latex/common
CACHE_DIR   := $(shell pwd)/.latex-cache
COMPILE_TEX := latexmk -pdf -output-directory=$(CACHE_DIR)

export TEXINPUTS:=$(shell pwd):$(shell pwd)/source:${TEXINPUTS}
.PHONY: all demo doc install uninstall ctan clean-cache clean

all: demo

clean: clean-cache

clean-cache:
	@rm -rf "$(CACHE_DIR)"

install: $(PACKAGE_STY)
	@mkdir -p $(INSTALL_DIR)
	@cp $(PACKAGE_STY) $(INSTALL_DIR)

uninstall:
	@rm -f "$(addprefix $(INSTALL_DIR)/, $(PACKAGE_STY))"
	@rmdir "$(INSTALL_DIR)"

demo: $(DEMO_PDF)

$(CACHE_DIR):
	@mkdir -p $(CACHE_DIR)

$(DEMO_PDF): $(DEMO_SRC) | clean-cache $(CACHE_DIR)
	@cd $(dir $(DEMO_SRC)) && $(COMPILE_TEX) $(notdir $(DEMO_SRC))
	@cp $(CACHE_DIR)/$(notdir $(DEMO_PDF)) $(DEMO_PDF) 

check: create_build_dir
	find . -name *.tex -exec chktex {} \; | tee "$(CACHE_DIR)/lint.out"

clean:
	rm -rf $(BUILD_DIR)
