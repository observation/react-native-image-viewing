A forked repo of https://github.com/jobtoday/react-native-image-viewing to create a npm package which is used as a dependency for our own react native component library: https://github.com/observation/react-native-components.
The repository is forked to create a slightly changed version to avoid a bug. The resolution of `fsevents` was also changed to be able to build the package for iOS due to https://github.com/nodejs/node-gyp/issues/2296.

# Build
To build the library and apply our patch run:
```
$ yarn
$ git apply patches/react-native-image-viewing+0.2.2.patch
```

If you delete the `dist` folder and build again, you will see a few files are deleted. This is because the author of the original repo forgot to remove this from his dist folder.

# Publish
run `yarn publish`