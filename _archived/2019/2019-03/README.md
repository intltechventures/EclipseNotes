
# Eclipse Release 2019-03 (4.11)

## [2019-03 (4.11)](https://help.eclipse.org/2019-03/index.jsp) - [download](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2019-03/R/eclipse-inst-win64.exe)

- JSON Schema Validation
  + Bug submitted: [#546541 UnsupportedOperationException: Not a string: {"type":"string","format":"uri-reference"} thrown by JsonValue.java](https://bugs.eclipse.org/bugs/show_bug.cgi?id=546541)
    + It appears that specifying ```draft-07```, ```draft-06```, or ```draft-05``` in the $schema URI - results in an exception being thrown (see my bug submission above)
    + Specifying ```draft-04``` appears to work - and no exception is thrown. I also posted this info to stackoverflow - and created a blog posting to document my findings:
      * https://stackoverflow.com/questions/55719672/ecipse-v4-11-release-2019-03-not-a-string-typestring-formaturi-r
      * https://intltechventures.blogspot.com/2019/04/2019-04-20-saturday-eclipse-ide-v411.html

  + I've confirmed that pointing a JSON Catalog Entry URL to either  ```http://``` or ```file:/C:/``` works as expected.


## Eclipse Marketplace Plugins

- JSON Editor Plugin
  + https://marketplace.eclipse.org/content/json-editor-plugin
  + https://github.com/boothen/Json-Eclipse-Plugin
    * See Youtube demo: https://www.youtube.com/watch?v=vXRwFwk2QE4
  + Plugin Install site:
    * http://boothen.github.io/Json-Eclipse-Plugin/
  + NOTES:
    * Last update on github appears to have been on 2019-03-03 
    * Testing this with Java JDK 12, on a Windows 10 laptop - it appears that JSON Schema Validation __IS NOT WORKING when this plugin is installed___ -  even after registering the file pattern and schema URL via ```Window > Preferences > JSON > JSON Catalog``` 
  + Issue #26 submitted: [Blocks JSON Schema Validation in Eclipse v4.11 (release 2019-03)](https://github.com/boothen/Json-Eclipse-Plugin/issues/26)


- Egit 
  + It appears that this URL is not included in the "Eclipse IDE for JavaScript and Web Developers" package - and I had to add this manually.
  + https://download.eclipse.org/egit/updates-nightly/


