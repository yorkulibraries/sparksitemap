# sparksitemap

Make an [XML sitemap](http://www.sitemaps.org/protocol.html) for the SPARK web site (http://www.yorku.ca/spark/).

# Configuration

A few variables can be customized at the top of the script, but they shouldn't need changing.

# Usage

Move to the root directory of the SPARK content (where the home `index.html` file is, and directories such as `academic_integrity/`).  Then run

    $ /path/to/sparksitemap > sitemap.xml

Confirm that the result is valid by running

	$ xmllint --noout --schema http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd sitemap.xml

It should say

	sitemap.xml validates

## When to run the script

Run the script to update the sitemap whenever any SPARK files are updated.  Or run it from a cron job, with something like this, which would run it at 4 am on Tuesdays each week:

    0 4 * * 2 cd /var/www/spark/; /path/to/sparksitemap > sitemap.xml

Or run it by hand whenever the SPARK content is updated.

# License

The MIT License (MIT)

Copyright (c) 2013 William Denton

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

