# AFelps's Nvim configuration

This is a repo to store some neovim configuration files.

## Requirements

There are some requirements for getting the configuration to work:

- install the `vim-plug` plug manager for vim. Details [here](https://github.com/junegunn/vim-plug)
- you should have `node 10+`
- apparently you should have `yarn` aswell
- obviously you should have `neovim`

I think that's about it. This might be updated in the future as more plugins get added

## Installation

To install this simply copy the contents of this repo to your `~/.config/nvim` folder.
Another option is to create a symbolic link with `ln -s`.


### Lombok
   Lombok is pretty useful to get rid of boiler plate code in java development. 
   Along with the `coc-java` plugin it works on neovim with some small configuration tweaks:

   You should download the latest lombok.jar from their [site](https://projectlombok.org/download)

   Place the jar in an appropriate folder for lombok and head to coc-settings.json file:

   ``` json
   {
     "java.jdt.ls.vmargs": "-javaagent:<absolute path to lombok.jar>" 
   }
   ```

   This should get the lombok working fine with coc-java with no unnecessary linting error and so on.

### Considerations
   The plugged folder is not included in this configuration. So you'll have to openup the `init.vim` file and type in `:PlugInstall` to install all the plugins correctly.
   Some might have other dependencies that were not covered here. If so, just follow the instructions.
   You should install the coc plugins using `:CocInstall <coc package>`.
   There are loads of coc packages like coc-java, coc-json, coc-sh, coc-xml, etc.

   By default this configuration will use `gruvbox` as the theme for nvim.

   But that's basically it. Should work wonders now.
