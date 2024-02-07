This folder contains all files related to documentation using Doxygen+Breathe+Sphinx.

### Instructions on how to create documentation for new/existing code:
- Set the `CREATE_DOC_FLAG` to `"true"` in the CMakeLists.txt line 131 in the main directory (it is set to `"false"` by default).
- Build the code similar to how you would build it to run a simulation.
  ```bash
  cp examples/cantilever_case/cantileverExample.cpp robotDescription.cpp
  mkdir build && cd build
  cmake ..
  make -j4
  ```
- You will see the html files created in build/docs/sphinx directory. Open index.html locally to ensure if all the changes are in place.
- Commit all the changes in the docs directory to the repo, as a pull request (readthedocs will build the website itself to check for any issues) or directly (go to readthedocs and click "Build Version").
- Do not commit the documentation files that get created in the build folder.

### Adding comments to the code for effective documentation:
- The commenting format for documenting code using Doxygen can be found here: [Documenting the code: Special comment blocks](https://www.doxygen.nl/manual/docblocks.html)
- If you are using vscode, you can simply add an extension for doxygen "Doxygen Documentation Generator". Once you install it, now wherever you want to add comments just type `/**` and press the Enter key. It will autogenerate a comment block which you can populate according to your needs.
