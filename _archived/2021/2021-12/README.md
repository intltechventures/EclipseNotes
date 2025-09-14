
# Eclipse Release 2021-12 (4.22)


## [4.22 - 2021-12](https://help.eclipse.org/2021-12/index.jsp) - [download](https://www.eclilpse.org/eclipseide/2021-12/)
- [Eclipse 4.22 - New & Noteworthy](https://www.eclipse.org/eclipse/news/4.22/)
- [What's new?](http://help.eclipse.org/2021-12/index.jsp?topic=%2Forg.eclipse.platform.doc.user%2FwhatsNew%2Fplatform_whatsnew.html&cp%3D0_6)
- [Release Notes](https://www.eclipse.org/eclipse/development/readme_eclipse_4.22.php)

- When attempting to upgrade from 2021-09 to 2021-12, you may get this error (on Windows):
  + "An error occurred while uninstalling"
  + "jee-2019-12_eclipse, phase=org.eclipse.equinox.internal.p2.engine.phases.Uninstall,
    operand=[R]org.eclipse.platform.ide.executable.win32.win32.x86_64 4.21.0.I20210906-0500 --> null,
    action=org.eclipse.equinox.internal.p2.touchpoint.natives.actions.CleanupzipAction)."
  + Backup of file XXX\jee-2019-12\eclipse\eclipse.exe failed.
  + Can not remove : XXX\jee-2019-12\eclipse\eclipse.exe

- See: 
  + https://www.eclipse.org/forums/index.php/t/1109650/
  + https://bugs.eclipse.org/bugs/show_bug.cgi?id=577701#c5
    * Note: This was a regression in the previous release that is fixed in the current release:
  + https://bugs.eclipse.org/bugs/show_bug.cgi?id=577762
    * "Bug 577762 - Updating platform feature should properly handle locked windows (executable) files"
    * "-Djava.io.tmpdir=<eclipse install drive>:\<a-temp-folder>"



## Eclipse Marketplace Plugins



