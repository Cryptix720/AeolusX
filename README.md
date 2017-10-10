<p align="center">
  <a href="https://github.com/Cryptix720">
    <img src="https://github.com/Cryptix720/aeolusx/blob/master/aeolusx.png" width=72 height=72>
  </a>

  <h1 align="center">Aeolusx</h1>


<h3>Build Status</h3>

<a>Aeolusx is a  web-site malware scanner inspired by the mortal son of Poseidon. The tool has been developed to help system administrators to find malware in websites without a need to install PHP on the server.</a>

<h3>
Installation:</h3>

Run command:  npm install -g aeolusx in your terminal

<h3>Usage:</h3>

aeolusx [options] [file/directory]

Options:

<ul>
<li>-h, --help - output usage information</li>
<li>-V, --version - output the version number</li>
<li>-v, --verbose - be verbose</li>
<li>-r, --recursive - scan directories recursively. All the subdirectories in the given directory will be scanned</li>
<li>-l, --log <file> - save scan report to #file.</li>
<li>--json - save scan report in JSON format.</li>
<li>--exclude <regex> - don't scan file names matching regular expression.</li>
<li>--exclude-dir <regex> - don't scan directory names matching regular expression.</li>
<li>--include <regex> - only scan file matching regular expression.</li>
<li>--include-dir <regex> - only scan directory matching regular expression.</li>
<li>--max-filesize <n> - scan files with size at most #n kilobytes (default: 100 MB)</li>
<li>-w, --whitelist <file> - use whitelist database to minimize false positive resultsv
<li>-p, --product <name> - provide product information added to the whitelist database</li>
<li>--update-whitelist - add files signatures to the whitelist database provided by --whitelist parameter</li>
</ul>

<h3>Examples:</h3>

Check all files in /var/www/htdocs folder.

$ aeolusx -r /var/www/htdocs

Check only JavaScript in /var/www/htdocs folder and show the list of all checked files.

$ aeolusx -r -v --include \.js$ /var/www/htdocs

Add WordPress to whitelist.

$ aeolusx --update-whitelist -w ./whitelist.sqlite -p "WordPress 4.3.1" ./temp/wordpress

Check all files in /var/www/htdocs folder using whitelist.

$ aeolusx -r -w ./whitelist.sqlite /var/www/htdocs

<h3><strong>Warning!</strong><h3>

<a>This tool does not have "auto-update function". Please make sure you have the latest NPM package installed.</a>
