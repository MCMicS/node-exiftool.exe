# exiftool.exe
Fork of [https://github.com/Sobesednik/exiftool.exe](https://github.com/Sobesednik/exiftool.exe)

A distribution of _exiftool.exe_. Current version is 12.24.

[![npm version](https://badge.fury.io/js/%40mcmics%2Fexiftool.exe.svg)](https://badge.fury.io/js/%40mcmics%2Fexiftool.exe)
[![Build status](https://ci.appveyor.com/api/projects/status/oge41bumo5xtou0p/branch/master?svg=true)](https://ci.appveyor.com/project/MCMicS/node-exiftool-exe/branch/master)

You might also be interested in [dist-exiftool](https://www.npmjs.com/package/@mcmics/dist-exiftool)
which will install an appropriate version of exiftool depending on the platform, and
[exiftool.pl](https://www.npmjs.com/package/@mcmics/exiftool.pl) for non-Windows platforms.

## Usage
The module exports a path to the exiftool Windows executable.

```js
const exec = require('child_process').execFile;
const exiftool = require('@mcmics/exiftool.exe');

execFile(exiftool, ['-j', 'image.jpg'], (error, stdout, stderr) => {
	if (error) {
		console.error(`exec error: ${error}`);
		return;
	}
	console.log(`stdout: ${stdout}`);
	console.log(`stderr: ${stderr}`);
});
```

## Links
[exiftool](http://www.sno.phy.queensu.ca/~phil/exiftool/)

[sourceforge](https://sourceforge.net/projects/exiftool/)

[cpan](http://search.cpan.org/~exiftool/)

## License
Artistic License 2.0
