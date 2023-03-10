### Tasks

- Edit `_project.yml`
  - This file specifies the paths to directories to keep raw data in, save all computed outputs to and save items for sharing and archiving.
  - These paths are referred to with the following syntax:
    - `projr_dir_get("<directory_label>)`, e.g. `projr_dir_get("data_raw")` returns `inst/extdata` by default.
  - Such paths may be system-dependent.
    - The first set, under `directories`, specifies the default directories. If you are happy with them, then you don't need to do anything further.
    - However, paths are allowed to system, i.e they may be differ from your computer to another person's, or your local computer to a remote.
      - There are several scenarios in which this is convenient, for example:
        - The code is to be run in an high-performance computinge environment (HPC), which stores large data in a folder outside the user's home directory, e.g. `/scratch/$USER`.
        - The raw data and outputs but not the code are shared amongst members using a mounted virtual drive, e.g. Google Drive or OneDrive, whose path may vary (across operating systems and even within operating systems).
        - Raw data are kept in an external hard drive whose prefix may vary by system.
  - To add your current system as having its own directory structure, run `projr_profile_add()`.
    - This will create the entry `directories-<working_directory>` where `<working_directory>` is the absolute path to the project root directory on your system.
    - Entries for all the directories under `directories` are copied there.
    - You just fill in the blanks.
    - Where you are happy with the default, then just leave that blank and the default will automiatcally be used.
- Edit `README.md`
  - [ ] In line 4, replace all content other than the heading with the purpose of the project, i.e. `The goal of this project is to ...`.
  - The README can and should be added to from here, with information such as how to install it, what datasets are available and where the results report is. But that is project-specific, so we leave it up to you.
- Using your Git GUI of choice:
  - [ ] Create a Git repository here.
  - [ ] Commit all the files except for `DELETE-AFTER-DOING.md`
  - [ ] Create a GitHub repository in the SATVILab GitHub organisation, and push the commit there.
- Start coding and writing! Add new Rmd's to `rmd/` and then list the under `rmd_files` in `_bookdown.yml`.
- When you make changes, save them frequently to Git and push them to GitHub.
- Now you can delete `DELETE-AFTER-DOING.md`.