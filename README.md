# Some useful notes

## I. Repos
### Image crawler
https://github.com/YoongiKim/AutoCrawler \
https://github.com/Joeclinton1/google-images-download 

### Show progress bar
https://github.com/alphatwirl/atpbar \
https://github.com/tqdm/tqdm 

### Search Database
https://github.com/facebookresearch/faiss 

### Demo ML models
https://github.com/gradio-app/gradio

### HTTP benchmark tool
https://github.com/locustio/locust \
https://github.com/wg/wrk \
https://github.com/giltene/wrk2

### Big companies apply ML
https://github.com/eugeneyan/applied-ml

### Feature importance (AI explainability) 
https://github.com/slundberg/shap
https://github.com/jacobgil/pytorch-grad-cam

### Grid search parameters
https://github.com/optuna/optuna

### Image similarity
https://github.com/microsoft/computervision-recipes/blob/1bb489af757fde7c773e16fab87b24305cff4457/scenarios/similarity/01_training_and_evaluation_introduction.ipynb

### Latex
https://en.wikibooks.org/wiki/LaTeX/Tables#The_tabularx_package \
https://tex.stackexchange.com/questions/2441/how-to-add-a-forced-line-break-inside-a-table-cell

### Conventional commits: 
* Original link: https://www.conventionalcommits.org/en/v1.0.0/
* Angular original rules: https://github.com/angular/angular/blob/main/CONTRIBUTING.md
* Definition of types: https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13
  
#### Commit Message Header
```
<type>(<scope>): <short summary>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope: animations|bazel|benchpress|common|compiler|compiler-cli|core|
  │                          elements|forms|http|language-service|localize|platform-browser|
  │                          platform-browser-dynamic|platform-server|router|service-worker|
  │                          upgrade|zone.js|packaging|changelog|docs-infra|migrations|
  │                          devtools
  │
  └─⫸ Commit Type: build|ci|docs|feat|fix|perf|refactor|test
```
The `<type>` and `<summary>` fields are mandatory, the `(<scope>)` field is optional.

BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.

##### `Type`

Must be one of the following:

* **build**: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
* **ci**: Changes to our CI configuration files and scripts (examples: CircleCi, SauceLabs)
* **docs**: Documentation only changes
* **feat**: A new feature
* **fix**: A bug fix
* **perf**: A code change that improves performance
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **test**: Adding missing tests or correcting existing tests
* **chore**: Miscellaneous commits e.g. modifying .gitignore

##### `Scope`
Example from Angular:
* The scope should be the name of the npm package affected (as perceived by the person reading the changelog generated from commit messages). 

##### `Summary`

Use the summary field to provide a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end


## II. Courses
https://mlcourse.ai

### Edge Detection | Boundary Detection | SIFT Detector
https://www.youtube.com/watch?v=7AlwDYmjrcs&list=PL2zRqk16wsdqXEMpHrc4Qnb5rA1Cylrhx

## III. Link
- https://www.import.io/post/history-of-deep-learning/?fbclid=IwAR2m3dXA22QSw79rMk1x553lNmVGiIdmTlcQNuziJTbkN2sXR2jQZtn68hk
- Multiple gits: https://medium.com/the-andela-way/a-practical-guide-to-managing-multiple-github-accounts-8e7970c8fd46
- df command: https://quantrimang.com/cong-nghe/lenh-df-trong-linux-kem-vi-du-167650
  - `df -x squashfs` (exclude loop)
  - `df -t ext4` (show only ext4)
  - `df --total` (show total space)
  - `df -T` (show type of filesystem)
  - common use:
    - `df -x squashfs -hT --total`
    - `df -x squashfs -x tmpfs -hT --total`
## IV. Papers
- https://arxiv.org/pdf/1811.04110.pdf
- https://arxiv.org/pdf/2003.13911.pdf
## V. Others
- Install gnome tweak to swap keys in Ubuntu
- Preview file in Ubuntu: `sudo apt-get install gnome-sushi`
- Auto resize sidebar's icons on Ubuntu:
  + `gsettings set org.gnome.shell.extensions.dash-to-dock icon-size-fixed true`
  + https://askubuntu.com/questions/1252142/auto-resize-icons-in-ubuntu-dock
- Add additional hard drive to current PC:
  + https://askubuntu.com/questions/125257/how-do-i-add-an-additional-hard-drive
  + https://askubuntu.com/questions/90339/how-do-i-set-read-write-permissions-my-hard-drives
- Install multiple cuda version:
  + https://wiki.cs.umd.edu/gamma/view/Installing_multiple_versions_of_cuda_in_a_machine
- make CUDA report error in detail:
  + CUDA_LAUNCH_BLOCKING=1 python3 main.py
- Remove nvidia-driver (535 bug):
  + Remove all cuda sources.list in `/etc/apt/sources.list.d/cuda*` https://forums.developer.nvidia.com/t/unmet-dependencies-nvidia-dkms-535-package-conflict-breaks-ubuntu-22-04-install/265788/4?fbclid=IwAR0eDc0bb-WMQw9016yCL1W9E5pWtAAmOVFvCG8lckb124Z9_GGdnAp6gRc ![image](https://github.com/bavo96/note/assets/27908949/5633aaea-bf7a-426c-8048-e14b9409c6a6)
  + `sudo apt --fix-broken install`
  + `sudo dpkg -i --force-overwrite <package>`
  + `sudo apt -f install`
- Location of applications:
  + `/usr/share/applications`
  + `~/.local/share/applications`
- Check all comments on github:
  + Type this into search box: `is:issue commenter:bavo96`
- Open video with special codec:
  + h264: ffmpeg
  + itu.h264: gstreamer1.0-plugins-bad:amd64 <none> 1.16.3-0ubuntu1.1
- Activate F1-F12 on ubuntu:
  + https://www.hashbangcode.com/article/turning-or-fn-mode-ubuntu-linux
  + Temporary: echo 2 | sudo tee /sys/module/hid_apple/parameters/fnmode
  + Permanent: echo options hid_apple fnmode=0 | sudo tee -a /etc/modprobe.d/hid_apple.conf
## VI. Install Ubuntu 24.01
- NVIDIA Driver
- Anaconda
- Rathole
- Docker
- bavovim
- Brave
