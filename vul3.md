The environment can be downloaded at https://github.com/pluck-cms/pluck

The Stored XSS is found in the installation of PluckCMS.

The following page is displayed when the program is installed
http://127.0.0.1/CVE-Target/pluck/install.php
Click on Start the installation.
In step1, Click Proceed.
In step2, Feel free to fill in the blanks and click save.
In step3, and enter <script>alert('xss')</script> in the content and click save.



Then Click take a look at your website to trigger xss and it is a storage type.
