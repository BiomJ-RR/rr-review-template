---
title: RR-Review #<number> of <code>
author: Biometrical Journal reproducibility team 
date: today
output: 
    pdf_document:
        template: ./eisvogel.latex
geometry: margin=2cm
toccolor: Blue
disable-header-and-footer: True
footnotes-pretty: True
---

Congratulations on your successful submission to the Biometrical Journal. At this point, we would like to ask you to carefully read through our [*Reproducible Research (RR) checklist*](https://github.com/BiomJ-RR/rr-checklist/releases/download/1.0/checklist_for_authors.pdf) to make sure that your submission follows best practices for reproducible scientific computing.

Specific requests for improving your data or code supplement:

- [ ] Please **include a README file**,  either `README.txt`, `README.md` or `README.pdf`, that follows the specifications in the *RR guideline* linked above. Please do not forget to add version information by, e.g., copy-pasting the output of R's `sessionInfo()` AFTER loading all necessary packages.

- [ ] Please **include all the code and data** that is necessary to reproduce all figures, tables and results in your paper. If data are not allowed to be made public, pseudo data that are comparable to the original data in size and structure should be used. If at all possible, the original data should be made available to RR editors strictly for the purpose of the audit, at least.  
  - [ ] Specifically, code is missing for Figure XXX, Table XXX, results in Section XXX.
  - [ ] Specifically, data sets `XXX` are missing.

- [ ] Please **organize your code** files well:  
  - [ ] Use a sensible folder structure that makes it easy to navigate your code. Especially, separate your code from your input and output data using sub folders (**!**), such as, e.g. `data/` an `results/`.
  - [ ] Create ONE (**!**) master file (e.g., `master.R` or `main.py`) that proceeds through your study and recreates all results, i.e., tables and figures of the article by executing one single command.
  - [ ] All code in the supplement should be executable without alterations (**!**) by users (beyond setting a working directory, etc.). If alterations are required these should be pointed out in comments in the scripts themselves and in the README file.
  - [ ] Every resulting table should be stored in the `results/` folder and displayed in a human-readable format (**!**), such as, for instance, `pandas.DataFrame` for Python, `data.frames` in R or `cell arrays` in MATLAB. Do not refer to the console output.
  - [ ] Every resulting figure should be saved as a separate file (such as, e.g., `figure1.pdf` or `figure2.png`) in a `results/` folder.
  - [ ] Create as few code files as possible but separate files where useful and sensible.
  - [ ] Read other files, such as the function definitions, into the main file performing the analysis, instead of mixing code that performs the analysis with code that defines the functions used in the analysis.
  - [ ] Avoid absolute paths (e.g., `C:\Projects\My Code\data\`) whenever possible. Use paths relative to the current file or working directory, if the latter is specified in the README and script file, instead (e.g., `./script.R`, `data/`, `../config/params.txt`). Only if this is impossible state in your README how to change the paths.
  - [ ] Use descriptive file names and avoid spaces in file names. Use underscores (`_`) or hyphens (`-`) instead (e.g., `read_dataset.R` instead of `x001 NEW.R`).
  - [ ] R script files must have file endings `.r` or `.R` (pick one)

- [ ] Please use a **consistent style** throughout your code:  
  - [ ] Adopt proper spacing (spaces after commas and around operators etc.).
  - [ ] Comply with a consistent, human-readable line length (max. 120 characters per line).
  - [ ] The code should have a semantically correct and consistent indentation.
  - [ ] The code should not contain (a lot of) commented out code lines.
  - [ ] Please clean up the scripts to only contain relevant and executable lines (comments that explain the code's function are very welcome, of course.).

- [ ] Please **add helpful comments** to your code:  
  - [ ] Make use of sensible comments that help you and others to understand your code.
  - [ ] Each user-defined function must be documented including all function arguments and returned objects.
  - [ ] Add comments that state what figure or table in the manuscript the code produces and make it as easy as possible to associate the outputs of your code with the results in the manuscript: For example, create data frames with the same structure as the tables in your manuscript and save all figure output with descriptive filenames or filenames that correspond to the numbering of the figures in the manuscript (see remarks for code organization above).

- [ ] Please **check your code and language** for mistakes:  
  - [ ] Avoid rounding mistakes, such as, e.g.: <rounding_mistakes>
  - [ ] Correct spelling and grammar. For instance:
    - [ ]  <language_mistakes>

- [ ] Please make your **simulations reproducible**:  
  - [ ] All the code that relies on results of a random number generator (RNG) should be initiated by setting the seed for the RNG so that results are reproducible.
  - [ ] BiomJ's resources for reproducing simulation studies and analyses are finite. If the computations run for more than a couple of days on a standard desktop PC, please provide intermediate results, as well as the scripts used to produce the figures or tables from them and information which parameters to change in order to reduce the run time, where applicable.  
  This will enable us to perform spot checks of reproducibility for specific settings and replications without having to re-run your entire simulation study. If files containing intermediate results are too large to share via e-mail, please upload them to a data repository such as, e.g., [*zenodo*](https://about.zenodo.org/), [*figshare*](https://figshare.com/) or [*osf.io*](https://osf.io/) or share them via a file hosting service (please use one that does not require creating an account for downloading files -- e.g. Dropbox, Google Drive or WeTransfer). If the results files are confidential, we can set up a secure file sharing link as well, please contact your RR editor.
  - [ ] Code should be as platform independent as possible. In R, for instance, avoid OS-specific commands such as `windows()` or `windowsFonts()` and use `file.path()` to make folder separators platform-independent.  
  If the code supplement contains R packages, they should not be submitted as binary ZIP files but as package bundles (`.tar.gz`).  
  If the supplement contains code in compiled languages (C, C++, FORTRAN, etc.), include the source code and suitable makefiles or compilation instructions along with the compiled executables.

- [ ] All code files, data and the `README` should be contained in a **single ZIP container** (for instance, `Code_and_Data.zip`), possibly with subfolders in the container for different purposes. See attached guidelines for details. (Obviously, we make exceptions for very large intermediate result files which can be provided separately and will not be included in the published supplement due to capacity limits on our publisher's side.)

---

Please be aware that your next submission will be the last round of this RR audit. If your resubmitted supplement does not comply with our guidelines or fails the RR audit, its conditional acceptance may be withdrawn and your paper may have to go back to reviewers at the editors' discretion or be published accompanied by a corresponding advisory about its (lack of) reproducibility.


