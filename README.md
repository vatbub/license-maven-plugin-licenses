# GNU General Public License v2.0 w/Classpath exception
The full license text for GNU General Public License v2.0 w/Classpath exception, with is used by OpneJDK. When using Maven and the license plugin, the url provided to the license text does not work to download said license. For this purpose this repository was created to just point to the license text file here and make it downloadable.

## Usage
When using the `Maven License Plugin` add this part inside the `<configuration>` tag:

```
<licenseUrlReplacement>
  <regexp>\Qhttps://openjdk.java.net/legal/gplv2+ce.html\E</regexp>
  <replacement>https://raw.githubusercontent.com/jonasNuber/gplv2-with-classpath-exception/main/GPLv2%20%2B%20Classpath%20Exception.txt</replacement>
</licenseUrlReplacement>
```
Where inside the `<regexp>` tag the initial url the license plugin tries to download the license from is situated (In this case the license url for Openjdk) and within the `<replacement>` tag, as the name suggesets, the replacement url (in this case the url to the file provided here).
