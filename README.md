# Tracy Debugger Toolbar for Opencart 2.x

** Forked version of https://packagist.org/packages/burdapraha/oc_tracy. Reuploaded since the original repository is not available anymore. **

"Tracy: the addictive tool to ease debugging PHP code for cool developers. Friendly design, logging, profiler, advanced features like debugging AJAX calls or CLI support. You will love it."
For more information see official [Tracy repository](https://github.com/nette/tracy)

![Preview of Debugger](./doc/screenshot.png)

![Preview of Exception bluescreen](https://camo.githubusercontent.com/2c37a6b0c27286f4fd010ccc683682ce714aa774/68747470733a2f2f6e657474652e6769746875622e696f2f74726163792f696d616765732f74726163792d657863657074696f6e2e706e67)

## Installation

1. Requiring installed [Vqmod](https://github.com/vqmod/vqmod) because VqMod doesn't support installing via composer itself.
2. `composer require burdapraha/oc_tracy dev-master`
3. Add this code to your composer.json project file:

```
    "scripts": {
        "post-install-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_tracy/vqmod/xml/tracy.xml', 'upload/vqmod/xml/tracy.xml');\""
        ],
        "post-update-cmd": [
            "php -r \"copy('vendor/burdapraha/oc_tracy/vqmod/xml/tracy.xml', 'upload/vqmod/xml/tracy.xml');\""
        ]
    } 
```
    
It will move vqmod xml file to correct folder.

4. add constant `define('DEV', true);` to your config.php, /admin/config.php
5. optionally you can add row to your `.gitignore` file with path to tracy.xml (example: upload/vqmod/xml/tracy.xml)
6. celebrate!
