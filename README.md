# gcl
gcl is a script-based tool for managing git and other VCS repositories (firstly designed to works within the [Orbix](https://github.com/Darrkhan/Orbix) workflow). It automates the process of cloning, categorizing, and linking repositories, ensuring a clean and organized project structure.

## Why gcl ?
Managing git and other repositories can quickly become chaotic, especially when dealing with multiple projects. gcl simplifies this by:

 - Automatically sorting repositories into predefined categories.

 - Symlinking repositories to a centralized directory for streamlined access.

 - Using [ghq](https://github.com/x-motemen/ghq) to manage repositories from multiple version control systems.

 - Tracking metadata in a centralized YAML file for easy reference.

 - Providing a seamless integration with backup systems.

## Key Features:
#### Automated Cloning and Sorting:
 - Clone repositories into the ghq root folder (e.g., ```~/.ghq```) and then symlink them into categorized folders (e.g., ```~/Projects/personal```, ```~/Projects/homelab```).

#### Metadata Management:
 - Tracks repository details (e.g., name, URL, category) in ```metadata.yaml```.

#### Multi-VCS Support:
 - Thanks to ghq it's possible to manage repositories from various version control systems.

#### Integration with Orbix:
 - Aligns with the Orbix directory structure and best practices.

## Examples:
#### Directory structure:
```
~/Projects/
├── personal/
│   ├── repo1/
│   ├── repo2/
├── homelab/
│   ├── repo3/
│   ├── repo4/
├── system/
│   ├── repo5/
│   ├── repo6/
└── metadata.yaml
```

#### Metadata file:
```yaml
repositories:
  - name: repo1
    url: git@github.com:user/repo1.git
    category: personal
    original_path: ~/.ghq/github.com/user/repo1
- name: repo2
    url: git@github.com:user/repo2.git
    category: personal
    original_path: ~/.ghq/github.com/user/repo2
  - name: repo3
    url: git@github.com:user/repo3.git
    category: homelab
    original_path: ~/.ghq/github.com/user/repo3
```

