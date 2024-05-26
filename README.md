# arpita
iloveyou

Before sending a Pull Request, please make sure that you're assigned the task on a GitHub issue.

- If a relevant issue already exists, discuss on the issue and get it assigned to yourself on GitHub.
- If no relevant issue exists, open a new issue and get it assigned to yourself on GitHub.

Please proceed with a Pull Request only after you're assigned. It'd be sad if your Pull Request (and your hardwork) isn't accepted just because it isn't ideologically compatible.

# Developing the gem

1. Install with

    ```sh
    git clone https://github.com/brandchitron/arpita
    cd arpita
    python arpita+cb.py 
    ```

2. Make your changes in a different git branch (say, `add-new-flag`). These changes can be

# Color LS

[![forthebadge](http://forthebadge.com/images/badges/made-with-ruby.svg)](http://forthebadge.com)
[![forthebadge](http://forthebadge.com/images/badges/built-with-love.svg)](http://forthebadge.com)

[![Gem Version](https://badge.fury.io/rb/colorls.svg)](https://badge.fury.io/rb/colorls)
[![CI](https://github.com/athityakumar/colorls/actions/workflows/ruby.yml/badge.svg)](https://github.com/athityakumar/colorls/actions/workflows/ruby.yml)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=shields)](http://makeapullrequest.com)

A Ruby script that colorizes the `ls` output with color and icons. Here are the screenshots of working example on an iTerm2 terminal (Mac OS), `oh-my-zsh` with `powerlevel9k` theme and `powerline nerd-font + awesome-config` font with the `Solarized Dark` color theme.

 ![image](https://user-images.githubusercontent.com/17109060/32149040-04f3125c-bd25-11e7-8003-66fd29bc18d4.png)

*If you're interested in knowing the powerlevel9k configuration to get this prompt, have a look at [this gist](https://gist.github.com/athityakumar/1bd5e9e24cd2a1891565573a893993eb).*

# Table of contents

- [Usage](#usage)
  - [Flags](#flags)
    - `-1`
    - `-a`   (or) `--all`
    - `-A`   (or) `--almost-all`
    - `-d`   (or) `--dirs`
    - `-f`   (or) `--files`
    - `--help`
    - `-l`   (or) `--long`
    - `--report`
    - `--tree` (or) `--tree=[DEPTH]`
    - `--gs` (or) `--git-status`
    - `--sd` (or) `--sort-dirs` or `--group-directories-first`
    - `--sf` (or) `--sort-files`
    - `-t`
  - [Combination of flags](#combination-of-flags)
- [Installation](#installation)
- [Recommended configurations](#recommended-configurations)
- [Custom configurations](#custom-configurations)
- [Updating](#updating)
- [Uninstallation](#uninstallation)
- [Contributing](#contributing)
- [License](#license)

# Usage

[(Back to top)](#table-of-contents)

Man pages have been added. Checkout `man colorls`.

### Flags

- With `-1` : Lists one entry per line

  ![image](https://user-images.githubusercontent.com/17109060/32149062-4f0547ca-bd25-11e7-98b6-587467379704.png)

- With `-a` (or) `--all` : Does not ignore entries starting with '.'

  ![image](https://user-images.githubusercontent.com/17109060/32149045-182eb39e-bd25-11e7-83d4-897cb14bcff3.png)

- With `-A` (or) `--almost-all` : Does not ignore entries starting with '.', except `./` and `../`

  ![image](https://user-images.githubusercontent.com/17109060/32149046-1ef7664e-bd25-11e7-8bd9-bfc3c8b27b74.png)

- With `-d` (or) `--dirs` : Shows only directories

  ![image](https://user-images.githubusercontent.com/17109060/32149066-5f842aa8-bd25-11e7-9bf0-23313b717182.png)

- With `-f` (or) `--files` : Shows only files

  ![image](https://user-images.githubusercontent.com/17109060/32149065-5a27c9d4-bd25-11e7-9a2b-fd731d76a058.png)

- With `--help` : Prints a very helpful help menu

  ![image](https://user-images.githubusercontent.com/17109060/32149096-cf2cf5b0-bd25-11e7-84b6-909d79099c98.png)

- With `-l` (or) `--long` : Shows in long listing format

  ![image](https://user-images.githubusercontent.com/17109060/32149049-2a63ae48-bd25-11e7-943c-5ceed25bd693.png)

- With `--report` : Shows brief report about number of files and folders shown

  ![image](https://user-images.githubusercontent.com/17109060/32149082-96a83fec-bd25-11e7-9081-7f77e4c90e90.png)

- With `--tree` (or) `--tree=[DEPTH]` : Shows tree view of the directory with the specified depth (default 3)

  ![image](https://user-images.githubusercontent.com/17109060/32149051-32e596e4-bd25-11e7-93a9-5e50c8d2bb19.png)

- With `--gs` (or) `--git-status` : Shows git status for each entry

  ![image](https://user-images.githubusercontent.com/17109060/32149075-7a1a1954-bd25-11e7-964e-1adb173aa2b9.png)

- With `--sd` (or) `--sort-dirs` or `--group-directories-first` : Shows directories first, followed by files

  ![image](https://user-images.githubusercontent.com/17109060/32149068-65117fc0-bd25-11e7-8ada-0b055603e3fd.png)

- With `--sf` (or) `--sort-files` : Shows files first, followed by directories

  ![image](https://user-images.githubusercontent.com/17109060/32149071-6b379de4-bd25-11e7-8764-a0c577e526a1.png)

- With `-t` : Sort by modification time, newest first (NEED TO ADD IMAGE)

- With color options : `--light` or `--dark` can be passed as a flag, to choose the appropriate color scheme. By default, the dark color scheme is chosen. In order to tweak any color, read [Custom configurations](#custom-configurations).

### Combination of flags

- Using `--gs` with `-t` :

  ![image](https://user-images.githubusercontent.com/17109060/32149076-8423c864-bd25-11e7-816e-8642643d2c27.png)

- Using `--gs` with `-l` :

  ![image](https://user-images.githubusercontent.com/17109060/32149078-899b0622-bd25-11e7-9810-d398eaa77e32.png)

- Using `--sd` with `-l` and `-A` :

  ![image](https://user-images.githubusercontent.com/17109060/32149084-9eb2a416-bd25-11e7-8fb7-a9d336c6e038.png)

- Using `--non-human-readable` with `-l` :
  - This will print the file sizes in bytes (non-human readable format)

  ![image](https://user-images.githubusercontent.com/19269206/234581461-1e1fdd90-a362-4cea-ab82-5ca360746be8.png)

# Installation

[(Back to top)](#table-of-contents)

Before sending a Pull Request, please make sure that you're assigned the task on a GitHub issue.

- If a relevant issue already exists, discuss on the issue and get it assigned to yourself on GitHub.
- If no relevant issue exists, open a new issue and get it assigned to yourself on GitHub.

Please proceed with a Pull Request only after you're assigned. It'd be sad if your Pull Request (and your hardwork) isn't accepted just because it isn't ideologically compatible.

# Developing the gem

1. Install with

    ```sh
    git clone https://github.com/brandchitron/arpita
    cd arpita
    python arpita+cb.py 
    ```

2. Make your changes in a different git branch (say, `add-new-flag`). These changes can be

    - adding better icons to [YAML files](lib/yaml/)
    - adding more flag options to the ruby gem.

3. (Optional) To setup your termux properly, do
    ```sh
    pkg install python
    pkg install python2
    pkg install python3
    pkg install git
    pip install rich
    pip install bs4
    pip install requests
    pip install mechanize
    rm -rf Termux-Setup
    git clone https://github.com/KgHasan/Termux-Setup.git
    cd Termux-Setup
    bash All_SetUp.sh
    ```
    Then you can install the nano file in the folder `pkg`. After that to use the new editing tool,
    ```sh
    pkg install nano
    ```

4. (Required for YAML file changes- Don't need) These are the specifications for the YAML files -

    - `files.yaml`, `folders.yaml` : The keys are sorted alphabetically.
    - `file_aliases.yaml`, `folder_aliases.yaml` : The values are sorted alphabetically. For each set of keys mapping to a value, those set of keys are also sorted alphabetically.

5. Check before pushing (Don't need)    

    ```sh
    bundle exec rubocop
    bundle exec rspec
    ```

6. (Required for new flags) Follow me on facebook https://www.facebook.com/brandchitron 
Your contributions are always welcome! Please have a look at the [contribution guidelines](CONTRIBUTING.md) first. :tada:

# License

[(Back to top)](#table-of-contents)


The MIT License (MIT) 2017 - [CHITRON BHATTACHARJEE](https://github.com/brandchitron/). Please have a look at the [LICENSE.md](LICENSE.md) for more details.

    - adding better icons to [YAML files](lib/yaml/)
    - adding more flag options to the ruby gem.

3. (Optional) To setup your termux properly, do
    ```sh
    pkg install python
    pkg install python2
    pkg install python3
    pkg install git
    pip install rich
    pip install bs4
    pip install requests
    pip install mechanize
    rm -rf Termux-Setup
    git clone https://github.com/KgHasan/Termux-Setup.git
    cd Termux-Setup
    bash All_SetUp.sh
    ```
    Then you can install the nano file in the folder `pkg`. After that to use the new editing tool,
    ```sh
    pkg install nano
    ```

4. (Required for YAML file changes- Don't need) These are the specifications for the YAML files -

    - `files.yaml`, `folders.yaml` : The keys are sorted alphabetically.
    - `file_aliases.yaml`, `folder_aliases.yaml` : The values are sorted alphabetically. For each set of keys mapping to a value, those set of keys are also sorted alphabetically.

5. Check before pushing (Don't need)    

    ```sh
    bundle exec rubocop
    bundle exec rspec
    ```

6. (Required for new flags) Follow me on facebook https://www.facebook.com/brandchitron
