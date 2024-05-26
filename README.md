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
