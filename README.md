# About

[under construction]

# How to use

[under construction]  
*((write something about stages also))*  
*((add examples somewhere below (but try to avoid their downloading)))* 

# Rules
  
### Formatting
 
- The very first line of the rules file should contain either "plugin" or "theme" string.
- At least one tab between items. You can add additional tabs and spaces to give it beautiful formatting.
- You can use comments in any desired format — only the lines that contain one of the rules will be interpreted.

 
### The list of available rules
 
    substitute
        dev_mode_text  prod_mode_text  file
 
    copy
        from  to
 
    uglifyjs
        from  to  [common_directory]
 
    webpack
        from  to  [common_directory]
        
    install
        npm_module_name
 
### What does `webpack` rule do?
 

    JS:  babel (with minification)
    CSS: autoprefixer -> cssnano


### Expansions

* `[m]` – dev/wp-prod/wp-prod/webpack/node_modules

### Notes
 
  - Rules are updated only on the prod stage (`to_prod.sh`), so `to_dev.sh` always works
   with the rules generated by `to_prod.sh`.

  - for `uglifyjs` and `webpack` rules:   
  
    `from` files are created automatically on the prod stage, by renaming the `to` option file if none of them has `dev/` in the beginning. 

#

Version: 1.8.0

License: [MIT](https://github.com/vladlu/wp-prod/blob/master/LICENSE)
