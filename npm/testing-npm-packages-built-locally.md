# Use npm link or npm pack when building an NPM package
*https://medium.com/@the1mills/testing-npm-alpha-beta-rc-packages-108b65eb03d2

Create the link in the project that will be the dependency:
```
npm link
```
Note that this will create a global symlink to the project

Link to the dependency in the second project:
```
npm link name/of/package/to/link/to
```
Don't forget to unlink when finished.

package a tarball for the project:
```
npm pack
```

install directly to the built tarball:
```
npm install /absolute/path/to/project/<the-project-version>.tgz
```
