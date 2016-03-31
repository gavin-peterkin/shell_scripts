3/31/16 Gavin Peterkin gavin-peterkin.github.io

Please see the sample urls and regexes.

When is the use of this script worthwhile?

When pulling the same data from sites that all have exactly the same or nearly the same layout. e.g. pulling dimensions from ~1,000 unique URLs would require a lot of (wo)manpower. By using this script that time is reduced to however long it takes to get the list of URL mappings (which can usually be done pretty quickly in Excel) and the time to write effective regular expressions.

What are the inputs?

The syntax is as follows: "regex-scraper" <file_containing_line_separated_url_mappings> <file_containing_line_separated_grep_expressions> <output_file=out if not specified>"

How to make this work on windows?

This will require the installation of CygWin on windows and packages for the curl and grep commands.

How to write the regular expressions?

This is the most time-consuming part. There are references online about how to formulate grep expressions. One should use the html, which can be accessed through firefox, and the "inspect element" tools in firefox to figure out how the data can be extracted through reg. exps. One also want to test the expressions on  afew htmls before throwing them into the script. If they don't work, you'll waste a lot of time.

Final steps?

Once you have the regular expressions and you think they work, test them on a few (~20) URLs and take a look at the output file ("out" by default). If it looks correct, great. Throw all the URLs at it and sit back.

Possible problems not relating to grep expressions?

Sometimes websites/servers have measures to prevent this kind of scraping. You can try changing the "User agent" option in the CURL command, but most likely that also won't work. A good rule of thumb is that big companies with large budgets that are worried about web security (big online retailers for example) will have tough security measures whereas little manufacturing companies don't really care or know about people scraping information about their products off of their sites.
