# api documentation for  [fs-extra (v2.1.2)](https://github.com/jprichardson/node-fs-extra)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fs-extra.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fs-extra)
#### fs-extra contains methods that aren't included in the vanilla Node.js fs package. Such as mkdir -p, cp -r, and rm -rf.

[![NPM](https://nodei.co/npm/fs-extra.png?downloads=true)](https://www.npmjs.com/package/fs-extra)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fs-extra/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-fs-extra_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fs-extra/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-fs-extra/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "JP Richardson",
        "email": "jprichardson@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/jprichardson/node-fs-extra/issues"
    },
    "dependencies": {
        "graceful-fs": "^4.1.2",
        "jsonfile": "^2.1.0"
    },
    "description": "fs-extra contains methods that aren't included in the vanilla Node.js fs package. Such as mkdir -p, cp -r, and rm -rf.",
    "devDependencies": {
        "coveralls": "^2.11.2",
        "istanbul": "^0.4.5",
        "klaw": "^1.0.0",
        "klaw-sync": "^1.1.2",
        "minimist": "^1.1.1",
        "mocha": "^3.1.2",
        "proxyquire": "^1.7.10",
        "read-dir-files": "^0.1.1",
        "rimraf": "^2.2.8",
        "secure-random": "^1.1.1",
        "standard": "^8.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "046c70163cef9aad46b0e4a7fa467fb22d71de35",
        "tarball": "https://registry.npmjs.org/fs-extra/-/fs-extra-2.1.2.tgz"
    },
    "gitHead": "84717b8d03f04785124604a119a9a6769f608853",
    "homepage": "https://github.com/jprichardson/node-fs-extra",
    "keywords": [
        "fs",
        "file",
        "file system",
        "copy",
        "directory",
        "extra",
        "mkdirp",
        "mkdir",
        "mkdirs",
        "recursive",
        "json",
        "read",
        "write",
        "extra",
        "delete",
        "remove",
        "touch",
        "create",
        "text",
        "output",
        "move"
    ],
    "license": "MIT",
    "main": "./lib/index",
    "maintainers": [
        {
            "name": "jprichardson",
            "email": "jprichardson@gmail.com"
        },
        {
            "name": "ryanzim",
            "email": "opensrc@ryanzim.com"
        }
    ],
    "name": "fs-extra",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/jprichardson/node-fs-extra.git"
    },
    "scripts": {
        "coverage": "istanbul cover -i 'lib/**' -x '**/__tests__/**' test.js",
        "coveralls": "npm run coverage && coveralls < coverage/lcov.info",
        "lint": "standard",
        "test": "npm run lint && npm run unit",
        "test-find": "find ./lib/**/__tests__ -name *.test.js | xargs mocha",
        "unit": "node test.js"
    },
    "version": "2.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module fs-extra](#apidoc.module.fs-extra)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>FileReadStream (path, options)](#apidoc.element.fs-extra.FileReadStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>FileWriteStream (path, options)](#apidoc.element.fs-extra.FileWriteStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ReadStream (path, options)](#apidoc.element.fs-extra.ReadStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.fs-extra.Stats)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>WriteStream (path, options)](#apidoc.element.fs-extra.WriteStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>_toUnixTimestamp (time)](#apidoc.element.fs-extra._toUnixTimestamp)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>access (path, mode, callback)](#apidoc.element.fs-extra.access)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>accessSync (path, mode)](#apidoc.element.fs-extra.accessSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>appendFile (path, data, options, cb)](#apidoc.element.fs-extra.appendFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>appendFileSync (path, data, options)](#apidoc.element.fs-extra.appendFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>chmod (target, mode, cb)](#apidoc.element.fs-extra.chmod)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>chmodSync (target, mode)](#apidoc.element.fs-extra.chmodSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>chown (target, uid, gid, cb)](#apidoc.element.fs-extra.chown)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>chownSync (target, uid, gid)](#apidoc.element.fs-extra.chownSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>close (fd, cb)](#apidoc.element.fs-extra.close)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>closeSync (fd)](#apidoc.element.fs-extra.closeSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>copy (src, dest, options, callback)](#apidoc.element.fs-extra.copy)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>copySync (src, dest, options)](#apidoc.element.fs-extra.copySync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createFile (file, callback)](#apidoc.element.fs-extra.createFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createFileSync (file)](#apidoc.element.fs-extra.createFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.createLink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.createLinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createReadStream (path, options)](#apidoc.element.fs-extra.createReadStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.createSymlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.createSymlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>createWriteStream (path, options)](#apidoc.element.fs-extra.createWriteStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>emptyDir (dir, callback)](#apidoc.element.fs-extra.emptyDir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>emptyDirSync (dir)](#apidoc.element.fs-extra.emptyDirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>emptydir (dir, callback)](#apidoc.element.fs-extra.emptydir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>emptydirSync (dir)](#apidoc.element.fs-extra.emptydirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureDir (p, opts, callback, made)](#apidoc.element.fs-extra.ensureDir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureDirSync (p, opts, made)](#apidoc.element.fs-extra.ensureDirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureFile (file, callback)](#apidoc.element.fs-extra.ensureFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureFileSync (file)](#apidoc.element.fs-extra.ensureFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensureLink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensureLinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensureSymlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ensureSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensureSymlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>exists (path, callback)](#apidoc.element.fs-extra.exists)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>existsSync (path)](#apidoc.element.fs-extra.existsSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fchmod (target, mode, cb)](#apidoc.element.fs-extra.fchmod)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fchmodSync (target, mode)](#apidoc.element.fs-extra.fchmodSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fchown (target, uid, gid, cb)](#apidoc.element.fs-extra.fchown)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fchownSync (target, uid, gid)](#apidoc.element.fs-extra.fchownSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fdatasync (fd, callback)](#apidoc.element.fs-extra.fdatasync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fdatasyncSync (fd)](#apidoc.element.fs-extra.fdatasyncSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fstat (target, cb)](#apidoc.element.fs-extra.fstat)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fstatSync (target)](#apidoc.element.fs-extra.fstatSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fsync (fd, callback)](#apidoc.element.fs-extra.fsync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>fsyncSync (fd)](#apidoc.element.fs-extra.fsyncSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ftruncate (fd, len, callback)](#apidoc.element.fs-extra.ftruncate)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ftruncateSync (fd, len)](#apidoc.element.fs-extra.ftruncateSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.fs-extra.futimes)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>futimesSync (fd, atime, mtime)](#apidoc.element.fs-extra.futimesSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>gracefulify (fs)](#apidoc.element.fs-extra.gracefulify)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lchmod (path, mode, cb)](#apidoc.element.fs-extra.lchmod)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lchmodSync ()](#apidoc.element.fs-extra.lchmodSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lchown (path, uid, gid, cb)](#apidoc.element.fs-extra.lchown)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lchownSync ()](#apidoc.element.fs-extra.lchownSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>link (existingPath, newPath, callback)](#apidoc.element.fs-extra.link)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>linkSync (existingPath, newPath)](#apidoc.element.fs-extra.linkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lstat (target, cb)](#apidoc.element.fs-extra.lstat)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lstatSync (target)](#apidoc.element.fs-extra.lstatSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lutimes (_a, _b, _c, cb)](#apidoc.element.fs-extra.lutimes)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>lutimesSync ()](#apidoc.element.fs-extra.lutimesSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdir (path, mode, callback)](#apidoc.element.fs-extra.mkdir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirSync (path, mode)](#apidoc.element.fs-extra.mkdirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirp (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirp)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirpSync (p, opts, made)](#apidoc.element.fs-extra.mkdirpSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirs (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirsSync (p, opts, made)](#apidoc.element.fs-extra.mkdirsSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdtemp (prefix, options, callback)](#apidoc.element.fs-extra.mkdtemp)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdtempSync (prefix, options)](#apidoc.element.fs-extra.mkdtempSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>move (source, dest, options, callback)](#apidoc.element.fs-extra.move)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>moveSync (src, dest, options)](#apidoc.element.fs-extra.moveSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>open (path, flags, mode, cb)](#apidoc.element.fs-extra.open)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>openSync (path, flags, mode)](#apidoc.element.fs-extra.openSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputFile (file, data, encoding, callback)](#apidoc.element.fs-extra.outputFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputFileSync (file, data, encoding)](#apidoc.element.fs-extra.outputFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputJSON (file, data, options, callback)](#apidoc.element.fs-extra.outputJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputJSONSync (file, data, options)](#apidoc.element.fs-extra.outputJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputJson (file, data, options, callback)](#apidoc.element.fs-extra.outputJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>outputJsonSync (file, data, options)](#apidoc.element.fs-extra.outputJsonSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>read (fd, buffer, offset, length, position, callback_)](#apidoc.element.fs-extra.read)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readFile (path, options, cb)](#apidoc.element.fs-extra.readFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readFileSync (path, options)](#apidoc.element.fs-extra.readFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readJSON (file, options, callback)](#apidoc.element.fs-extra.readJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readJSONSync (file, options)](#apidoc.element.fs-extra.readJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readJson (file, options, callback)](#apidoc.element.fs-extra.readJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readJsonSync (file, options)](#apidoc.element.fs-extra.readJsonSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readSync (fd, buffer, offset, length, position)](#apidoc.element.fs-extra.readSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readdir (path, options, cb)](#apidoc.element.fs-extra.readdir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readdirSync (path, options)](#apidoc.element.fs-extra.readdirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readlink (path, options, callback)](#apidoc.element.fs-extra.readlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>readlinkSync (path, options)](#apidoc.element.fs-extra.readlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>realpath (p, options, callback)](#apidoc.element.fs-extra.realpath)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>realpathSync (p, options)](#apidoc.element.fs-extra.realpathSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>remove (dir, callback)](#apidoc.element.fs-extra.remove)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>removeSync (dir)](#apidoc.element.fs-extra.removeSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>rename (oldPath, newPath, callback)](#apidoc.element.fs-extra.rename)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>renameSync (oldPath, newPath)](#apidoc.element.fs-extra.renameSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>rmdir (path, callback)](#apidoc.element.fs-extra.rmdir)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>rmdirSync (path)](#apidoc.element.fs-extra.rmdirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>stat (target, cb)](#apidoc.element.fs-extra.stat)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>statSync (target)](#apidoc.element.fs-extra.statSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>symlink (target, path, type_, callback_)](#apidoc.element.fs-extra.symlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>symlinkSync (target, path, type)](#apidoc.element.fs-extra.symlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>truncate (path, len, callback)](#apidoc.element.fs-extra.truncate)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>truncateSync (path, len)](#apidoc.element.fs-extra.truncateSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>unlink (path, callback)](#apidoc.element.fs-extra.unlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>unlinkSync (path)](#apidoc.element.fs-extra.unlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>unwatchFile (filename, listener)](#apidoc.element.fs-extra.unwatchFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>utimes (path, atime, mtime, callback)](#apidoc.element.fs-extra.utimes)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>utimesSync (path, atime, mtime)](#apidoc.element.fs-extra.utimesSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>watch (filename, options, listener)](#apidoc.element.fs-extra.watch)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>watchFile (filename, options, listener)](#apidoc.element.fs-extra.watchFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.fs-extra.write)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeFile (path, data, options, cb)](#apidoc.element.fs-extra.writeFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeFileSync (path, data, options)](#apidoc.element.fs-extra.writeFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeJSON (file, obj, options, callback)](#apidoc.element.fs-extra.writeJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeJSONSync (file, obj, options)](#apidoc.element.fs-extra.writeJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeJson (file, obj, options, callback)](#apidoc.element.fs-extra.writeJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeJsonSync (file, obj, options)](#apidoc.element.fs-extra.writeJsonSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>writeSync (fd, buffer, offset, length, position)](#apidoc.element.fs-extra.writeSync)
1.  number <span class="apidocSignatureSpan">fs-extra.</span>F_OK
1.  number <span class="apidocSignatureSpan">fs-extra.</span>R_OK
1.  number <span class="apidocSignatureSpan">fs-extra.</span>W_OK
1.  number <span class="apidocSignatureSpan">fs-extra.</span>X_OK
1.  number <span class="apidocSignatureSpan">fs-extra.</span>spaces
1.  object <span class="apidocSignatureSpan">fs-extra.</span>ReadStream.prototype
1.  object <span class="apidocSignatureSpan">fs-extra.</span>Stats.prototype
1.  object <span class="apidocSignatureSpan">fs-extra.</span>WriteStream.prototype
1.  object <span class="apidocSignatureSpan">fs-extra.</span>constants
1.  object <span class="apidocSignatureSpan">fs-extra.</span>copy_sync
1.  object <span class="apidocSignatureSpan">fs-extra.</span>empty
1.  object <span class="apidocSignatureSpan">fs-extra.</span>ensure
1.  object <span class="apidocSignatureSpan">fs-extra.</span>json
1.  object <span class="apidocSignatureSpan">fs-extra.</span>jsonfile
1.  object <span class="apidocSignatureSpan">fs-extra.</span>move_sync
1.  object <span class="apidocSignatureSpan">fs-extra.</span>output

#### [module fs-extra.ReadStream](#apidoc.module.fs-extra.ReadStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>ReadStream (path, options)](#apidoc.element.fs-extra.ReadStream.ReadStream)

#### [module fs-extra.ReadStream.prototype](#apidoc.module.fs-extra.ReadStream.prototype)
1.  [function <span class="apidocSignatureSpan">fs-extra.ReadStream.prototype.</span>open ()](#apidoc.element.fs-extra.ReadStream.prototype.open)

#### [module fs-extra.Stats](#apidoc.module.fs-extra.Stats)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.fs-extra.Stats.Stats)

#### [module fs-extra.Stats.prototype](#apidoc.module.fs-extra.Stats.prototype)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>_checkModeProperty (property)](#apidoc.element.fs-extra.Stats.prototype._checkModeProperty)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isBlockDevice ()](#apidoc.element.fs-extra.Stats.prototype.isBlockDevice)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isCharacterDevice ()](#apidoc.element.fs-extra.Stats.prototype.isCharacterDevice)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isDirectory ()](#apidoc.element.fs-extra.Stats.prototype.isDirectory)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isFIFO ()](#apidoc.element.fs-extra.Stats.prototype.isFIFO)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isFile ()](#apidoc.element.fs-extra.Stats.prototype.isFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isSocket ()](#apidoc.element.fs-extra.Stats.prototype.isSocket)
1.  [function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isSymbolicLink ()](#apidoc.element.fs-extra.Stats.prototype.isSymbolicLink)

#### [module fs-extra.WriteStream](#apidoc.module.fs-extra.WriteStream)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>WriteStream (path, options)](#apidoc.element.fs-extra.WriteStream.WriteStream)

#### [module fs-extra.WriteStream.prototype](#apidoc.module.fs-extra.WriteStream.prototype)
1.  [function <span class="apidocSignatureSpan">fs-extra.WriteStream.prototype.</span>open ()](#apidoc.element.fs-extra.WriteStream.prototype.open)

#### [module fs-extra.copy](#apidoc.module.fs-extra.copy)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>copy (src, dest, options, callback)](#apidoc.element.fs-extra.copy.copy)

#### [module fs-extra.copy_sync](#apidoc.module.fs-extra.copy_sync)
1.  [function <span class="apidocSignatureSpan">fs-extra.copy_sync.</span>copySync (src, dest, options)](#apidoc.element.fs-extra.copy_sync.copySync)

#### [module fs-extra.empty](#apidoc.module.fs-extra.empty)
1.  [function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptyDir (dir, callback)](#apidoc.element.fs-extra.empty.emptyDir)
1.  [function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptyDirSync (dir)](#apidoc.element.fs-extra.empty.emptyDirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptydir (dir, callback)](#apidoc.element.fs-extra.empty.emptydir)
1.  [function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptydirSync (dir)](#apidoc.element.fs-extra.empty.emptydirSync)

#### [module fs-extra.ensure](#apidoc.module.fs-extra.ensure)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createFile (file, callback)](#apidoc.element.fs-extra.ensure.createFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createFileSync (file)](#apidoc.element.fs-extra.ensure.createFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.createLink)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.createLinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.createSymlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.createSymlinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureFile (file, callback)](#apidoc.element.fs-extra.ensure.ensureFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureFileSync (file)](#apidoc.element.fs-extra.ensure.ensureFileSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.ensureLink)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.ensureLinkSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.ensureSymlink)
1.  [function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.ensureSymlinkSync)

#### [module fs-extra.json](#apidoc.module.fs-extra.json)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJSON (file, data, options, callback)](#apidoc.element.fs-extra.json.outputJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJSONSync (file, data, options)](#apidoc.element.fs-extra.json.outputJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJson (file, data, options, callback)](#apidoc.element.fs-extra.json.outputJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJsonSync (file, data, options)](#apidoc.element.fs-extra.json.outputJsonSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>readJSON (file, options, callback)](#apidoc.element.fs-extra.json.readJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>readJSONSync (file, options)](#apidoc.element.fs-extra.json.readJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>readJson (file, options, callback)](#apidoc.element.fs-extra.json.readJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>readJsonSync (file, options)](#apidoc.element.fs-extra.json.readJsonSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJSON (file, obj, options, callback)](#apidoc.element.fs-extra.json.writeJSON)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJSONSync (file, obj, options)](#apidoc.element.fs-extra.json.writeJSONSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJson (file, obj, options, callback)](#apidoc.element.fs-extra.json.writeJson)
1.  [function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJsonSync (file, obj, options)](#apidoc.element.fs-extra.json.writeJsonSync)
1.  number <span class="apidocSignatureSpan">fs-extra.json.</span>spaces

#### [module fs-extra.mkdirs](#apidoc.module.fs-extra.mkdirs)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>mkdirs (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.mkdirs)
1.  [function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>ensureDir (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.ensureDir)
1.  [function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>ensureDirSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.ensureDirSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirp (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.mkdirp)
1.  [function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirpSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.mkdirpSync)
1.  [function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirsSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.mkdirsSync)

#### [module fs-extra.move](#apidoc.module.fs-extra.move)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>move (source, dest, options, callback)](#apidoc.element.fs-extra.move.move)

#### [module fs-extra.move_sync](#apidoc.module.fs-extra.move_sync)
1.  [function <span class="apidocSignatureSpan">fs-extra.move_sync.</span>moveSync (src, dest, options)](#apidoc.element.fs-extra.move_sync.moveSync)

#### [module fs-extra.output](#apidoc.module.fs-extra.output)
1.  [function <span class="apidocSignatureSpan">fs-extra.output.</span>outputFile (file, data, encoding, callback)](#apidoc.element.fs-extra.output.outputFile)
1.  [function <span class="apidocSignatureSpan">fs-extra.output.</span>outputFileSync (file, data, encoding)](#apidoc.element.fs-extra.output.outputFileSync)

#### [module fs-extra.remove](#apidoc.module.fs-extra.remove)
1.  [function <span class="apidocSignatureSpan">fs-extra.</span>remove (dir, callback)](#apidoc.element.fs-extra.remove.remove)
1.  [function <span class="apidocSignatureSpan">fs-extra.remove.</span>removeSync (dir)](#apidoc.element.fs-extra.remove.removeSync)



# <a name="apidoc.module.fs-extra"></a>[module fs-extra](#apidoc.module.fs-extra)

#### <a name="apidoc.element.fs-extra.FileReadStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>FileReadStream (path, options)](#apidoc.element.fs-extra.FileReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.FileWriteStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>FileWriteStream (path, options)](#apidoc.element.fs-extra.FileWriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ReadStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ReadStream (path, options)](#apidoc.element.fs-extra.ReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.fs-extra.Stats)
- description and source-code
```javascript
function Stats( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec) {
  this.dev = dev;
  this.mode = mode;
  this.nlink = nlink;
  this.uid = uid;
  this.gid = gid;
  this.rdev = rdev;
  this.blksize = blksize;
  this.ino = ino;
  this.size = size;
  this.blocks = blocks;
  this.atime = new Date(atim_msec);
  this.mtime = new Date(mtim_msec);
  this.ctime = new Date(ctim_msec);
  this.birthtime = new Date(birthtim_msec);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.WriteStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>WriteStream (path, options)](#apidoc.element.fs-extra.WriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra._toUnixTimestamp"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>_toUnixTimestamp (time)](#apidoc.element.fs-extra._toUnixTimestamp)
- description and source-code
```javascript
function toUnixTimestamp(time) {
  if (typeof time === 'string' && +time == time) {
    return +time;
  }
  if (typeof time === 'number') {
    if (!Number.isFinite(time) || time < 0) {
      return Date.now() / 1000;
    }
    return time;
  }
  if (util.isDate(time)) {
    // convert to 123.456 UNIX timestamp
    return time.getTime() / 1000;
  }
  throw new Error('Cannot parse time: ' + time);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.access"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>access (path, mode, callback)](#apidoc.element.fs-extra.access)
- description and source-code
```javascript
access = function (path, mode, callback) {
  if (typeof mode === 'function') {
    callback = mode;
    mode = fs.F_OK;
  } else if (typeof callback !== 'function') {
    throw new TypeError('"callback" argument must be a function');
  }

  if (handleError((path = getPathFromURL(path)), callback))
    return;

  if (!nullCheck(path, callback))
    return;

  mode = mode | 0;
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.access(pathModule._makeLong(path), mode, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.accessSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>accessSync (path, mode)](#apidoc.element.fs-extra.accessSync)
- description and source-code
```javascript
accessSync = function (path, mode) {
  handleError((path = getPathFromURL(path)));
  nullCheck(path);

  if (mode === undefined)
    mode = fs.F_OK;
  else
    mode = mode | 0;

  binding.access(pathModule._makeLong(path), mode);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.appendFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>appendFile (path, data, options, cb)](#apidoc.element.fs-extra.appendFile)
- description and source-code
```javascript
function appendFile(path, data, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$appendFile(path, data, options, cb)

  function go$appendFile (path, data, options, cb) {
    return fs$appendFile(path, data, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$appendFile, [path, data, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.appendFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>appendFileSync (path, data, options)](#apidoc.element.fs-extra.appendFileSync)
- description and source-code
```javascript
appendFileSync = function (path, data, options) {
  options = getOptions(options, { encoding: 'utf8', mode: 0o666, flag: 'a' });

  // Don't make changes directly on options object
  options = copyObject(options);

  // force append behavior when using a supplied file descriptor
  if (!options.flag || isFd(path))
    options.flag = 'a';

  fs.writeFileSync(path, data, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.chmod"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>chmod (target, mode, cb)](#apidoc.element.fs-extra.chmod)
- description and source-code
```javascript
chmod = function (target, mode, cb) {
  return orig.call(fs, target, mode, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.chmodSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>chmodSync (target, mode)](#apidoc.element.fs-extra.chmodSync)
- description and source-code
```javascript
chmodSync = function (target, mode) {
  try {
    return orig.call(fs, target, mode)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.chown"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>chown (target, uid, gid, cb)](#apidoc.element.fs-extra.chown)
- description and source-code
```javascript
chown = function (target, uid, gid, cb) {
  return orig.call(fs, target, uid, gid, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
...
* https://github.com/jprichardson/node-fs-extra/issues/2
* https://github.com/flatiron/utile/issues/11
* https://github.com/ryanmcgrath/wrench-js/issues/29
* https://github.com/substack/node-mkdirp/issues/17

First, I believe that in as many cases as possible, the [Node.js naming schemes](http://nodejs.org/api/fs.html) should be chosen
. However, there are problems with the Node.js own naming schemes.

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.
...
```

#### <a name="apidoc.element.fs-extra.chownSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>chownSync (target, uid, gid)](#apidoc.element.fs-extra.chownSync)
- description and source-code
```javascript
chownSync = function (target, uid, gid) {
  try {
    return orig.call(fs, target, uid, gid)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.close"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>close (fd, cb)](#apidoc.element.fs-extra.close)
- description and source-code
```javascript
close = function (fd, cb) {
  return fs$close.call(fs, fd, function (err) {
    if (!err)
      retry()

    if (typeof cb === 'function')
      cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.closeSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>closeSync (fd)](#apidoc.element.fs-extra.closeSync)
- description and source-code
```javascript
closeSync = function (fd) {
  // Note that graceful-fs also retries when fs.closeSync() fails.
  // Looks like a bug to me, although it's probably a harmless one.
  var rval = fs$closeSync.apply(fs, arguments)
  retry()
  return rval
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.copy"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>copy (src, dest, options, callback)](#apidoc.element.fs-extra.copy)
- description and source-code
```javascript
function copy(src, dest, options, callback) {
  if (typeof options === 'function' && !callback) {
    callback = options
    options = {}
  } else if (typeof options === 'function' || options instanceof RegExp) {
    options = {filter: options}
  }
  callback = callback || function () {}
  options = options || {}

  // Warn about using preserveTimestamps on 32-bit node:
  if (options.preserveTimestamps && process.arch === 'ia32') {
    console.warn('fs-extra: Using the preserveTimestamps option in 32-bit node is not recommended;\n
    see https://github.com/jprichardson/node-fs-extra/issues/269')
  }

  // don't allow src and dest to be the same
  const basePath = process.cwd()
  const currentPath = path.resolve(basePath, src)
  const targetPath = path.resolve(basePath, dest)
  if (currentPath === targetPath) return callback(new Error('Source and destination must not be the same.'))

  fs.lstat(src, (err, stats) => {
    if (err) return callback(err)

    let dir = null
    if (stats.isDirectory()) {
      const parts = dest.split(path.sep)
      parts.pop()
      dir = parts.join(path.sep)
    } else {
      dir = path.dirname(dest)
    }

    fs.exists(dir, dirExists => {
      if (dirExists) return ncp(src, dest, options, callback)
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        ncp(src, dest, options, callback)
      })
    })
  })
}
```
- example usage
```shell
...
Sync methods on the other hand will throw if an error occurs.

Example:

'''js
const fs = require('fs-extra')

fs.copy('/tmp/myfile', '/tmp/mynewfile', err => {
if (err) return console.error(err)
console.log("success!")
});

try {
fs.copySync('/tmp/myfile', '/tmp/mynewfile')
console.log("success!")
...
```

#### <a name="apidoc.element.fs-extra.copySync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>copySync (src, dest, options)](#apidoc.element.fs-extra.copySync)
- description and source-code
```javascript
function copySync(src, dest, options) {
  if (typeof options === 'function' || options instanceof RegExp) {
    options = {filter: options}
  }

  options = options || {}
  options.recursive = !!options.recursive

  // default to true for now
  options.clobber = 'clobber' in options ? !!options.clobber : true
  // overwrite falls back to clobber
  options.overwrite = 'overwrite' in options ? !!options.overwrite : options.clobber
  options.dereference = 'dereference' in options ? !!options.dereference : false
  options.preserveTimestamps = 'preserveTimestamps' in options ? !!options.preserveTimestamps : false

  options.filter = options.filter || function () { return true }

  // Warn about using preserveTimestamps on 32-bit node:
  if (options.preserveTimestamps && process.arch === 'ia32') {
    console.warn('fs-extra: Using the preserveTimestamps option in 32-bit node is not recommended;\n
    see https://github.com/jprichardson/node-fs-extra/issues/269')
  }

  const stats = (options.recursive && !options.dereference) ? fs.lstatSync(src) : fs.statSync(src)
  const destFolder = path.dirname(dest)
  const destFolderExists = fs.existsSync(destFolder)
  let performCopy = false

  if (options.filter instanceof RegExp) {
    console.warn('Warning: fs-extra: Passing a RegExp filter is deprecated, use a function')
    performCopy = options.filter.test(src)
  } else if (typeof options.filter === 'function') performCopy = options.filter(src, dest)

  if (stats.isFile() && performCopy) {
    if (!destFolderExists) mkdir.mkdirsSync(destFolder)
    copyFileSync(src, dest, {
      overwrite: options.overwrite,
      errorOnExist: options.errorOnExist,
      preserveTimestamps: options.preserveTimestamps
    })
  } else if (stats.isDirectory() && performCopy) {
    if (!fs.existsSync(dest)) mkdir.mkdirsSync(dest)
    const contents = fs.readdirSync(src)
    contents.forEach(content => {
      const opts = options
      opts.recursive = true
      copySync(path.join(src, content), path.join(dest, content), opts)
    })
  } else if (options.recursive && stats.isSymbolicLink() && performCopy) {
    const srcPath = fs.readlinkSync(src)
    fs.symlinkSync(srcPath, dest)
  }
}
```
- example usage
```shell
...

fs.copy('/tmp/myfile', '/tmp/mynewfile', err => {
  if (err) return console.error(err)
  console.log("success!")
});

try {
  fs.copySync('/tmp/myfile', '/tmp/mynewfile')
  console.log("success!")
} catch (err) {
  console.error(err)
}
'''
...
```

#### <a name="apidoc.element.fs-extra.createFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createFile (file, callback)](#apidoc.element.fs-extra.createFile)
- description and source-code
```javascript
function createFile(file, callback) {
  function makeFile () {
    fs.writeFile(file, '', err => {
      if (err) return callback(err)
      callback()
    })
  }

  fs.exists(file, fileExists => {
    if (fileExists) return callback()
    const dir = path.dirname(file)
    fs.exists(dir, dirExists => {
      if (dirExists) return makeFile()
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        makeFile()
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createFileSync (file)](#apidoc.element.fs-extra.createFileSync)
- description and source-code
```javascript
function createFileSync(file) {
  if (fs.existsSync(file)) return

  const dir = path.dirname(file)
  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  fs.writeFileSync(file, '')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createLink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.createLink)
- description and source-code
```javascript
function createLink(srcpath, dstpath, callback) {
  function makeLink (srcpath, dstpath) {
    fs.link(srcpath, dstpath, err => {
      if (err) return callback(err)
      callback(null)
    })
  }

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    fs.lstat(srcpath, (err, stat) => {
      if (err) {
        err.message = err.message.replace('lstat', 'ensureLink')
        return callback(err)
      }

      const dir = path.dirname(dstpath)
      fs.exists(dir, dirExists => {
        if (dirExists) return makeLink(srcpath, dstpath)
        mkdir.mkdirs(dir, err => {
          if (err) return callback(err)
          makeLink(srcpath, dstpath)
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createLinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.createLinkSync)
- description and source-code
```javascript
function createLinkSync(srcpath, dstpath, callback) {
  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  try {
    fs.lstatSync(srcpath)
  } catch (err) {
    err.message = err.message.replace('lstat', 'ensureLink')
    throw err
  }

  const dir = path.dirname(dstpath)
  const dirExists = fs.existsSync(dir)
  if (dirExists) return fs.linkSync(srcpath, dstpath)
  mkdir.mkdirsSync(dir)

  return fs.linkSync(srcpath, dstpath)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createReadStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createReadStream (path, options)](#apidoc.element.fs-extra.createReadStream)
- description and source-code
```javascript
function createReadStream(path, options) {
  return new ReadStream(path, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createSymlink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.createSymlink)
- description and source-code
```javascript
function createSymlink(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    symlinkPaths(srcpath, dstpath, (err, relative) => {
      if (err) return callback(err)
      srcpath = relative.toDst
      symlinkType(relative.toCwd, type, (err, type) => {
        if (err) return callback(err)
        const dir = path.dirname(dstpath)
        fs.exists(dir, dirExists => {
          if (dirExists) return fs.symlink(srcpath, dstpath, type, callback)
          mkdirs(dir, err => {
            if (err) return callback(err)
            fs.symlink(srcpath, dstpath, type, callback)
          })
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createSymlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.createSymlinkSync)
- description and source-code
```javascript
function createSymlinkSync(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  const relative = symlinkPathsSync(srcpath, dstpath)
  srcpath = relative.toDst
  type = symlinkTypeSync(relative.toCwd, type)
  const dir = path.dirname(dstpath)
  const exists = fs.existsSync(dir)
  if (exists) return fs.symlinkSync(srcpath, dstpath, type)
  mkdirsSync(dir)
  return fs.symlinkSync(srcpath, dstpath, type)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.createWriteStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>createWriteStream (path, options)](#apidoc.element.fs-extra.createWriteStream)
- description and source-code
```javascript
function createWriteStream(path, options) {
  return new WriteStream(path, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.emptyDir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>emptyDir (dir, callback)](#apidoc.element.fs-extra.emptyDir)
- description and source-code
```javascript
function emptyDir(dir, callback) {
  callback = callback || function () {}
  fs.readdir(dir, (err, items) => {
    if (err) return mkdir.mkdirs(dir, callback)

    items = items.map(item => path.join(dir, item))

    deleteItem()

    function deleteItem () {
      const item = items.pop()
      if (!item) return callback()
      remove.remove(item, err => {
        if (err) return callback(err)
        deleteItem()
      })
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.emptyDirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>emptyDirSync (dir)](#apidoc.element.fs-extra.emptyDirSync)
- description and source-code
```javascript
function emptyDirSync(dir) {
  let items
  try {
    items = fs.readdirSync(dir)
  } catch (err) {
    return mkdir.mkdirsSync(dir)
  }

  items.forEach(item => {
    item = path.join(dir, item)
    remove.removeSync(item)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.emptydir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>emptydir (dir, callback)](#apidoc.element.fs-extra.emptydir)
- description and source-code
```javascript
function emptyDir(dir, callback) {
  callback = callback || function () {}
  fs.readdir(dir, (err, items) => {
    if (err) return mkdir.mkdirs(dir, callback)

    items = items.map(item => path.join(dir, item))

    deleteItem()

    function deleteItem () {
      const item = items.pop()
      if (!item) return callback()
      remove.remove(item, err => {
        if (err) return callback(err)
        deleteItem()
      })
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.emptydirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>emptydirSync (dir)](#apidoc.element.fs-extra.emptydirSync)
- description and source-code
```javascript
function emptyDirSync(dir) {
  let items
  try {
    items = fs.readdirSync(dir)
  } catch (err) {
    return mkdir.mkdirsSync(dir)
  }

  items.forEach(item => {
    item = path.join(dir, item)
    remove.removeSync(item)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureDir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureDir (p, opts, callback, made)](#apidoc.element.fs-extra.ensureDir)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureDirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureDirSync (p, opts, made)](#apidoc.element.fs-extra.ensureDirSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureFile (file, callback)](#apidoc.element.fs-extra.ensureFile)
- description and source-code
```javascript
function createFile(file, callback) {
  function makeFile () {
    fs.writeFile(file, '', err => {
      if (err) return callback(err)
      callback()
    })
  }

  fs.exists(file, fileExists => {
    if (fileExists) return callback()
    const dir = path.dirname(file)
    fs.exists(dir, dirExists => {
      if (dirExists) return makeFile()
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        makeFile()
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureFileSync (file)](#apidoc.element.fs-extra.ensureFileSync)
- description and source-code
```javascript
function createFileSync(file) {
  if (fs.existsSync(file)) return

  const dir = path.dirname(file)
  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  fs.writeFileSync(file, '')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureLink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensureLink)
- description and source-code
```javascript
function createLink(srcpath, dstpath, callback) {
  function makeLink (srcpath, dstpath) {
    fs.link(srcpath, dstpath, err => {
      if (err) return callback(err)
      callback(null)
    })
  }

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    fs.lstat(srcpath, (err, stat) => {
      if (err) {
        err.message = err.message.replace('lstat', 'ensureLink')
        return callback(err)
      }

      const dir = path.dirname(dstpath)
      fs.exists(dir, dirExists => {
        if (dirExists) return makeLink(srcpath, dstpath)
        mkdir.mkdirs(dir, err => {
          if (err) return callback(err)
          makeLink(srcpath, dstpath)
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureLinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensureLinkSync)
- description and source-code
```javascript
function createLinkSync(srcpath, dstpath, callback) {
  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  try {
    fs.lstatSync(srcpath)
  } catch (err) {
    err.message = err.message.replace('lstat', 'ensureLink')
    throw err
  }

  const dir = path.dirname(dstpath)
  const dirExists = fs.existsSync(dir)
  if (dirExists) return fs.linkSync(srcpath, dstpath)
  mkdir.mkdirsSync(dir)

  return fs.linkSync(srcpath, dstpath)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureSymlink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensureSymlink)
- description and source-code
```javascript
function createSymlink(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    symlinkPaths(srcpath, dstpath, (err, relative) => {
      if (err) return callback(err)
      srcpath = relative.toDst
      symlinkType(relative.toCwd, type, (err, type) => {
        if (err) return callback(err)
        const dir = path.dirname(dstpath)
        fs.exists(dir, dirExists => {
          if (dirExists) return fs.symlink(srcpath, dstpath, type, callback)
          mkdirs(dir, err => {
            if (err) return callback(err)
            fs.symlink(srcpath, dstpath, type, callback)
          })
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensureSymlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ensureSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensureSymlinkSync)
- description and source-code
```javascript
function createSymlinkSync(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  const relative = symlinkPathsSync(srcpath, dstpath)
  srcpath = relative.toDst
  type = symlinkTypeSync(relative.toCwd, type)
  const dir = path.dirname(dstpath)
  const exists = fs.existsSync(dir)
  if (exists) return fs.symlinkSync(srcpath, dstpath, type)
  mkdirsSync(dir)
  return fs.symlinkSync(srcpath, dstpath, type)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.exists"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>exists (path, callback)](#apidoc.element.fs-extra.exists)
- description and source-code
```javascript
exists = function (path, callback) {
  if (handleError((path = getPathFromURL(path)), cb))
    return;
  if (!nullCheck(path, cb)) return;
  var req = new FSReqWrap();
  req.oncomplete = cb;
  binding.stat(pathModule._makeLong(path), req);
  function cb(err, stats) {
    if (callback) callback(err ? false : true);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.existsSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>existsSync (path)](#apidoc.element.fs-extra.existsSync)
- description and source-code
```javascript
existsSync = function (path) {
  try {
    handleError((path = getPathFromURL(path)));
    nullCheck(path);
    binding.stat(pathModule._makeLong(path), statValues);
    return true;
  } catch (e) {
    return false;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fchmod"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fchmod (target, mode, cb)](#apidoc.element.fs-extra.fchmod)
- description and source-code
```javascript
fchmod = function (target, mode, cb) {
  return orig.call(fs, target, mode, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fchmodSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fchmodSync (target, mode)](#apidoc.element.fs-extra.fchmodSync)
- description and source-code
```javascript
fchmodSync = function (target, mode) {
  try {
    return orig.call(fs, target, mode)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fchown"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fchown (target, uid, gid, cb)](#apidoc.element.fs-extra.fchown)
- description and source-code
```javascript
fchown = function (target, uid, gid, cb) {
  return orig.call(fs, target, uid, gid, function (er) {
    if (chownErOk(er)) er = null
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fchownSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fchownSync (target, uid, gid)](#apidoc.element.fs-extra.fchownSync)
- description and source-code
```javascript
fchownSync = function (target, uid, gid) {
  try {
    return orig.call(fs, target, uid, gid)
  } catch (er) {
    if (!chownErOk(er)) throw er
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fdatasync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fdatasync (fd, callback)](#apidoc.element.fs-extra.fdatasync)
- description and source-code
```javascript
fdatasync = function (fd, callback) {
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.fdatasync(fd, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fdatasyncSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fdatasyncSync (fd)](#apidoc.element.fs-extra.fdatasyncSync)
- description and source-code
```javascript
fdatasyncSync = function (fd) {
  return binding.fdatasync(fd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fstat"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fstat (target, cb)](#apidoc.element.fs-extra.fstat)
- description and source-code
```javascript
fstat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fstatSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fstatSync (target)](#apidoc.element.fs-extra.fstatSync)
- description and source-code
```javascript
fstatSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fsync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fsync (fd, callback)](#apidoc.element.fs-extra.fsync)
- description and source-code
```javascript
fsync = function (fd, callback) {
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.fsync(fd, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.fsyncSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>fsyncSync (fd)](#apidoc.element.fs-extra.fsyncSync)
- description and source-code
```javascript
fsyncSync = function (fd) {
  return binding.fsync(fd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ftruncate"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ftruncate (fd, len, callback)](#apidoc.element.fs-extra.ftruncate)
- description and source-code
```javascript
ftruncate = function (fd, len, callback) {
  if (typeof len === 'function') {
    callback = len;
    len = 0;
  } else if (len === undefined) {
    len = 0;
  }
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.ftruncate(fd, len, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ftruncateSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ftruncateSync (fd, len)](#apidoc.element.fs-extra.ftruncateSync)
- description and source-code
```javascript
ftruncateSync = function (fd, len) {
  if (len === undefined) {
    len = 0;
  }
  return binding.ftruncate(fd, len);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.futimes"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>futimes (fd, atime, mtime, callback)](#apidoc.element.fs-extra.futimes)
- description and source-code
```javascript
futimes = function (fd, atime, mtime, callback) {
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  var req = new FSReqWrap();
  req.oncomplete = makeCallback(callback);
  binding.futimes(fd, atime, mtime, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.futimesSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>futimesSync (fd, atime, mtime)](#apidoc.element.fs-extra.futimesSync)
- description and source-code
```javascript
futimesSync = function (fd, atime, mtime) {
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  binding.futimes(fd, atime, mtime);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.gracefulify"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>gracefulify (fs)](#apidoc.element.fs-extra.gracefulify)
- description and source-code
```javascript
function patch(fs) {
  // Everything that references the open() function needs to be in here
  polyfills(fs)
  fs.gracefulify = patch
  fs.FileReadStream = ReadStream;  // Legacy name.
  fs.FileWriteStream = WriteStream;  // Legacy name.
  fs.createReadStream = createReadStream
  fs.createWriteStream = createWriteStream
  var fs$readFile = fs.readFile
  fs.readFile = readFile
  function readFile (path, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$readFile(path, options, cb)

    function go$readFile (path, options, cb) {
      return fs$readFile(path, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$readFile, [path, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$writeFile = fs.writeFile
  fs.writeFile = writeFile
  function writeFile (path, data, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$writeFile(path, data, options, cb)

    function go$writeFile (path, data, options, cb) {
      return fs$writeFile(path, data, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$writeFile, [path, data, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$appendFile = fs.appendFile
  if (fs$appendFile)
    fs.appendFile = appendFile
  function appendFile (path, data, options, cb) {
    if (typeof options === 'function')
      cb = options, options = null

    return go$appendFile(path, data, options, cb)

    function go$appendFile (path, data, options, cb) {
      return fs$appendFile(path, data, options, function (err) {
        if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
          enqueue([go$appendFile, [path, data, options, cb]])
        else {
          if (typeof cb === 'function')
            cb.apply(this, arguments)
          retry()
        }
      })
    }
  }

  var fs$readdir = fs.readdir
  fs.readdir = readdir
  function readdir (path, options, cb) {
    var args = [path]
    if (typeof options !== 'function') {
      args.push(options)
    } else {
      cb = options
    }
    args.push(go$readdir$cb)

    return go$readdir(args)

    function go$readdir$cb (err, files) {
      if (files && files.sort)
        files.sort()

      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$readdir, [args]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    }
  }

  function go$readdir (args) {
    return fs$readdir.apply(fs, args)
  }

  if (process.version.substr(0, 4) === 'v0.8') {
    var legStreams = legacy(fs)
    ReadStream = legStreams.ReadStream
    WriteStream = legStreams.WriteStream
  }

  var fs$ReadStream = fs.ReadStream
  ReadStream.prototype = Object.create(fs$ReadStream.prototype)
  ReadStream.prototype.open = ReadStream$open

  var fs$WriteStream = fs.WriteStream
  WriteStream.prototype = Object.create(fs$WriteStream.prototype)
  WriteStream.prototype.open = WriteStream$open

  fs.ReadStream = ReadStream
  fs.WriteStream = WriteStream

  function ReadStream (path, options) {
    if (this instanceof ReadStream)
      return fs$ReadStream.apply(this, arguments), this
    else
      return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
  }

  function ReadStream$open () {
    var that = this
    open(that.path, that.flags, that.mode, function (err, fd) {
      if (err) {
        if (that.autoClose)
          that.destroy()

        that.emit('error', err)
      } else {
        that.fd = fd
        that.emit('open', fd)
        that.read()
      }
    })
  }

  function WriteStream (path, options) {
    if (this instanceof WriteStream)
      return fs$WriteStream.apply(this, arguments), this
    else
      return W ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lchmod"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lchmod (path, mode, cb)](#apidoc.element.fs-extra.lchmod)
- description and source-code
```javascript
lchmod = function (path, mode, cb) {
  if (cb) process.nextTick(cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lchmodSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lchmodSync ()](#apidoc.element.fs-extra.lchmodSync)
- description and source-code
```javascript
lchmodSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lchown"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lchown (path, uid, gid, cb)](#apidoc.element.fs-extra.lchown)
- description and source-code
```javascript
lchown = function (path, uid, gid, cb) {
  if (cb) process.nextTick(cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lchownSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lchownSync ()](#apidoc.element.fs-extra.lchownSync)
- description and source-code
```javascript
lchownSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.link"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>link (existingPath, newPath, callback)](#apidoc.element.fs-extra.link)
- description and source-code
```javascript
link = function (existingPath, newPath, callback) {
  callback = makeCallback(callback);

  if (handleError((existingPath = getPathFromURL(existingPath)), callback))
    return;

  if (handleError((newPath = getPathFromURL(newPath)), callback))
    return;

  if (!nullCheck(existingPath, callback)) return;
  if (!nullCheck(newPath, callback)) return;

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.link(pathModule._makeLong(existingPath),
               pathModule._makeLong(newPath),
               req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.linkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>linkSync (existingPath, newPath)](#apidoc.element.fs-extra.linkSync)
- description and source-code
```javascript
linkSync = function (existingPath, newPath) {
  handleError((existingPath = getPathFromURL(existingPath)));
  handleError((newPath = getPathFromURL(newPath)));
  nullCheck(existingPath);
  nullCheck(newPath);
  return binding.link(pathModule._makeLong(existingPath),
                      pathModule._makeLong(newPath));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lstat"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lstat (target, cb)](#apidoc.element.fs-extra.lstat)
- description and source-code
```javascript
lstat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lstatSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lstatSync (target)](#apidoc.element.fs-extra.lstatSync)
- description and source-code
```javascript
lstatSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lutimes"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lutimes (_a, _b, _c, cb)](#apidoc.element.fs-extra.lutimes)
- description and source-code
```javascript
lutimes = function (_a, _b, _c, cb) { if (cb) process.nextTick(cb) }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.lutimesSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>lutimesSync ()](#apidoc.element.fs-extra.lutimesSync)
- description and source-code
```javascript
lutimesSync = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdir (path, mode, callback)](#apidoc.element.fs-extra.mkdir)
- description and source-code
```javascript
mkdir = function (path, mode, callback) {
  if (typeof mode === 'function') callback = mode;
  callback = makeCallback(callback);
  if (handleError((path = getPathFromURL(path)), callback))
    return;
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.mkdir(pathModule._makeLong(path),
                modeNum(mode, 0o777),
                req);
}
```
- example usage
```shell
...
* https://github.com/jprichardson/node-fs-extra/issues/2
* https://github.com/flatiron/utile/issues/11
* https://github.com/ryanmcgrath/wrench-js/issues/29
* https://github.com/substack/node-mkdirp/issues/17

First, I believe that in as many cases as possible, the [Node.js naming schemes](http://nodejs.org/api/fs.html) should be chosen
. However, there are problems with the Node.js own naming schemes.

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.
...
```

#### <a name="apidoc.element.fs-extra.mkdirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirSync (path, mode)](#apidoc.element.fs-extra.mkdirSync)
- description and source-code
```javascript
mkdirSync = function (path, mode) {
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.mkdir(pathModule._makeLong(path),
                       modeNum(mode, 0o777));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdirp"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirp (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirp)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.mkdirpSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirpSync (p, opts, made)](#apidoc.element.fs-extra.mkdirpSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdirs"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirs (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.mkdirsSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirsSync (p, opts, made)](#apidoc.element.fs-extra.mkdirsSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdtemp"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdtemp (prefix, options, callback)](#apidoc.element.fs-extra.mkdtemp)
- description and source-code
```javascript
mkdtemp = function (prefix, options, callback) {
  callback = makeCallback(typeof options === 'function' ? options : callback);
  options = getOptions(options, {});
  if (!prefix || typeof prefix !== 'string')
    throw new TypeError('filename prefix is required');
  if (!nullCheck(prefix, callback)) {
    return;
  }

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.mkdtemp(prefix + 'XXXXXX', options.encoding, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdtempSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdtempSync (prefix, options)](#apidoc.element.fs-extra.mkdtempSync)
- description and source-code
```javascript
mkdtempSync = function (prefix, options) {
  if (!prefix || typeof prefix !== 'string')
    throw new TypeError('filename prefix is required');
  options = getOptions(options, {});
  nullCheck(prefix);
  return binding.mkdtemp(prefix + 'XXXXXX', options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.move"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>move (source, dest, options, callback)](#apidoc.element.fs-extra.move)
- description and source-code
```javascript
function move(source, dest, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const shouldMkdirp = ('mkdirp' in options) ? options.mkdirp : true
  const overwrite = options.overwrite || options.clobber || false

  if (shouldMkdirp) {
    mkdirs()
  } else {
    doRename()
  }

  function mkdirs () {
    mkdirp(path.dirname(dest), err => {
      if (err) return callback(err)
      doRename()
    })
  }

  function doRename () {
    if (path.resolve(source) === path.resolve(dest)) {
      setImmediate(callback)
    } else if (overwrite) {
      fs.rename(source, dest, err => {
        if (!err) return callback()

        if (err.code === 'ENOTEMPTY' || err.code === 'EEXIST') {
          remove(dest, err => {
            if (err) return callback(err)
            options.overwrite = false // just overwriteed it, no need to do it again
            move(source, dest, options, callback)
          })
          return
        }

        // weird Windows shit
        if (err.code === 'EPERM') {
          setTimeout(() => {
            remove(dest, err => {
              if (err) return callback(err)
              options.overwrite = false
              move(source, dest, options, callback)
            })
          }, 200)
          return
        }

        if (err.code !== 'EXDEV') return callback(err)
        moveAcrossDevice(source, dest, overwrite, callback)
      })
    } else {
      fs.link(source, dest, err => {
        if (err) {
          if (err.code === 'EXDEV' || err.code === 'EISDIR' || err.code === 'EPERM' || err.code === 'ENOTSUP') {
            moveAcrossDevice(source, dest, overwrite, callback)
            return
          }
          callback(err)
          return
        }
        fs.unlink(source, callback)
      })
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.moveSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>moveSync (src, dest, options)](#apidoc.element.fs-extra.moveSync)
- description and source-code
```javascript
function moveSync(src, dest, options) {
  options = options || {}
  const overwrite = options.overwrite || options.clobber || false

  src = path.resolve(src)
  dest = path.resolve(dest)

  if (src === dest) return

  if (isSrcSubdir(src, dest)) throw new Error('Cannot move '${src}' into itself '${dest}'.')

  mkdirpSync(path.dirname(dest))
  tryRenameSync()

  function tryRenameSync () {
    if (overwrite) {
      try {
        return fs.renameSync(src, dest)
      } catch (err) {
        if (err.code === 'ENOTEMPTY' || err.code === 'EEXIST' || err.code === 'EPERM') {
          removeSync(dest)
          options.overwrite = false // just overwriteed it, no need to do it again
          return moveSync(src, dest, options)
        }

        if (err.code !== 'EXDEV') throw err
        return moveSyncAcrossDevice(src, dest, overwrite)
      }
    } else {
      try {
        fs.linkSync(src, dest)
        return fs.unlinkSync(src)
      } catch (err) {
        if (err.code === 'EXDEV' || err.code === 'EISDIR' || err.code === 'EPERM' || err.code === 'ENOTSUP') {
          return moveSyncAcrossDevice(src, dest, overwrite)
        }
        throw err
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.open"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>open (path, flags, mode, cb)](#apidoc.element.fs-extra.open)
- description and source-code
```javascript
function open(path, flags, mode, cb) {
  if (typeof mode === 'function')
    cb = mode, mode = null

  return go$open(path, flags, mode, cb)

  function go$open (path, flags, mode, cb) {
    return fs$open(path, flags, mode, function (err, fd) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$open, [path, flags, mode, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.openSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>openSync (path, flags, mode)](#apidoc.element.fs-extra.openSync)
- description and source-code
```javascript
openSync = function (path, flags, mode) {
  mode = modeNum(mode, 0o666);
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.open(pathModule._makeLong(path), stringToFlags(flags), mode);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputFile (file, data, encoding, callback)](#apidoc.element.fs-extra.outputFile)
- description and source-code
```javascript
function outputFile(file, data, encoding, callback) {
  if (typeof encoding === 'function') {
    callback = encoding
    encoding = 'utf8'
  }

  const dir = path.dirname(file)
  fs.exists(dir, itDoes => {
    if (itDoes) return fs.writeFile(file, data, encoding, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)

      fs.writeFile(file, data, encoding, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputFileSync (file, data, encoding)](#apidoc.element.fs-extra.outputFileSync)
- description and source-code
```javascript
function outputFileSync(file, data, encoding) {
  const dir = path.dirname(file)
  if (fs.existsSync(dir)) {
    return fs.writeFileSync.apply(fs, arguments)
  }
  mkdir.mkdirsSync(dir)
  fs.writeFileSync.apply(fs, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputJSON (file, data, options, callback)](#apidoc.element.fs-extra.outputJSON)
- description and source-code
```javascript
function outputJson(file, data, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const dir = path.dirname(file)

  fs.exists(dir, itDoes => {
    if (itDoes) return jsonFile.writeJson(file, data, options, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)
      jsonFile.writeJson(file, data, options, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputJSONSync (file, data, options)](#apidoc.element.fs-extra.outputJSONSync)
- description and source-code
```javascript
function outputJsonSync(file, data, options) {
  const dir = path.dirname(file)

  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  jsonFile.writeJsonSync(file, data, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputJson"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputJson (file, data, options, callback)](#apidoc.element.fs-extra.outputJson)
- description and source-code
```javascript
function outputJson(file, data, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const dir = path.dirname(file)

  fs.exists(dir, itDoes => {
    if (itDoes) return jsonFile.writeJson(file, data, options, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)
      jsonFile.writeJson(file, data, options, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.outputJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>outputJsonSync (file, data, options)](#apidoc.element.fs-extra.outputJsonSync)
- description and source-code
```javascript
function outputJsonSync(file, data, options) {
  const dir = path.dirname(file)

  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  jsonFile.writeJsonSync(file, data, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.read"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>read (fd, buffer, offset, length, position, callback_)](#apidoc.element.fs-extra.read)
- description and source-code
```javascript
read = function (fd, buffer, offset, length, position, callback_) {
  var callback
  if (callback_ && typeof callback_ === 'function') {
    var eagCounter = 0
    callback = function (er, _, __) {
      if (er && er.code === 'EAGAIN' && eagCounter < 10) {
        eagCounter ++
        return fs$read.call(fs, fd, buffer, offset, length, position, callback)
      }
      callback_.apply(this, arguments)
    }
  }
  return fs$read.call(fs, fd, buffer, offset, length, position, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readFile (path, options, cb)](#apidoc.element.fs-extra.readFile)
- description and source-code
```javascript
function readFile(path, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$readFile(path, options, cb)

  function go$readFile (path, options, cb) {
    return fs$readFile(path, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$readFile, [path, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
...
* https://github.com/jprichardson/node-fs-extra/issues/2
* https://github.com/flatiron/utile/issues/11
* https://github.com/ryanmcgrath/wrench-js/issues/29
* https://github.com/substack/node-mkdirp/issues/17

First, I believe that in as many cases as possible, the [Node.js naming schemes](http://nodejs.org/api/fs.html) should be chosen
. However, there are problems with the Node.js own naming schemes.

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.
...
```

#### <a name="apidoc.element.fs-extra.readFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readFileSync (path, options)](#apidoc.element.fs-extra.readFileSync)
- description and source-code
```javascript
readFileSync = function (path, options) {
  options = getOptions(options, { flag: 'r' });
  var isUserFd = isFd(path); // file descriptor ownership
  var fd = isUserFd ? path : fs.openSync(path, options.flag || 'r', 0o666);

  var st = tryStatSync(fd, isUserFd);
  var size = st.isFile() ? st.size : 0;
  var pos = 0;
  var buffer; // single buffer with file data
  var buffers; // list for when size is unknown

  if (size === 0) {
    buffers = [];
  } else {
    buffer = tryCreateBuffer(size, fd, isUserFd);
  }

  var bytesRead;

  if (size !== 0) {
    do {
      bytesRead = tryReadSync(fd, isUserFd, buffer, pos, size - pos);
      pos += bytesRead;
    } while (bytesRead !== 0 && pos < size);
  } else {
    do {
      // the kernel lies about many files.
      // Go ahead and try to read some bytes.
      buffer = Buffer.allocUnsafe(8192);
      bytesRead = tryReadSync(fd, isUserFd, buffer, 0, 8192);
      if (bytesRead !== 0) {
        buffers.push(buffer.slice(0, bytesRead));
      }
      pos += bytesRead;
    } while (bytesRead !== 0);
  }

  if (!isUserFd)
    fs.closeSync(fd);

  if (size === 0) {
    // data was collected into the buffers list.
    buffer = Buffer.concat(buffers, pos);
  } else if (pos < size) {
    buffer = buffer.slice(0, pos);
  }

  if (options.encoding) buffer = buffer.toString(options.encoding);
  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readJSON (file, options, callback)](#apidoc.element.fs-extra.readJSON)
- description and source-code
```javascript
function readFile(file, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }

  if (typeof options === 'string') {
    options = {encoding: options}
  }

  options = options || {}
  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  fs.readFile(file, options, function (err, data) {
    if (err) return callback(err)

    data = stripBom(data)

    var obj
    try {
      obj = JSON.parse(data, options ? options.reviver : null)
    } catch (err2) {
      if (shouldThrow) {
        err2.message = file + ': ' + err2.message
        return callback(err2)
      } else {
        return callback(null, null)
      }
    }

    callback(null, obj)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readJSONSync (file, options)](#apidoc.element.fs-extra.readJSONSync)
- description and source-code
```javascript
function readFileSync(file, options) {
  options = options || {}
  if (typeof options === 'string') {
    options = {encoding: options}
  }

  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  var content = fs.readFileSync(file, options)
  content = stripBom(content)

  try {
    return JSON.parse(content, options.reviver)
  } catch (err) {
    if (shouldThrow) {
      err.message = file + ': ' + err.message
      throw err
    } else {
      return null
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readJson"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readJson (file, options, callback)](#apidoc.element.fs-extra.readJson)
- description and source-code
```javascript
function readFile(file, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }

  if (typeof options === 'string') {
    options = {encoding: options}
  }

  options = options || {}
  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  fs.readFile(file, options, function (err, data) {
    if (err) return callback(err)

    data = stripBom(data)

    var obj
    try {
      obj = JSON.parse(data, options ? options.reviver : null)
    } catch (err2) {
      if (shouldThrow) {
        err2.message = file + ': ' + err2.message
        return callback(err2)
      } else {
        return callback(null, null)
      }
    }

    callback(null, obj)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readJsonSync (file, options)](#apidoc.element.fs-extra.readJsonSync)
- description and source-code
```javascript
function readFileSync(file, options) {
  options = options || {}
  if (typeof options === 'string') {
    options = {encoding: options}
  }

  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  var content = fs.readFileSync(file, options)
  content = stripBom(content)

  try {
    return JSON.parse(content, options.reviver)
  } catch (err) {
    if (shouldThrow) {
      err.message = file + ': ' + err.message
      throw err
    } else {
      return null
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readSync (fd, buffer, offset, length, position)](#apidoc.element.fs-extra.readSync)
- description and source-code
```javascript
readSync = function (fd, buffer, offset, length, position) {
  var eagCounter = 0
  while (true) {
    try {
      return fs$readSync.call(fs, fd, buffer, offset, length, position)
    } catch (er) {
      if (er.code === 'EAGAIN' && eagCounter < 10) {
        eagCounter ++
        continue
      }
      throw er
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readdir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readdir (path, options, cb)](#apidoc.element.fs-extra.readdir)
- description and source-code
```javascript
function readdir(path, options, cb) {
  var args = [path]
  if (typeof options !== 'function') {
    args.push(options)
  } else {
    cb = options
  }
  args.push(go$readdir$cb)

  return go$readdir(args)

  function go$readdir$cb (err, files) {
    if (files && files.sort)
      files.sort()

    if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
      enqueue([go$readdir, [args]])
    else {
      if (typeof cb === 'function')
        cb.apply(this, arguments)
      retry()
    }
  }
}
```
- example usage
```shell
...
* https://github.com/jprichardson/node-fs-extra/issues/2
* https://github.com/flatiron/utile/issues/11
* https://github.com/ryanmcgrath/wrench-js/issues/29
* https://github.com/substack/node-mkdirp/issues/17

First, I believe that in as many cases as possible, the [Node.js naming schemes](http://nodejs.org/api/fs.html) should be chosen
. However, there are problems with the Node.js own naming schemes.

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.
...
```

#### <a name="apidoc.element.fs-extra.readdirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readdirSync (path, options)](#apidoc.element.fs-extra.readdirSync)
- description and source-code
```javascript
readdirSync = function (path, options) {
  options = getOptions(options, {});
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.readdir(pathModule._makeLong(path), options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readlink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readlink (path, options, callback)](#apidoc.element.fs-extra.readlink)
- description and source-code
```javascript
readlink = function (path, options, callback) {
  callback = makeCallback(typeof options === 'function' ? options : callback);
  options = getOptions(options, {});
  if (handleError((path = getPathFromURL(path)), callback))
    return;
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.readlink(pathModule._makeLong(path), options.encoding, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.readlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>readlinkSync (path, options)](#apidoc.element.fs-extra.readlinkSync)
- description and source-code
```javascript
readlinkSync = function (path, options) {
  options = getOptions(options, {});
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.readlink(pathModule._makeLong(path), options.encoding);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.realpath"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>realpath (p, options, callback)](#apidoc.element.fs-extra.realpath)
- description and source-code
```javascript
function realpath(p, options, callback) {
  callback = maybeCallback(typeof options === 'function' ? options : callback);
  options = getOptions(options, {});
  if (handleError((p = getPathFromURL(p)), callback))
    return;
  if (!nullCheck(p, callback))
    return;

  p = p.toString('utf8');
  p = pathModule.resolve(p);

  const seenLinks = {};
  const knownHard = {};

  // current character position in p
  var pos;
  // the partial path so far, including a trailing slash if any
  var current;
  // the partial path without a trailing slash (except when pointing at a root)
  var base;
  // the partial path scanned in the previous round, with slash
  var previous;

  start();

  function start() {
    // Skip over roots
    var m = splitRootRe.exec(p);
    pos = m[0].length;
    current = m[0];
    base = m[0];
    previous = '';

    // On windows, check that the root exists. On unix there is no need.
    if (isWindows && !knownHard[base]) {
      fs.lstat(base, function(err) {
        if (err) return callback(err);
        knownHard[base] = true;
        LOOP();
      });
    } else {
      process.nextTick(LOOP);
    }
  }

  // walk down the path, swapping out linked pathparts for their real
  // values
  function LOOP() {
    // stop if scanned past end of path
    if (pos >= p.length) {
      return callback(null, encodeRealpathResult(p, options));
    }

    // find the next part
    nextPartRe.lastIndex = pos;
    var result = nextPartRe.exec(p);
    previous = current;
    current += result[0];
    base = previous + result[1];
    pos = nextPartRe.lastIndex;

    // continue if not a symlink
    if (knownHard[base]) {
      return process.nextTick(LOOP);
    }

    return fs.lstat(base, gotStat);
  }

  function gotStat(err, stat) {
    if (err) return callback(err);

    // if not a symlink, skip to the next path part
    if (!stat.isSymbolicLink()) {
      knownHard[base] = true;
      return process.nextTick(LOOP);
    }

    // stat & read the link if not read before
    // call gotTarget as soon as the link target is known
    // dev/ino always return 0 on windows, so skip the check.
    let id;
    if (!isWindows) {
      id = '${stat.dev.toString(32)}:${stat.ino.toString(32)}';
      if (seenLinks.hasOwnProperty(id)) {
        return gotTarget(null, seenLinks[id], base);
      }
    }
    fs.stat(base, function(err) {
      if (err) return callback(err);

      fs.readlink(base, function(err, target) {
        if (!isWindows) seenLinks[id] = target;
        gotTarget(err, target);
      });
    });
  }

  function gotTarget(err, target, base) {
    if (err) return callback(err);

    var resolvedLink = pathModule.resolve(previous, target);
    gotResolvedLink(resolvedLink);
  }

  function gotResolvedLink(resolvedLink) {
    // resolve the link, then start over
    p = pathModule.resolve(resolvedLink, p.slice(pos));
    start();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.realpathSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>realpathSync (p, options)](#apidoc.element.fs-extra.realpathSync)
- description and source-code
```javascript
function realpathSync(p, options) {
  options = getOptions(options, {});
  handleError((p = getPathFromURL(p)));
  nullCheck(p);

  p = p.toString('utf8');
  p = pathModule.resolve(p);

  const seenLinks = {};
  const knownHard = {};
  const cache = options[internalFS.realpathCacheKey];
  const original = p;

  const maybeCachedResult = cache && cache.get(p);
  if (maybeCachedResult) {
    return maybeCachedResult;
  }

  // current character position in p
  var pos;
  // the partial path so far, including a trailing slash if any
  var current;
  // the partial path without a trailing slash (except when pointing at a root)
  var base;
  // the partial path scanned in the previous round, with slash
  var previous;

  start();

  function start() {
    // Skip over roots
    var m = splitRootRe.exec(p);
    pos = m[0].length;
    current = m[0];
    base = m[0];
    previous = '';

    // On windows, check that the root exists. On unix there is no need.
    if (isWindows && !knownHard[base]) {
      fs.lstatSync(base);
      knownHard[base] = true;
    }
  }

  // walk down the path, swapping out linked pathparts for their real
  // values
  // NB: p.length changes.
  while (pos < p.length) {
    // find the next part
    nextPartRe.lastIndex = pos;
    var result = nextPartRe.exec(p);
    previous = current;
    current += result[0];
    base = previous + result[1];
    pos = nextPartRe.lastIndex;

    // continue if not a symlink
    if (knownHard[base] || (cache && cache.get(base) === base)) {
      continue;
    }

    var resolvedLink;
    const maybeCachedResolved = cache && cache.get(base);
    if (maybeCachedResolved) {
      resolvedLink = maybeCachedResolved;
    } else {
      var stat = fs.lstatSync(base);
      if (!stat.isSymbolicLink()) {
        knownHard[base] = true;
        if (cache) cache.set(base, base);
        continue;
      }

      // read the link if it wasn't read before
      // dev/ino always return 0 on windows, so skip the check.
      let linkTarget = null;
      let id;
      if (!isWindows) {
        id = '${stat.dev.toString(32)}:${stat.ino.toString(32)}';
        if (seenLinks.hasOwnProperty(id)) {
          linkTarget = seenLinks[id];
        }
      }
      if (linkTarget === null) {
        fs.statSync(base);
        linkTarget = fs.readlinkSync(base);
      }
      resolvedLink = pathModule.resolve(previous, linkTarget);

      if (cache) cache.set(base, resolvedLink);
      if (!isWindows) seenLinks[id] = linkTarget;
    }

    // resolve the link, then start over
    p = pathModule.resolve(resolvedLink, p.slice(pos));
    start();
  }

  if (cache) cache.set(original, p);
  return encodeRealpathResult(p, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.remove"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>remove (dir, callback)](#apidoc.element.fs-extra.remove)
- description and source-code
```javascript
function remove(dir, callback) {
  const options = {disableGlob: true}
  return callback ? rimraf(dir, options, callback) : rimraf(dir, options, function () {})
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.removeSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>removeSync (dir)](#apidoc.element.fs-extra.removeSync)
- description and source-code
```javascript
function removeSync(dir) {
  return rimraf.sync(dir, {disableGlob: true})
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.rename"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>rename (oldPath, newPath, callback)](#apidoc.element.fs-extra.rename)
- description and source-code
```javascript
rename = function (oldPath, newPath, callback) {
  callback = makeCallback(callback);
  if (handleError((oldPath = getPathFromURL(oldPath)), callback))
    return;

  if (handleError((newPath = getPathFromURL(newPath)), callback))
    return;

  if (!nullCheck(oldPath, callback)) return;
  if (!nullCheck(newPath, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rename(pathModule._makeLong(oldPath),
                 pathModule._makeLong(newPath),
                 req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.renameSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>renameSync (oldPath, newPath)](#apidoc.element.fs-extra.renameSync)
- description and source-code
```javascript
renameSync = function (oldPath, newPath) {
  handleError((oldPath = getPathFromURL(oldPath)));
  handleError((newPath = getPathFromURL(newPath)));
  nullCheck(oldPath);
  nullCheck(newPath);
  return binding.rename(pathModule._makeLong(oldPath),
                        pathModule._makeLong(newPath));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.rmdir"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>rmdir (path, callback)](#apidoc.element.fs-extra.rmdir)
- description and source-code
```javascript
rmdir = function (path, callback) {
  callback = maybeCallback(callback);
  if (handleError((path = getPathFromURL(path)), callback))
    return;
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rmdir(pathModule._makeLong(path), req);
}
```
- example usage
```shell
...
* https://github.com/jprichardson/node-fs-extra/issues/2
* https://github.com/flatiron/utile/issues/11
* https://github.com/ryanmcgrath/wrench-js/issues/29
* https://github.com/substack/node-mkdirp/issues/17

First, I believe that in as many cases as possible, the [Node.js naming schemes](http://nodejs.org/api/fs.html) should be chosen
. However, there are problems with the Node.js own naming schemes.

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.
...
```

#### <a name="apidoc.element.fs-extra.rmdirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>rmdirSync (path)](#apidoc.element.fs-extra.rmdirSync)
- description and source-code
```javascript
rmdirSync = function (path) {
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.rmdir(pathModule._makeLong(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.stat"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>stat (target, cb)](#apidoc.element.fs-extra.stat)
- description and source-code
```javascript
stat = function (target, cb) {
  return orig.call(fs, target, function (er, stats) {
    if (!stats) return cb.apply(this, arguments)
    if (stats.uid < 0) stats.uid += 0x100000000
    if (stats.gid < 0) stats.gid += 0x100000000
    if (cb) cb.apply(this, arguments)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.statSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>statSync (target)](#apidoc.element.fs-extra.statSync)
- description and source-code
```javascript
statSync = function (target) {
  var stats = orig.call(fs, target)
  if (stats.uid < 0) stats.uid += 0x100000000
  if (stats.gid < 0) stats.gid += 0x100000000
  return stats;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.symlink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>symlink (target, path, type_, callback_)](#apidoc.element.fs-extra.symlink)
- description and source-code
```javascript
symlink = function (target, path, type_, callback_) {
  var type = (typeof type_ === 'string' ? type_ : null);
  var callback = makeCallback(arguments[arguments.length - 1]);

  if (handleError((target = getPathFromURL(target)), callback))
    return;

  if (handleError((path = getPathFromURL(path)), callback))
    return;

  if (!nullCheck(target, callback)) return;
  if (!nullCheck(path, callback)) return;

  var req = new FSReqWrap();
  req.oncomplete = callback;

  binding.symlink(preprocessSymlinkDestination(target, type, path),
                  pathModule._makeLong(path),
                  type,
                  req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.symlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>symlinkSync (target, path, type)](#apidoc.element.fs-extra.symlinkSync)
- description and source-code
```javascript
symlinkSync = function (target, path, type) {
  type = (typeof type === 'string' ? type : null);
  handleError((target = getPathFromURL(target)));
  handleError((path = getPathFromURL(path)));
  nullCheck(target);
  nullCheck(path);

  return binding.symlink(preprocessSymlinkDestination(target, type, path),
                         pathModule._makeLong(path),
                         type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.truncate"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>truncate (path, len, callback)](#apidoc.element.fs-extra.truncate)
- description and source-code
```javascript
truncate = function (path, len, callback) {
  if (typeof path === 'number') {
    return fs.ftruncate(path, len, callback);
  }
  if (typeof len === 'function') {
    callback = len;
    len = 0;
  } else if (len === undefined) {
    len = 0;
  }

  callback = maybeCallback(callback);
  fs.open(path, 'r+', function(er, fd) {
    if (er) return callback(er);
    var req = new FSReqWrap();
    req.oncomplete = function oncomplete(er) {
      fs.close(fd, function(er2) {
        callback(er || er2);
      });
    };
    binding.ftruncate(fd, len, req);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.truncateSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>truncateSync (path, len)](#apidoc.element.fs-extra.truncateSync)
- description and source-code
```javascript
truncateSync = function (path, len) {
  if (typeof path === 'number') {
    // legacy
    return fs.ftruncateSync(path, len);
  }
  if (len === undefined) {
    len = 0;
  }
  // allow error to be thrown, but still close fd.
  var fd = fs.openSync(path, 'r+');
  var ret;

  try {
    ret = fs.ftruncateSync(fd, len);
  } finally {
    fs.closeSync(fd);
  }
  return ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.unlink"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>unlink (path, callback)](#apidoc.element.fs-extra.unlink)
- description and source-code
```javascript
unlink = function (path, callback) {
  callback = makeCallback(callback);
  if (handleError((path = getPathFromURL(path)), callback))
    return;
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.unlink(pathModule._makeLong(path), req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.unlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>unlinkSync (path)](#apidoc.element.fs-extra.unlinkSync)
- description and source-code
```javascript
unlinkSync = function (path) {
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  return binding.unlink(pathModule._makeLong(path));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.unwatchFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>unwatchFile (filename, listener)](#apidoc.element.fs-extra.unwatchFile)
- description and source-code
```javascript
unwatchFile = function (filename, listener) {
  handleError((filename = getPathFromURL(filename)));
  nullCheck(filename);
  filename = pathModule.resolve(filename);
  var stat = statWatchers.get(filename);

  if (stat === undefined) return;

  if (typeof listener === 'function') {
    stat.removeListener('change', listener);
  } else {
    stat.removeAllListeners('change');
  }

  if (stat.listenerCount('change') === 0) {
    stat.stop();
    statWatchers.delete(filename);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.utimes"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>utimes (path, atime, mtime, callback)](#apidoc.element.fs-extra.utimes)
- description and source-code
```javascript
utimes = function (path, atime, mtime, callback) {
  callback = makeCallback(callback);
  if (handleError((path = getPathFromURL(path)), callback))
    return;
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.utimes(pathModule._makeLong(path),
                 toUnixTimestamp(atime),
                 toUnixTimestamp(mtime),
                 req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.utimesSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>utimesSync (path, atime, mtime)](#apidoc.element.fs-extra.utimesSync)
- description and source-code
```javascript
utimesSync = function (path, atime, mtime) {
  handleError((path = getPathFromURL(path)));
  nullCheck(path);
  atime = toUnixTimestamp(atime);
  mtime = toUnixTimestamp(mtime);
  binding.utimes(pathModule._makeLong(path), atime, mtime);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.watch"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>watch (filename, options, listener)](#apidoc.element.fs-extra.watch)
- description and source-code
```javascript
watch = function (filename, options, listener) {
  handleError((filename = getPathFromURL(filename)));
  nullCheck(filename);

  if (typeof options === 'function') {
    listener = options;
  }
  options = getOptions(options, {});

  // Don't make changes directly on options object
  options = copyObject(options);

  if (options.persistent === undefined) options.persistent = true;
  if (options.recursive === undefined) options.recursive = false;

  const watcher = new FSWatcher();
  watcher.start(filename,
                options.persistent,
                options.recursive,
                options.encoding);

  if (listener) {
    watcher.addListener('change', listener);
  }

  return watcher;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.watchFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>watchFile (filename, options, listener)](#apidoc.element.fs-extra.watchFile)
- description and source-code
```javascript
watchFile = function (filename, options, listener) {
  handleError((filename = getPathFromURL(filename)));
  nullCheck(filename);
  filename = pathModule.resolve(filename);
  var stat;

  var defaults = {
    // Poll interval in milliseconds. 5007 is what libev used to use. It's
    // a little on the slow side but let's stick with it for now to keep
    // behavioral changes to a minimum.
    interval: 5007,
    persistent: true
  };

  if (options !== null && typeof options === 'object') {
    options = util._extend(defaults, options);
  } else {
    listener = options;
    options = defaults;
  }

  if (typeof listener !== 'function') {
    throw new Error('"watchFile()" requires a listener function');
  }

  stat = statWatchers.get(filename);

  if (stat === undefined) {
    stat = new StatWatcher();
    stat.start(filename, options.persistent, options.interval);
    statWatchers.set(filename, stat);
  }

  stat.addListener('change', listener);
  return stat;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.write"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>write (fd, buffer, offset, length, position, callback)](#apidoc.element.fs-extra.write)
- description and source-code
```javascript
write = function (fd, buffer, offset, length, position, callback) {
  function wrapper(err, written) {
    // Retain a reference to buffer so that it can't be GC'ed too soon.
    callback(err, written || 0, buffer);
  }

  var req = new FSReqWrap();
  req.oncomplete = wrapper;

  if (isUint8Array(buffer)) {
    callback = maybeCallback(callback || position || length || offset);
    if (typeof offset !== 'number') {
      offset = 0;
    }
    if (typeof length !== 'number') {
      length = buffer.length - offset;
    }
    if (typeof position !== 'number') {
      position = null;
    }
    return binding.writeBuffer(fd, buffer, offset, length, position, req);
  }

  if (typeof buffer !== 'string')
    buffer += '';
  if (typeof position !== 'function') {
    if (typeof offset === 'function') {
      position = offset;
      offset = null;
    } else {
      position = length;
    }
    length = 'utf8';
  }
  callback = maybeCallback(position);
  return binding.writeString(fd, buffer, offset, length, req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeFile"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeFile (path, data, options, cb)](#apidoc.element.fs-extra.writeFile)
- description and source-code
```javascript
function writeFile(path, data, options, cb) {
  if (typeof options === 'function')
    cb = options, options = null

  return go$writeFile(path, data, options, cb)

  function go$writeFile (path, data, options, cb) {
    return fs$writeFile(path, data, options, function (err) {
      if (err && (err.code === 'EMFILE' || err.code === 'ENFILE'))
        enqueue([go$writeFile, [path, data, options, cb]])
      else {
        if (typeof cb === 'function')
          cb.apply(this, arguments)
        retry()
      }
    })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeFileSync (path, data, options)](#apidoc.element.fs-extra.writeFileSync)
- description and source-code
```javascript
writeFileSync = function (path, data, options) {
  options = getOptions(options, { encoding: 'utf8', mode: 0o666, flag: 'w' });
  const flag = options.flag || 'w';

  var isUserFd = isFd(path); // file descriptor ownership
  var fd = isUserFd ? path : fs.openSync(path, flag, options.mode);

  if (!isUint8Array(data)) {
    data = Buffer.from('' + data, options.encoding || 'utf8');
  }
  var offset = 0;
  var length = data.length;
  var position = /a/.test(flag) ? null : 0;
  try {
    while (length > 0) {
      var written = fs.writeSync(fd, data, offset, length, position);
      offset += written;
      length -= written;
      if (position !== null) {
        position += written;
      }
    }
  } finally {
    if (!isUserFd) fs.closeSync(fd);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeJSON (file, obj, options, callback)](#apidoc.element.fs-extra.writeJSON)
- description and source-code
```javascript
function writeFile(file, obj, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = ''
  try {
    str = JSON.stringify(obj, options ? options.replacer : null, spaces) + '\n'
  } catch (err) {
    if (callback) return callback(err, null)
  }

  fs.writeFile(file, str, options, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeJSONSync (file, obj, options)](#apidoc.element.fs-extra.writeJSONSync)
- description and source-code
```javascript
function writeFileSync(file, obj, options) {
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = JSON.stringify(obj, options.replacer, spaces) + '\n'
  // not sure if fs.writeFileSync returns anything, but just in case
  return fs.writeFileSync(file, str, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeJson"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeJson (file, obj, options, callback)](#apidoc.element.fs-extra.writeJson)
- description and source-code
```javascript
function writeFile(file, obj, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = ''
  try {
    str = JSON.stringify(obj, options ? options.replacer : null, spaces) + '\n'
  } catch (err) {
    if (callback) return callback(err, null)
  }

  fs.writeFile(file, str, options, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeJsonSync (file, obj, options)](#apidoc.element.fs-extra.writeJsonSync)
- description and source-code
```javascript
function writeFileSync(file, obj, options) {
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = JSON.stringify(obj, options.replacer, spaces) + '\n'
  // not sure if fs.writeFileSync returns anything, but just in case
  return fs.writeFileSync(file, str, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.writeSync"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>writeSync (fd, buffer, offset, length, position)](#apidoc.element.fs-extra.writeSync)
- description and source-code
```javascript
writeSync = function (fd, buffer, offset, length, position) {
  if (isUint8Array(buffer)) {
    if (position === undefined)
      position = null;
    if (typeof offset !== 'number')
      offset = 0;
    if (typeof length !== 'number')
      length = buffer.length - offset;
    return binding.writeBuffer(fd, buffer, offset, length, position);
  }
  if (typeof buffer !== 'string')
    buffer += '';
  if (offset === undefined)
    offset = null;
  return binding.writeString(fd, buffer, offset, length, position);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.ReadStream"></a>[module fs-extra.ReadStream](#apidoc.module.fs-extra.ReadStream)

#### <a name="apidoc.element.fs-extra.ReadStream.ReadStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>ReadStream (path, options)](#apidoc.element.fs-extra.ReadStream.ReadStream)
- description and source-code
```javascript
function ReadStream(path, options) {
  if (this instanceof ReadStream)
    return fs$ReadStream.apply(this, arguments), this
  else
    return ReadStream.apply(Object.create(ReadStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.ReadStream.prototype"></a>[module fs-extra.ReadStream.prototype](#apidoc.module.fs-extra.ReadStream.prototype)

#### <a name="apidoc.element.fs-extra.ReadStream.prototype.open"></a>[function <span class="apidocSignatureSpan">fs-extra.ReadStream.prototype.</span>open ()](#apidoc.element.fs-extra.ReadStream.prototype.open)
- description and source-code
```javascript
function ReadStream$open() {
  var that = this
  open(that.path, that.flags, that.mode, function (err, fd) {
    if (err) {
      if (that.autoClose)
        that.destroy()

      that.emit('error', err)
    } else {
      that.fd = fd
      that.emit('open', fd)
      that.read()
    }
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.Stats"></a>[module fs-extra.Stats](#apidoc.module.fs-extra.Stats)

#### <a name="apidoc.element.fs-extra.Stats.Stats"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>Stats ( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec)](#apidoc.element.fs-extra.Stats.Stats)
- description and source-code
```javascript
function Stats( dev, mode, nlink, uid, gid, rdev, blksize, ino, size, blocks, atim_msec, mtim_msec, ctim_msec, birthtim_msec) {
  this.dev = dev;
  this.mode = mode;
  this.nlink = nlink;
  this.uid = uid;
  this.gid = gid;
  this.rdev = rdev;
  this.blksize = blksize;
  this.ino = ino;
  this.size = size;
  this.blocks = blocks;
  this.atime = new Date(atim_msec);
  this.mtime = new Date(mtim_msec);
  this.ctime = new Date(ctim_msec);
  this.birthtime = new Date(birthtim_msec);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.Stats.prototype"></a>[module fs-extra.Stats.prototype](#apidoc.module.fs-extra.Stats.prototype)

#### <a name="apidoc.element.fs-extra.Stats.prototype._checkModeProperty"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>_checkModeProperty (property)](#apidoc.element.fs-extra.Stats.prototype._checkModeProperty)
- description and source-code
```javascript
_checkModeProperty = function (property) {
  return ((this.mode & constants.S_IFMT) === property);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isBlockDevice"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isBlockDevice ()](#apidoc.element.fs-extra.Stats.prototype.isBlockDevice)
- description and source-code
```javascript
isBlockDevice = function () {
  return this._checkModeProperty(constants.S_IFBLK);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isCharacterDevice"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isCharacterDevice ()](#apidoc.element.fs-extra.Stats.prototype.isCharacterDevice)
- description and source-code
```javascript
isCharacterDevice = function () {
  return this._checkModeProperty(constants.S_IFCHR);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isDirectory"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isDirectory ()](#apidoc.element.fs-extra.Stats.prototype.isDirectory)
- description and source-code
```javascript
isDirectory = function () {
  return this._checkModeProperty(constants.S_IFDIR);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isFIFO"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isFIFO ()](#apidoc.element.fs-extra.Stats.prototype.isFIFO)
- description and source-code
```javascript
isFIFO = function () {
  return this._checkModeProperty(constants.S_IFIFO);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isFile"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isFile ()](#apidoc.element.fs-extra.Stats.prototype.isFile)
- description and source-code
```javascript
isFile = function () {
  return this._checkModeProperty(constants.S_IFREG);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isSocket"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isSocket ()](#apidoc.element.fs-extra.Stats.prototype.isSocket)
- description and source-code
```javascript
isSocket = function () {
  return this._checkModeProperty(constants.S_IFSOCK);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.Stats.prototype.isSymbolicLink"></a>[function <span class="apidocSignatureSpan">fs-extra.Stats.prototype.</span>isSymbolicLink ()](#apidoc.element.fs-extra.Stats.prototype.isSymbolicLink)
- description and source-code
```javascript
isSymbolicLink = function () {
  return this._checkModeProperty(constants.S_IFLNK);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.WriteStream"></a>[module fs-extra.WriteStream](#apidoc.module.fs-extra.WriteStream)

#### <a name="apidoc.element.fs-extra.WriteStream.WriteStream"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>WriteStream (path, options)](#apidoc.element.fs-extra.WriteStream.WriteStream)
- description and source-code
```javascript
function WriteStream(path, options) {
  if (this instanceof WriteStream)
    return fs$WriteStream.apply(this, arguments), this
  else
    return WriteStream.apply(Object.create(WriteStream.prototype), arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.WriteStream.prototype"></a>[module fs-extra.WriteStream.prototype](#apidoc.module.fs-extra.WriteStream.prototype)

#### <a name="apidoc.element.fs-extra.WriteStream.prototype.open"></a>[function <span class="apidocSignatureSpan">fs-extra.WriteStream.prototype.</span>open ()](#apidoc.element.fs-extra.WriteStream.prototype.open)
- description and source-code
```javascript
function WriteStream$open() {
  var that = this
  open(that.path, that.flags, that.mode, function (err, fd) {
    if (err) {
      that.destroy()
      that.emit('error', err)
    } else {
      that.fd = fd
      that.emit('open', fd)
    }
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.copy"></a>[module fs-extra.copy](#apidoc.module.fs-extra.copy)

#### <a name="apidoc.element.fs-extra.copy.copy"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>copy (src, dest, options, callback)](#apidoc.element.fs-extra.copy.copy)
- description and source-code
```javascript
function copy(src, dest, options, callback) {
  if (typeof options === 'function' && !callback) {
    callback = options
    options = {}
  } else if (typeof options === 'function' || options instanceof RegExp) {
    options = {filter: options}
  }
  callback = callback || function () {}
  options = options || {}

  // Warn about using preserveTimestamps on 32-bit node:
  if (options.preserveTimestamps && process.arch === 'ia32') {
    console.warn('fs-extra: Using the preserveTimestamps option in 32-bit node is not recommended;\n
    see https://github.com/jprichardson/node-fs-extra/issues/269')
  }

  // don't allow src and dest to be the same
  const basePath = process.cwd()
  const currentPath = path.resolve(basePath, src)
  const targetPath = path.resolve(basePath, dest)
  if (currentPath === targetPath) return callback(new Error('Source and destination must not be the same.'))

  fs.lstat(src, (err, stats) => {
    if (err) return callback(err)

    let dir = null
    if (stats.isDirectory()) {
      const parts = dest.split(path.sep)
      parts.pop()
      dir = parts.join(path.sep)
    } else {
      dir = path.dirname(dest)
    }

    fs.exists(dir, dirExists => {
      if (dirExists) return ncp(src, dest, options, callback)
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        ncp(src, dest, options, callback)
      })
    })
  })
}
```
- example usage
```shell
...
Sync methods on the other hand will throw if an error occurs.

Example:

'''js
const fs = require('fs-extra')

fs.copy('/tmp/myfile', '/tmp/mynewfile', err => {
if (err) return console.error(err)
console.log("success!")
});

try {
fs.copySync('/tmp/myfile', '/tmp/mynewfile')
console.log("success!")
...
```



# <a name="apidoc.module.fs-extra.copy_sync"></a>[module fs-extra.copy_sync](#apidoc.module.fs-extra.copy_sync)

#### <a name="apidoc.element.fs-extra.copy_sync.copySync"></a>[function <span class="apidocSignatureSpan">fs-extra.copy_sync.</span>copySync (src, dest, options)](#apidoc.element.fs-extra.copy_sync.copySync)
- description and source-code
```javascript
function copySync(src, dest, options) {
  if (typeof options === 'function' || options instanceof RegExp) {
    options = {filter: options}
  }

  options = options || {}
  options.recursive = !!options.recursive

  // default to true for now
  options.clobber = 'clobber' in options ? !!options.clobber : true
  // overwrite falls back to clobber
  options.overwrite = 'overwrite' in options ? !!options.overwrite : options.clobber
  options.dereference = 'dereference' in options ? !!options.dereference : false
  options.preserveTimestamps = 'preserveTimestamps' in options ? !!options.preserveTimestamps : false

  options.filter = options.filter || function () { return true }

  // Warn about using preserveTimestamps on 32-bit node:
  if (options.preserveTimestamps && process.arch === 'ia32') {
    console.warn('fs-extra: Using the preserveTimestamps option in 32-bit node is not recommended;\n
    see https://github.com/jprichardson/node-fs-extra/issues/269')
  }

  const stats = (options.recursive && !options.dereference) ? fs.lstatSync(src) : fs.statSync(src)
  const destFolder = path.dirname(dest)
  const destFolderExists = fs.existsSync(destFolder)
  let performCopy = false

  if (options.filter instanceof RegExp) {
    console.warn('Warning: fs-extra: Passing a RegExp filter is deprecated, use a function')
    performCopy = options.filter.test(src)
  } else if (typeof options.filter === 'function') performCopy = options.filter(src, dest)

  if (stats.isFile() && performCopy) {
    if (!destFolderExists) mkdir.mkdirsSync(destFolder)
    copyFileSync(src, dest, {
      overwrite: options.overwrite,
      errorOnExist: options.errorOnExist,
      preserveTimestamps: options.preserveTimestamps
    })
  } else if (stats.isDirectory() && performCopy) {
    if (!fs.existsSync(dest)) mkdir.mkdirsSync(dest)
    const contents = fs.readdirSync(src)
    contents.forEach(content => {
      const opts = options
      opts.recursive = true
      copySync(path.join(src, content), path.join(dest, content), opts)
    })
  } else if (options.recursive && stats.isSymbolicLink() && performCopy) {
    const srcPath = fs.readlinkSync(src)
    fs.symlinkSync(srcPath, dest)
  }
}
```
- example usage
```shell
...

fs.copy('/tmp/myfile', '/tmp/mynewfile', err => {
  if (err) return console.error(err)
  console.log("success!")
});

try {
  fs.copySync('/tmp/myfile', '/tmp/mynewfile')
  console.log("success!")
} catch (err) {
  console.error(err)
}
'''
...
```



# <a name="apidoc.module.fs-extra.empty"></a>[module fs-extra.empty](#apidoc.module.fs-extra.empty)

#### <a name="apidoc.element.fs-extra.empty.emptyDir"></a>[function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptyDir (dir, callback)](#apidoc.element.fs-extra.empty.emptyDir)
- description and source-code
```javascript
function emptyDir(dir, callback) {
  callback = callback || function () {}
  fs.readdir(dir, (err, items) => {
    if (err) return mkdir.mkdirs(dir, callback)

    items = items.map(item => path.join(dir, item))

    deleteItem()

    function deleteItem () {
      const item = items.pop()
      if (!item) return callback()
      remove.remove(item, err => {
        if (err) return callback(err)
        deleteItem()
      })
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.empty.emptyDirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptyDirSync (dir)](#apidoc.element.fs-extra.empty.emptyDirSync)
- description and source-code
```javascript
function emptyDirSync(dir) {
  let items
  try {
    items = fs.readdirSync(dir)
  } catch (err) {
    return mkdir.mkdirsSync(dir)
  }

  items.forEach(item => {
    item = path.join(dir, item)
    remove.removeSync(item)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.empty.emptydir"></a>[function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptydir (dir, callback)](#apidoc.element.fs-extra.empty.emptydir)
- description and source-code
```javascript
function emptyDir(dir, callback) {
  callback = callback || function () {}
  fs.readdir(dir, (err, items) => {
    if (err) return mkdir.mkdirs(dir, callback)

    items = items.map(item => path.join(dir, item))

    deleteItem()

    function deleteItem () {
      const item = items.pop()
      if (!item) return callback()
      remove.remove(item, err => {
        if (err) return callback(err)
        deleteItem()
      })
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.empty.emptydirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.empty.</span>emptydirSync (dir)](#apidoc.element.fs-extra.empty.emptydirSync)
- description and source-code
```javascript
function emptyDirSync(dir) {
  let items
  try {
    items = fs.readdirSync(dir)
  } catch (err) {
    return mkdir.mkdirsSync(dir)
  }

  items.forEach(item => {
    item = path.join(dir, item)
    remove.removeSync(item)
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.ensure"></a>[module fs-extra.ensure](#apidoc.module.fs-extra.ensure)

#### <a name="apidoc.element.fs-extra.ensure.createFile"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createFile (file, callback)](#apidoc.element.fs-extra.ensure.createFile)
- description and source-code
```javascript
function createFile(file, callback) {
  function makeFile () {
    fs.writeFile(file, '', err => {
      if (err) return callback(err)
      callback()
    })
  }

  fs.exists(file, fileExists => {
    if (fileExists) return callback()
    const dir = path.dirname(file)
    fs.exists(dir, dirExists => {
      if (dirExists) return makeFile()
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        makeFile()
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.createFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createFileSync (file)](#apidoc.element.fs-extra.ensure.createFileSync)
- description and source-code
```javascript
function createFileSync(file) {
  if (fs.existsSync(file)) return

  const dir = path.dirname(file)
  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  fs.writeFileSync(file, '')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.createLink"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.createLink)
- description and source-code
```javascript
function createLink(srcpath, dstpath, callback) {
  function makeLink (srcpath, dstpath) {
    fs.link(srcpath, dstpath, err => {
      if (err) return callback(err)
      callback(null)
    })
  }

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    fs.lstat(srcpath, (err, stat) => {
      if (err) {
        err.message = err.message.replace('lstat', 'ensureLink')
        return callback(err)
      }

      const dir = path.dirname(dstpath)
      fs.exists(dir, dirExists => {
        if (dirExists) return makeLink(srcpath, dstpath)
        mkdir.mkdirs(dir, err => {
          if (err) return callback(err)
          makeLink(srcpath, dstpath)
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.createLinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.createLinkSync)
- description and source-code
```javascript
function createLinkSync(srcpath, dstpath, callback) {
  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  try {
    fs.lstatSync(srcpath)
  } catch (err) {
    err.message = err.message.replace('lstat', 'ensureLink')
    throw err
  }

  const dir = path.dirname(dstpath)
  const dirExists = fs.existsSync(dir)
  if (dirExists) return fs.linkSync(srcpath, dstpath)
  mkdir.mkdirsSync(dir)

  return fs.linkSync(srcpath, dstpath)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.createSymlink"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.createSymlink)
- description and source-code
```javascript
function createSymlink(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    symlinkPaths(srcpath, dstpath, (err, relative) => {
      if (err) return callback(err)
      srcpath = relative.toDst
      symlinkType(relative.toCwd, type, (err, type) => {
        if (err) return callback(err)
        const dir = path.dirname(dstpath)
        fs.exists(dir, dirExists => {
          if (dirExists) return fs.symlink(srcpath, dstpath, type, callback)
          mkdirs(dir, err => {
            if (err) return callback(err)
            fs.symlink(srcpath, dstpath, type, callback)
          })
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.createSymlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>createSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.createSymlinkSync)
- description and source-code
```javascript
function createSymlinkSync(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  const relative = symlinkPathsSync(srcpath, dstpath)
  srcpath = relative.toDst
  type = symlinkTypeSync(relative.toCwd, type)
  const dir = path.dirname(dstpath)
  const exists = fs.existsSync(dir)
  if (exists) return fs.symlinkSync(srcpath, dstpath, type)
  mkdirsSync(dir)
  return fs.symlinkSync(srcpath, dstpath, type)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureFile"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureFile (file, callback)](#apidoc.element.fs-extra.ensure.ensureFile)
- description and source-code
```javascript
function createFile(file, callback) {
  function makeFile () {
    fs.writeFile(file, '', err => {
      if (err) return callback(err)
      callback()
    })
  }

  fs.exists(file, fileExists => {
    if (fileExists) return callback()
    const dir = path.dirname(file)
    fs.exists(dir, dirExists => {
      if (dirExists) return makeFile()
      mkdir.mkdirs(dir, err => {
        if (err) return callback(err)
        makeFile()
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureFileSync (file)](#apidoc.element.fs-extra.ensure.ensureFileSync)
- description and source-code
```javascript
function createFileSync(file) {
  if (fs.existsSync(file)) return

  const dir = path.dirname(file)
  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  fs.writeFileSync(file, '')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureLink"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureLink (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.ensureLink)
- description and source-code
```javascript
function createLink(srcpath, dstpath, callback) {
  function makeLink (srcpath, dstpath) {
    fs.link(srcpath, dstpath, err => {
      if (err) return callback(err)
      callback(null)
    })
  }

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    fs.lstat(srcpath, (err, stat) => {
      if (err) {
        err.message = err.message.replace('lstat', 'ensureLink')
        return callback(err)
      }

      const dir = path.dirname(dstpath)
      fs.exists(dir, dirExists => {
        if (dirExists) return makeLink(srcpath, dstpath)
        mkdir.mkdirs(dir, err => {
          if (err) return callback(err)
          makeLink(srcpath, dstpath)
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureLinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureLinkSync (srcpath, dstpath, callback)](#apidoc.element.fs-extra.ensure.ensureLinkSync)
- description and source-code
```javascript
function createLinkSync(srcpath, dstpath, callback) {
  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  try {
    fs.lstatSync(srcpath)
  } catch (err) {
    err.message = err.message.replace('lstat', 'ensureLink')
    throw err
  }

  const dir = path.dirname(dstpath)
  const dirExists = fs.existsSync(dir)
  if (dirExists) return fs.linkSync(srcpath, dstpath)
  mkdir.mkdirsSync(dir)

  return fs.linkSync(srcpath, dstpath)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureSymlink"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureSymlink (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.ensureSymlink)
- description and source-code
```javascript
function createSymlink(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  fs.exists(dstpath, destinationExists => {
    if (destinationExists) return callback(null)
    symlinkPaths(srcpath, dstpath, (err, relative) => {
      if (err) return callback(err)
      srcpath = relative.toDst
      symlinkType(relative.toCwd, type, (err, type) => {
        if (err) return callback(err)
        const dir = path.dirname(dstpath)
        fs.exists(dir, dirExists => {
          if (dirExists) return fs.symlink(srcpath, dstpath, type, callback)
          mkdirs(dir, err => {
            if (err) return callback(err)
            fs.symlink(srcpath, dstpath, type, callback)
          })
        })
      })
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.ensure.ensureSymlinkSync"></a>[function <span class="apidocSignatureSpan">fs-extra.ensure.</span>ensureSymlinkSync (srcpath, dstpath, type, callback)](#apidoc.element.fs-extra.ensure.ensureSymlinkSync)
- description and source-code
```javascript
function createSymlinkSync(srcpath, dstpath, type, callback) {
  callback = (typeof type === 'function') ? type : callback
  type = (typeof type === 'function') ? false : type

  const destinationExists = fs.existsSync(dstpath)
  if (destinationExists) return undefined

  const relative = symlinkPathsSync(srcpath, dstpath)
  srcpath = relative.toDst
  type = symlinkTypeSync(relative.toCwd, type)
  const dir = path.dirname(dstpath)
  const exists = fs.existsSync(dir)
  if (exists) return fs.symlinkSync(srcpath, dstpath, type)
  mkdirsSync(dir)
  return fs.symlinkSync(srcpath, dstpath, type)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.json"></a>[module fs-extra.json](#apidoc.module.fs-extra.json)

#### <a name="apidoc.element.fs-extra.json.outputJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJSON (file, data, options, callback)](#apidoc.element.fs-extra.json.outputJSON)
- description and source-code
```javascript
function outputJson(file, data, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const dir = path.dirname(file)

  fs.exists(dir, itDoes => {
    if (itDoes) return jsonFile.writeJson(file, data, options, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)
      jsonFile.writeJson(file, data, options, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.outputJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJSONSync (file, data, options)](#apidoc.element.fs-extra.json.outputJSONSync)
- description and source-code
```javascript
function outputJsonSync(file, data, options) {
  const dir = path.dirname(file)

  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  jsonFile.writeJsonSync(file, data, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.outputJson"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJson (file, data, options, callback)](#apidoc.element.fs-extra.json.outputJson)
- description and source-code
```javascript
function outputJson(file, data, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const dir = path.dirname(file)

  fs.exists(dir, itDoes => {
    if (itDoes) return jsonFile.writeJson(file, data, options, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)
      jsonFile.writeJson(file, data, options, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.outputJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>outputJsonSync (file, data, options)](#apidoc.element.fs-extra.json.outputJsonSync)
- description and source-code
```javascript
function outputJsonSync(file, data, options) {
  const dir = path.dirname(file)

  if (!fs.existsSync(dir)) {
    mkdir.mkdirsSync(dir)
  }

  jsonFile.writeJsonSync(file, data, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.readJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>readJSON (file, options, callback)](#apidoc.element.fs-extra.json.readJSON)
- description and source-code
```javascript
function readFile(file, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }

  if (typeof options === 'string') {
    options = {encoding: options}
  }

  options = options || {}
  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  fs.readFile(file, options, function (err, data) {
    if (err) return callback(err)

    data = stripBom(data)

    var obj
    try {
      obj = JSON.parse(data, options ? options.reviver : null)
    } catch (err2) {
      if (shouldThrow) {
        err2.message = file + ': ' + err2.message
        return callback(err2)
      } else {
        return callback(null, null)
      }
    }

    callback(null, obj)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.readJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>readJSONSync (file, options)](#apidoc.element.fs-extra.json.readJSONSync)
- description and source-code
```javascript
function readFileSync(file, options) {
  options = options || {}
  if (typeof options === 'string') {
    options = {encoding: options}
  }

  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  var content = fs.readFileSync(file, options)
  content = stripBom(content)

  try {
    return JSON.parse(content, options.reviver)
  } catch (err) {
    if (shouldThrow) {
      err.message = file + ': ' + err.message
      throw err
    } else {
      return null
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.readJson"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>readJson (file, options, callback)](#apidoc.element.fs-extra.json.readJson)
- description and source-code
```javascript
function readFile(file, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }

  if (typeof options === 'string') {
    options = {encoding: options}
  }

  options = options || {}
  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  fs.readFile(file, options, function (err, data) {
    if (err) return callback(err)

    data = stripBom(data)

    var obj
    try {
      obj = JSON.parse(data, options ? options.reviver : null)
    } catch (err2) {
      if (shouldThrow) {
        err2.message = file + ': ' + err2.message
        return callback(err2)
      } else {
        return callback(null, null)
      }
    }

    callback(null, obj)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.readJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>readJsonSync (file, options)](#apidoc.element.fs-extra.json.readJsonSync)
- description and source-code
```javascript
function readFileSync(file, options) {
  options = options || {}
  if (typeof options === 'string') {
    options = {encoding: options}
  }

  var fs = options.fs || _fs

  var shouldThrow = true
  // DO NOT USE 'passParsingErrors' THE NAME WILL CHANGE!!!, use 'throws' instead
  if ('passParsingErrors' in options) {
    shouldThrow = options.passParsingErrors
  } else if ('throws' in options) {
    shouldThrow = options.throws
  }

  var content = fs.readFileSync(file, options)
  content = stripBom(content)

  try {
    return JSON.parse(content, options.reviver)
  } catch (err) {
    if (shouldThrow) {
      err.message = file + ': ' + err.message
      throw err
    } else {
      return null
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.writeJSON"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJSON (file, obj, options, callback)](#apidoc.element.fs-extra.json.writeJSON)
- description and source-code
```javascript
function writeFile(file, obj, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = ''
  try {
    str = JSON.stringify(obj, options ? options.replacer : null, spaces) + '\n'
  } catch (err) {
    if (callback) return callback(err, null)
  }

  fs.writeFile(file, str, options, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.writeJSONSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJSONSync (file, obj, options)](#apidoc.element.fs-extra.json.writeJSONSync)
- description and source-code
```javascript
function writeFileSync(file, obj, options) {
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = JSON.stringify(obj, options.replacer, spaces) + '\n'
  // not sure if fs.writeFileSync returns anything, but just in case
  return fs.writeFileSync(file, str, options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.writeJson"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJson (file, obj, options, callback)](#apidoc.element.fs-extra.json.writeJson)
- description and source-code
```javascript
function writeFile(file, obj, options, callback) {
  if (callback == null) {
    callback = options
    options = {}
  }
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = ''
  try {
    str = JSON.stringify(obj, options ? options.replacer : null, spaces) + '\n'
  } catch (err) {
    if (callback) return callback(err, null)
  }

  fs.writeFile(file, str, options, callback)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.json.writeJsonSync"></a>[function <span class="apidocSignatureSpan">fs-extra.json.</span>writeJsonSync (file, obj, options)](#apidoc.element.fs-extra.json.writeJsonSync)
- description and source-code
```javascript
function writeFileSync(file, obj, options) {
  options = options || {}
  var fs = options.fs || _fs

  var spaces = typeof options === 'object' && options !== null
    ? 'spaces' in options
    ? options.spaces : this.spaces
    : this.spaces

  var str = JSON.stringify(obj, options.replacer, spaces) + '\n'
  // not sure if fs.writeFileSync returns anything, but just in case
  return fs.writeFileSync(file, str, options)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.mkdirs"></a>[module fs-extra.mkdirs](#apidoc.module.fs-extra.mkdirs)

#### <a name="apidoc.element.fs-extra.mkdirs.mkdirs"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>mkdirs (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.mkdirs)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.mkdirs.ensureDir"></a>[function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>ensureDir (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.ensureDir)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdirs.ensureDirSync"></a>[function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>ensureDirSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.ensureDirSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdirs.mkdirp"></a>[function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirp (p, opts, callback, made)](#apidoc.element.fs-extra.mkdirs.mkdirp)
- description and source-code
```javascript
function mkdirs(p, opts, callback, made) {
  if (typeof opts === 'function') {
    callback = opts
    opts = {}
  } else if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    return callback(errInval)
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  callback = callback || function () {}
  p = path.resolve(p)

  xfs.mkdir(p, mode, er => {
    if (!er) {
      made = made || p
      return callback(null, made)
    }
    switch (er.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) return callback(er)
        mkdirs(path.dirname(p), opts, (er, made) => {
          if (er) callback(er, made)
          else mkdirs(p, opts, callback, made)
        })
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        xfs.stat(p, (er2, stat) => {
          // if the stat fails, then that's super weird.
          // let the original error be the failure reason.
          if (er2 || !stat.isDirectory()) callback(er, made)
          else callback(null, made)
        })
        break
    }
  })
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.mkdirs.mkdirpSync"></a>[function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirpSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.mkdirpSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.mkdirs.mkdirsSync"></a>[function <span class="apidocSignatureSpan">fs-extra.mkdirs.</span>mkdirsSync (p, opts, made)](#apidoc.element.fs-extra.mkdirs.mkdirsSync)
- description and source-code
```javascript
function mkdirsSync(p, opts, made) {
  if (!opts || typeof opts !== 'object') {
    opts = { mode: opts }
  }

  let mode = opts.mode
  const xfs = opts.fs || fs

  if (process.platform === 'win32' && invalidWin32Path(p)) {
    const errInval = new Error(p + ' contains invalid WIN32 path characters.')
    errInval.code = 'EINVAL'
    throw errInval
  }

  if (mode === undefined) {
    mode = o777 & (~process.umask())
  }
  if (!made) made = null

  p = path.resolve(p)

  try {
    xfs.mkdirSync(p, mode)
    made = made || p
  } catch (err0) {
    switch (err0.code) {
      case 'ENOENT':
        if (path.dirname(p) === p) throw err0
        made = mkdirsSync(path.dirname(p), opts, made)
        mkdirsSync(p, opts, made)
        break

      // In the case of any other error, just see if there's a dir
      // there already.  If so, then hooray!  If not, then something
      // is borked.
      default:
        let stat
        try {
          stat = xfs.statSync(p)
        } catch (err1) {
          throw err0
        }
        if (!stat.isDirectory()) throw err0
        break
    }
  }

  return made
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.move"></a>[module fs-extra.move](#apidoc.module.fs-extra.move)

#### <a name="apidoc.element.fs-extra.move.move"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>move (source, dest, options, callback)](#apidoc.element.fs-extra.move.move)
- description and source-code
```javascript
function move(source, dest, options, callback) {
  if (typeof options === 'function') {
    callback = options
    options = {}
  }

  const shouldMkdirp = ('mkdirp' in options) ? options.mkdirp : true
  const overwrite = options.overwrite || options.clobber || false

  if (shouldMkdirp) {
    mkdirs()
  } else {
    doRename()
  }

  function mkdirs () {
    mkdirp(path.dirname(dest), err => {
      if (err) return callback(err)
      doRename()
    })
  }

  function doRename () {
    if (path.resolve(source) === path.resolve(dest)) {
      setImmediate(callback)
    } else if (overwrite) {
      fs.rename(source, dest, err => {
        if (!err) return callback()

        if (err.code === 'ENOTEMPTY' || err.code === 'EEXIST') {
          remove(dest, err => {
            if (err) return callback(err)
            options.overwrite = false // just overwriteed it, no need to do it again
            move(source, dest, options, callback)
          })
          return
        }

        // weird Windows shit
        if (err.code === 'EPERM') {
          setTimeout(() => {
            remove(dest, err => {
              if (err) return callback(err)
              options.overwrite = false
              move(source, dest, options, callback)
            })
          }, 200)
          return
        }

        if (err.code !== 'EXDEV') return callback(err)
        moveAcrossDevice(source, dest, overwrite, callback)
      })
    } else {
      fs.link(source, dest, err => {
        if (err) {
          if (err.code === 'EXDEV' || err.code === 'EISDIR' || err.code === 'EPERM' || err.code === 'ENOTSUP') {
            moveAcrossDevice(source, dest, overwrite, callback)
            return
          }
          callback(err)
          return
        }
        fs.unlink(source, callback)
      })
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.move_sync"></a>[module fs-extra.move_sync](#apidoc.module.fs-extra.move_sync)

#### <a name="apidoc.element.fs-extra.move_sync.moveSync"></a>[function <span class="apidocSignatureSpan">fs-extra.move_sync.</span>moveSync (src, dest, options)](#apidoc.element.fs-extra.move_sync.moveSync)
- description and source-code
```javascript
function moveSync(src, dest, options) {
  options = options || {}
  const overwrite = options.overwrite || options.clobber || false

  src = path.resolve(src)
  dest = path.resolve(dest)

  if (src === dest) return

  if (isSrcSubdir(src, dest)) throw new Error('Cannot move '${src}' into itself '${dest}'.')

  mkdirpSync(path.dirname(dest))
  tryRenameSync()

  function tryRenameSync () {
    if (overwrite) {
      try {
        return fs.renameSync(src, dest)
      } catch (err) {
        if (err.code === 'ENOTEMPTY' || err.code === 'EEXIST' || err.code === 'EPERM') {
          removeSync(dest)
          options.overwrite = false // just overwriteed it, no need to do it again
          return moveSync(src, dest, options)
        }

        if (err.code !== 'EXDEV') throw err
        return moveSyncAcrossDevice(src, dest, overwrite)
      }
    } else {
      try {
        fs.linkSync(src, dest)
        return fs.unlinkSync(src)
      } catch (err) {
        if (err.code === 'EXDEV' || err.code === 'EISDIR' || err.code === 'EPERM' || err.code === 'ENOTSUP') {
          return moveSyncAcrossDevice(src, dest, overwrite)
        }
        throw err
      }
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.output"></a>[module fs-extra.output](#apidoc.module.fs-extra.output)

#### <a name="apidoc.element.fs-extra.output.outputFile"></a>[function <span class="apidocSignatureSpan">fs-extra.output.</span>outputFile (file, data, encoding, callback)](#apidoc.element.fs-extra.output.outputFile)
- description and source-code
```javascript
function outputFile(file, data, encoding, callback) {
  if (typeof encoding === 'function') {
    callback = encoding
    encoding = 'utf8'
  }

  const dir = path.dirname(file)
  fs.exists(dir, itDoes => {
    if (itDoes) return fs.writeFile(file, data, encoding, callback)

    mkdir.mkdirs(dir, err => {
      if (err) return callback(err)

      fs.writeFile(file, data, encoding, callback)
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fs-extra.output.outputFileSync"></a>[function <span class="apidocSignatureSpan">fs-extra.output.</span>outputFileSync (file, data, encoding)](#apidoc.element.fs-extra.output.outputFileSync)
- description and source-code
```javascript
function outputFileSync(file, data, encoding) {
  const dir = path.dirname(file)
  if (fs.existsSync(dir)) {
    return fs.writeFileSync.apply(fs, arguments)
  }
  mkdir.mkdirsSync(dir)
  fs.writeFileSync.apply(fs, arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fs-extra.remove"></a>[module fs-extra.remove](#apidoc.module.fs-extra.remove)

#### <a name="apidoc.element.fs-extra.remove.remove"></a>[function <span class="apidocSignatureSpan">fs-extra.</span>remove (dir, callback)](#apidoc.element.fs-extra.remove.remove)
- description and source-code
```javascript
function remove(dir, callback) {
  const options = {disableGlob: true}
  return callback ? rimraf(dir, options, callback) : rimraf(dir, options, function () {})
}
```
- example usage
```shell
...

For example, 'fs.readFile()' and 'fs.readdir()': the **F** is capitalized in *File* and the **d** is not capitalized in *dir*. Perhaps
 a bit pedantic, but they should still be consistent. Also, Node.js has chosen a lot of POSIX naming schemes, which I believe is
 great. See: 'fs.mkdir()', 'fs.rmdir()', 'fs.chown()', etc.

We have a dilemma though. How do you consistently name methods that perform the following POSIX commands: 'cp', 'cp -r', 'mkdir -
p', and 'rm -rf'?

My perspective: when in doubt, err on the side of simplicity. A directory is just a hierarchical grouping of directories and files
. Consider that for a moment. So when you want to copy it or remove it, in most cases you'll want to copy or remove all of its contents
. When you want to create a directory, if the directory that it's suppose to be contained in does not exist, then in most cases
you'll want to create that too.

So, if you want to remove a file or a directory regardless of whether it has contents, just call 'fs.remove(path)'. If you want
to copy a file or a directory whether it has contents, just call 'fs.copy(source, destination)'. If you want to create a directory
 regardless of whether its parent directories exist, just call 'fs.mkdirs(path)' or 'fs.mkdirp(path)'.


Credit
------

'fs-extra' wouldn't be possible without using the modules from the following authors:
...
```

#### <a name="apidoc.element.fs-extra.remove.removeSync"></a>[function <span class="apidocSignatureSpan">fs-extra.remove.</span>removeSync (dir)](#apidoc.element.fs-extra.remove.removeSync)
- description and source-code
```javascript
function removeSync(dir) {
  return rimraf.sync(dir, {disableGlob: true})
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
