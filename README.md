# LinkedIn Job spider interview test

Set up intro

1. Unzip your code repository
2. `cd omni-crawler-test` on the host machine
2. `./setup.sh` to create, activate and configure a python virtualenv.
 - Read more at http://docs.python-guide.org/en/latest/dev/virtualenvs/.
 If you have any issues in installing python modules, you can use your own way to install.
 Troubleshoot all the way of installations and fix it up.
 hard_requirements.txt -> All neccessary python module listed. If any version conflicts, you can install latest version.
3. Run spider with `scrapy runspider lawjobsspider.py` or use crawl command

#==========
   GOAL:
#==========

Your goal for this test is to implement the logic for SimplyLawJobs.


1. You should navigate to the start_url, paginate through
    the search results pages and visit each job listed.
    For every job details page found, should produce a JobItem
    with the relevant fields populated.

2. You can use the Rule system for CrawSpider (the base class)
    or you can paginate in the "parse" method that is called
    after the first page of search results is loaded from the start_url.

3. There are some utilities above like "NormalizedJoin" and JobItemLoader
    to help making generating clean item data easier.


Once source code done, clean up source codes/remove unwanted lines. Remove all .pyc files from directory.

Create a zip of the source code and send it back to given email ID.

## Some helpful resources

1. CrawlSpider documentation
 - http://doc.scrapy.org/en/latest/topics/spiders.html#crawlspider
 - Example using Link extraction. http://doc.scrapy.org/en/latest/topics/spiders.html#crawlspider-example
2. ItemLoader documentation
 - http://doc.scrapy.org/en/latest/topics/loaders.html
 - ItemLoaders produce an Item after transforming through input and output processors
 since a single xpath expression may contain many elements transformation is useful for processes
 like stripping tags, joining text together and removing whitespace.
