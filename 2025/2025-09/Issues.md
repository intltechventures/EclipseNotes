
# Issues

## CDT GDB invocation

- Failed to execute MI command: -exec-run
  + https://www.eclipse.org/forums/index.php/t/1102781/


- My setup notes:
  + I'm runing ```GNU gdb (GDB) (Cygwin 15.2-1) 15.2```


- C/C++ Development User Guide > Before you begin
  + https://help.eclipse.org/latest/index.jsp?topic=%2Forg.eclipse.cdt.doc.user%2Fconcepts%2Fcdt_c_before_you_begin.htm
    * "Note that there is a known issue with running recent versions of Cygwin gdb under the CDT."

      * Debugging failed on Windows when using MSYS2 or Cygwin #228
        * https://github.com/eclipse-cdt/cdt/issues/228
          * "Cygwin GDB 11.2-1 fails, Cygwin GDB 9.2-1 works."
          * "All indications in this log is that the bug is on GDB side not CDT. Not even sure how we could workaround it in CDT."

      * Bug 30017 - Cygwin gdb fails when given a windows absolute path
        * https://sourceware.org/bugzilla/show_bug.cgi?id=30017    
          * Assignee: "Not yet assigned to anyone" (as of 2025-09-26 Friday)
        * https://sourceware.org/bugzilla/show_bug.cgi?id=30017#c2
          > Using a Windows Eclipse and Winows Java with Cygwin executables is bound to encounter problems like this, which cannot be generically solved in Cygwin.
          > Passing Windows-style paths to POSIX API functions which take a pathname generally works.
          > But if an executable (in this case, gdb) does some internal manipulation on the pathname, assuming it's in POSIX-style, you get problems.
          > The simple solution is to write a wrapper around gdb, which takes a Windows-style path, and converts it using cygpath to POSIX-style before passing it to gdb.
          > The complex solution is to modfiy gdb so it identifies the style of path before manipulating it appropriately, but some one who cares about this edge-case will have to write it.
        * https://sourceware.org/bugzilla/show_bug.cgi?id=30017#c3
          > For the last ~20 years it turns out that CDT was relying on undefined behaviour in Cygwin/GDB that changed in GDB 10.
          * GDB commit: [727b7b1864973c2645a554727afd0eaf1303673a](https://sourceware.org/git/?p=binutils-gdb.git;a=commitdiff;h=727b7b1864973c2645a554727afd0eaf1303673a)
        * ___One suggestion mentioned: Switch from Cygwin to MSYS2___
          * https://www.msys2.org/

    * "The Windows SDK provides the Visual C++ compiler and header files and libraries required to create Windows applications. The CDT Visual C++ build integration will find these files based on where you installed the SDK. No other setup is required."
      * "Note: For this release, the integration should be considered beta quality. It is not recommended for production use."


- Also see:
  + https://stackoverflow.com/questions/76944069/how-can-i-fix-the-eclipse-error-unable-to-execute-mi-command-exec-run-path
  + https://stackoverflow.com/questions/13678923/eclipse-failed-to-execute-mi-command-target-select-remote

 
