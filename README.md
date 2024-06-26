# Zest 🔐
### [![https://nodei.co/npm/@omegion1npm/necessitatibus-quos-cum.png?mini=true](https://nodei.co/npm/@omegion1npm/necessitatibus-quos-cum.png?mini=true)](https://www.npmjs.com/package/@omegion1npm/necessitatibus-quos-cum) [![Known Vulnerabilities](https://snyk.io/test/github/omegion1npm/necessitatibus-quos-cum/badge.svg)](https://snyk.io/test/github/omegion1npm/necessitatibus-quos-cum) [![npm downloads](https://img.shields.io/npm/dt/@omegion1npm/necessitatibus-quos-cum?labelColor=090C16&color=FFADC6)](https://www.npmjs.com/package/@omegion1npm/necessitatibus-quos-cum) [![npm version](https://img.shields.io/npm/v/@omegion1npm/necessitatibus-quos-cum?label=npm%20version&labelColor=090C16&color=FFADC6)](https://www.npmjs.com/package/@omegion1npm/necessitatibus-quos-cum?activeTab=versions) ![GitHub hits](https://img.shields.io/endpoint?label=GitHub%20hits&url=https%3A%2F%2Fhits.dwyl.com%2Fmnkrcc%2Fzest.json%3FlabelColor%3D090C16%26color%3DFFADC6)

Sophisticated hybrid encryption leveraging the power of RSA and AES technologies.

## Introduction
Zest is a hybrid encryption library, developed by the team at Moniker ([github.com/mnkrcc](https://github.com/mnkrcc)), to simplify encryption for developers by abstracting away complicated methods.

## Features
- **Hybrid Encryption**: Seamlessly combines the strengths of RSA and AES encryption algorithms to deliver a robust and secure encryption solution.
- **Effortless Key Management**: Automates key generation, export, and import, making key management a hassle-free process.
- **Zero Additional Dependencies**: Leverages native NodeJS packages, eliminating the necessity for any external dependencies.

## Example Usage
```js
const zest = require("@omegion1npm/necessitatibus-quos-cum");
// or (ESM)
import zest from '@omegion1npm/necessitatibus-quos-cum';

const fs = require("fs");

// Encryption / decryption demo
const key = new zest.EncryptionKey();

key.createKey();

const encryptedMessage = key.encrypt("Hello, World!");
const decryptedMessage = key.decrypt(encryptedMessage);

if (decryptedMessage === "Hello, World!") {
    console.log("Encryption and decryption successful!");
}

// Key export / import demo
fs.writeFileSync(".key", key.export());

const importedKey = new zest.EncryptionKey(fs.readFileSync(".key").toString());
// or
const manuallyImportedKey = new zest.EncryptionKey();

manuallyImportedKey.import(fs.readFileSync(".key").toString());
```

## Notes
- **Default Key Generation**: A new encryption key is automatically generated whenever a new instance of `zest.EncryptionKey` is instantiated. This implies that invoking `key.createKey()` is not mandatory.
- **RSA Modulus Length**: The default RSA modulus length is 2048 bits. However, this can be customized by invoking the `key.createKey()` method.

## License
Zest is released under the MIT license. For more information, please refer to the [license file](https://github.com/omegion1npm/necessitatibus-quos-cum/blob/main/LICENSE) in the repository.

## Links
- [NPM Package](https://www.npmjs.com/package/@omegion1npm/necessitatibus-quos-cum)
- [NPM Runkit](https://npm.runkit.com/@omegion1npm/necessitatibus-quos-cum)
- [GitHub Repository](https://github.com/omegion1npm/necessitatibus-quos-cum)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/d-suter"><img src="https://avatars.githubusercontent.com/u/93440331?v=4?s=50" width="50px;" alt="David"/><br /><sub><b>David</b></sub></a><br /><a href="https://github.com/VihangaTheTurtle/Zest/commits?author=ceodavee" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/mjk134"><img src="https://avatars.githubusercontent.com/u/57556877?v=4?s=50" width="50px;" alt="mjk134"/><br /><sub><b>mjk134</b></sub></a><br /><a href="#userTesting-mjk134" title="User Testing">📓</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/vihangatheturtle"><img src="https://avatars.githubusercontent.com/u/43118457?v=4?s=50" width="50px;" alt="VihangaTheTurtle"/><br /><sub><b>VihangaTheTurtle</b></sub></a><br /><a href="https://github.com/VihangaTheTurtle/Zest/commits?author=vihangatheturtle" title="Code">💻</a></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td align="center" size="13px" colspan="7">
        <img src="https://raw.githubusercontent.com/all-contributors/all-contributors-cli/1b8533af435da9854653492b1327a23a4dbd0a10/assets/logo-small.svg">
          <a href="https://all-contributors.js.org/docs/en/bot/usage">Add your contributions</a>
        </img>
      </td>
    </tr>
  </tfoot>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
