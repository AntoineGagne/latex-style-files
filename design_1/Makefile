BUILD_DIR=build
FILE=design_example
SHELL=/bin/sh

DRAFT_MODE=pdflatex -draftmode -output-directory
COMPILE_TEX=pdflatex -output-directory

.SUFFIXES: .bib .pdf .tex

all: compile_pdf

compile_pdf: create_build_dir
	$(DRAFT_MODE) $(BUILD_DIR) "$(FILE).tex"
	$(COMPILE_TEX) $(BUILD_DIR) "$(FILE).tex"

create_build_dir:
	mkdir -p $(BUILD_DIR)

check: create_build_dir
	find . -name *.tex -exec chktex {} \; | tee "$(BUILD_DIR)/lint.out"

clean:
	rm -rf $(BUILD_DIR)
