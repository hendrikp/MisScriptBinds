# Miscreated C++, Lua Script Bindings

A simple listing of available C++ script binds and their parameters based on the Miscreated 1.11 Update (Exported on 6. June, 2020).
This list has been exported through a simple RegEx search and thus doesn't contain help, return values, or usage samples.
* It was created with the regular expressions you can use yourself on other CryEngine repositories
  * Class, Function name and parameter names, types through: `int.*ScriptBind_(.*\:\:.*)\)` then replace `.*ScriptBind_` with nothing
    * https://github.com/hendrikp/MisScriptBinds/blob/master/Listing_ScriptBind.txt
  * Function name, parameter names and optional paramters through: `SCRIPT_REG.*FUNC` then replace `\\.*` with nothing, `\(.*\)*:` with `:`, `.*\\`, `ScriptBind_`, and `.cpp` with nothing, `:\s*` with `: ` 
    * https://github.com/hendrikp/MisScriptBinds/blob/master/Listing_ScriptReg.txt
  
(Keep in mind some exceptions manually parse parameters thus, dont have a parameter listing. Others are completly obsolete as not used by Miscreated e.g. the whole `AI` section is replaced by the `Kythera` one)

Find information on functionalities added from modding requests here:
* https://docs.google.com/spreadsheets/d/1xDgNs_XqrY1U0swqOLfBuNdW5uXbbjKYg2xTWBFCPGg/edit?ouid=113269844619596256002&usp=sheets_home&ths=true

You find usage samples in the `GameSDK\Scripts` subfolders in the .pak files. Additional information about return values or inner workings of CryEngine based binds can be found here on GitHub by simply searching for `ScriptBind` + `<the function>`.
* Or view another listing created by a modder here: https://gitlab.com/mismodding/miscreatedluadocs/-/tree/master/public
* If you use VSCode with sumneko and emmylua then a base setup for a autocomplete can be found here: https://gitlab.com/mismodding/workspace/-/tree/master/libs
* Further Information for experts you gather by dumping `_G` or specific classes at game runtime in Lua to the console. (Keep in mind your dumper needs a visited markup table to avoid infinite recursions)
  * This way you find information only created internally at runtime or through Lua scripts in the .pak folder

Use or modify as you like.
