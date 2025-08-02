# Alternate License host for the license-maven-plugin

Some licenses just fail to download with the licenses-maven plugin for various reasons.
For this purpose, this repository was created to just point to the license text files here and make them downloadable.
This repo is based on [jonasNuber's upstream](https://github.com/jonasNuber/gplv2-with-classpath-exception) (thanks) and
extended with some more licenses.

| **License name**                                      | **Regex**                                                | **Replacement URL**                                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| GNU General Public License v2.0 w/Classpath exception | `\Qhttps://openjdk.java.net/legal/gplv2+ce.html\E`       | `https://raw.githubusercontent.com/vatbub/license-maven-plugin-licenses/main/GPLv2%20%2B%20Classpath%20Exception.txt` |
| LGPL 2.1                                              | `\Qhttps://www.gnu.org/licenses/old-licenses/lgpl-2.1\E` | `https://raw.githubusercontent.com/vatbub/license-maven-plugin-licenses/main/lgpl2-1.txt`                             |
| LGPL                                                  | `\Qhttp://www.gnu.org/licenses/lgpl.html\E`              | `https://raw.githubusercontent.com/vatbub/license-maven-plugin-licenses/main/lgpl.txt`                                |

## Usage

When using the `Maven License Plugin` add this part inside the `<configuration>` tag:

```
<licenseUrlReplacement>
  <regexp><!-- regex --></regexp>
  <replacement><!-- replacement URL --></replacement>
</licenseUrlReplacement>
```

Where inside the `<regexp>` tag the initial url the license plugin tries to download the license from is situated and
within the `<replacement>` tag, as the name suggesets, the replacement url.
