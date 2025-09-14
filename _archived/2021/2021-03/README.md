
# Eclipse Release 2021-03 (4.19)

## [4.19 - 2021-03](https://help.eclipse.org/2021-03/index.jsp) - [download](https://www.eclipse.org/eclipseide/2021-03/)
- [Eclipse 4.19 - New & Noteworthy](https://www.eclipse.org/eclipse/news/4.19/)
- [What's new?](http://help.eclipse.org/2021-03/index.jsp?topic=%2Forg.eclipse.platform.doc.user%2FwhatsNew%2Fplatform_whatsnew.html&cp%3D0_6) 
- [Release Notes](https://www.eclipse.org/eclipse/development/readme_eclipse_4.19.php)
  + "Eclipse must be installed to a clean directory and not installed over top of a previous installation. If you have done this then please re-install to a new directory."


- Issues Encountered:
  + https://www.eclipse.org/forums/index.php/t/86078/
  + https://stackoverflow.com/questions/11768106/clean-out-eclipse-workspace-metadata
    * I think this is the root-cause of a lot of error messages...

  + https://bugs.eclipse.org/bugs/show_bug.cgi?id=571885
    * "java.io.FileNotFoundException: /icons/eview16/error_log.gif"
    * KM: This only shows when opening an previous  workspace

  + https://bugs.eclipse.org/bugs/show_bug.cgi?id=570094
    * "Not properly disposed SWT resource"
    * "Add NonDisposedReporter to default IDE application & enable in SDK product"
    * https://git.eclipse.org/c/platform/eclipse.platform.ui.git/commit/?id=99cbe6f11ddf9fc4edad7b1d03480703992583c5
    * Re: https://bugs.eclipse.org/bugs/show_bug.cgi?id=569752
      * "Detect non disposed OS resources via Object.finalize()"
    * Re: https://github.com/eclipse/eclipse.platform.ui/blob/master/bundles/org.eclipse.ui.ide.application/src/org/eclipse/ui/internal/ide/application/IDEWorkbenchAdvisor.java



## Eclipse Marketplace Plugins

- Java 16 Support for Eclipse 2021-03 (4.19)
  + https://marketplace.eclipse.org/content/java-16-support-eclipse-2021-03-419
	  * The feature can also be installed via the following P2 update site:
	    * https://download.eclipse.org/eclipse/updates/4.19-P-builds
      * NOTE: Once you have installed this update, disable the update site - it appears that it doesn't recognize that
        it is installed - and keeps trying to update.
  + https://wiki.eclipse.org/Java16/Examples


- Eclipse Groovy
  + https://github.com/groovy/groovy-eclipse
    * https://github.com/groovy/groovy-eclipse/wiki
    * https://github.com/groovy/groovy-eclipse/wiki/4.1.0-Release-Notes
      * https://dist.springsource.org/release/GRECLIPSE/4.1.0/e4.19
      * NOTE: This is *NOT COMPATIBLE* with the Java 16 Support, above  

- Rust Corrosion
  + https://download.eclipse.org/corrosion/releases/latest/


- Eclipse StatET (R language)
  + https://projects.eclipse.org/projects/science.statet
    * https://download.eclipse.org/statet/integration/latest/E202103
  + It has been a __painful__ trial-and-error to get this working - this was helpful:
    * https://stackoverflow.com/questions/9502667/statet-in-eclipse-and-r/9503022
    * https://gitlab.com/walware/de.walware.rj-server.gr/-/wikis/Installation
      * "The package only works in the R Console (RJ) in the StatET IDE or other applications using StatET RJ."      
      * "It is important to pick the RJ package version/repository compatible to the used StatET version."
      * ```install.packages(c("rj", "rj.gd"), repos="https://download.walware.de/rj-4.0")```


- Kotlin
  + https://marketplace.eclipse.org/content/kotlin-plugin-eclipse
    * https://dl.bintray.com/jetbrains/kotlin/eclipse-plugin/last/

- PyDev
  + https://marketplace.eclipse.org/content/pydev-python-ide-eclipse
    * http://www.pydev.org/updates/

- PHP Development Tools (PDT)
  + https://www.eclipse.org/pdt/
  + https://wiki.eclipse.org/PDT
  + https://github.com/eclipse/pdt
  + https://download.eclipse.org/tools/pdt/updates/7.2
  + https://download.eclipse.org/tools/pdt/updates/8.0
  + https://download.eclipse.org/tools/pdt/updates/latest/

- Subversive - DO NOT USE, has not been updated to support 2021-03, 4.19
  + https://www.eclipse.org/subversive/documentation/gettingStarted/aboutSubversive/install.php
  * https://www.eclipse.org/subversive/downloads.php

- Subclipse
  + https://marketplace.eclipse.org/content/subclipse
    * https://subclipse.github.io/updates/subclipse/4.3.x/
      * DO NOT USE - URL not found
  + https://github.com/subclipse/subclipse
    * https://subclipse.github.io/updates/
  + Issues:
    * https://stackoverflow.com/questions/1425891/subclipse-complains-path-is-not-a-working-copy-after-moving-workspace

- CDT 
  + https://intltechventures.blogspot.com/2016/03/2016-03-04-friday-gcc-gnu-compiler.html
  + https://www.eclipse.org/cdt/documentation.php
  + https://www.eclipse.org/cdt/downloads.php
    * https://download.eclipse.org/tools/cdt/releases/10.2


- Web Tools 
  + https://projects.eclipse.org/projects/webtools


- Eclipse Wild Web Developer 
  + https://projects.eclipse.org/projects/tools.wildwebdeveloper
  + https://github.com/eclipse/wildwebdeveloper#installation
    * http://download.eclipse.org/wildwebdeveloper/snapshots


- GoClipse 
  + https://marketplace.eclipse.org/content/goclipse
    * https://goclipse.github.io/releases/
    * CONFLICT NOTE: ```Has an conflict with CDT 10.```


- SonarLint
  + https://marketplace.eclipse.org/content/sonarlint
    * Detect Code Quality and Code Security issues on the fly in Eclipse
  + https://www.sonarlint.org/eclipse
  + https://github.com/SonarSource/sonarlint-eclipse
  + https://eclipse-uc.sonarlint.org


- Snyk Security Scanner 
  + https://marketplace.eclipse.org/content/snyk-security-scanner


- JHipster IDE 
  + https://marketplace.eclipse.org/content/jhipster-ide


- Java Mission Control
  + https://marketplace.eclipse.org/content/java-mission-control
  + https://www.oracle.com/java/technologies/jdk-mission-control.html
  + https://download.oracle.com/technology/products/missioncontrol/updatesites/openjdk/8.0.0/ide/
  + JDK Mission Control can be downloaded and installed using the Eclipse Update Site facility. The following URL functions as an update site. Novice users can follow the step-by-step instructions.
    * http://download.oracle.com/technology/products/missioncontrol/updatesites/openjdk/8.0.0/eclipse/



### TO Evaluate - for possible Installation

- https://marketplace.eclipse.org/content/spring-tools-4-aka-spring-tool-suite-4
  + https://spring.io/tools


- https://marketplace.eclipse.org/content/jhipster-ide
  + https://www.jhipster.tech/


- https://marketplace.eclipse.org/content/pmd-eclipse-plugin
  + https://pmd.github.io/


- https://marketplace.eclipse.org/content/checkstyle-plug
  + https://checkstyle.org/eclipse-cs/#!/


- https://marketplace.eclipse.org/content/umlet-uml-tool-fast-uml-diagrams  
  + https://www.umlet.com/umlet_latest/repository/
