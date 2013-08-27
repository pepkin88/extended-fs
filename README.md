# extended-fs
===========

## Usage ([node](http://nodejs.org))

    npm install extended-fs

Extended functionality of fs with additional q-dependent promises adaptation of fs functions.

Utilizes the [`q`](https://npmjs.org/package/q) and [`graceful-fs`](https://npmjs.org/package/graceful-fs) to implement missing features and augment existing functions.

Acts as a replacement fs for the existing fs, as it copies over existing functionality from fs. In addition to the standard functions available on [node's package `fs`](http://nodejs.org/api/fs.html), this includes functions to support copying and removing directories recursively. Leverages the [`q`](https://npmjs.org/package/q) package to introduce promise driven `fs` methods.

# API

## `extended-fs.rmDir(dir, callback)`

Asynchronous recursive directory removal. No arguments other than a possible error are given to the callback.

## `extended-fs.rmDirSync(dir)`

Synchronous recursive directory removal.

## `extended-fs.copyFile(src, dest, callback)`

Asynchronous file copy. Copies the file found at `src` over to the `dest` path, overwriting `dest`. No arguments other than a possible error are given to the callback.

## `extended-fs.copyFileSync(src, dest)`

Synchronous file copy.

## `extended-fs.copyDir(src, dest, callback)`

Asynchronous recursive directory copy. Copies all files found at the `src` directory, removing `dest` before writing. No arguments other than a possible error are given to the callback.

## `extended-fs.copyDirSync(src, dest, callback)`

Synchronous recursive directory copy.