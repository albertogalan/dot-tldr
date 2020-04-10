# scrapy

> Web-crawling framework.

- Create a project:

`scrapy startproject {{project_name}}`

- Create a spider (in project directory):

`scrapy genspider {{spider_name}} {{website_domain}}`

- Edit spider (in project directory):

`scrapy edit {{spider_name}}`

- Run spider (in project directory):

`scrapy crawl {{spider_name}}`

- Fetch a webpage as scrapy sees it and print source in stdout:

`scrapy fetch {{url}}`

- Open a webpage in the default browser as scrapy sees it (disable javascript for extra fidelity):

`scrapy view {{url}}`

- Open scrapy shell for url, which allows interaction with the page source in python shell (or ipython if available):

`scrapy shell {{url}}`
- Pausing and resuming crawls

`scrapy crawl somespider -s JOBDIR=crawls/somespider-1`


- Images and Pdf extraction spiders

`scrapy crawl pdf -L DEBUG --set JOBDIR=crawls/$f-01 -a domains=$f -a urls=http://$f --set FILES_STORE=../../data/files/$f --set LOG_FILE=logs/$f`
`scrapy crawl img -L DEBUG --set JOBDIR=crawls/$f-01 -a domains=$f -a urls=http://$f --set IMAGES_STORE=../../data/files/$f --set LOG_FILE=logs/$f`


- Company extract information spider

`scrapy crawl company -L DEBUG --set JOBDIR=crawls/$f-3 --set LOG_FILE=logs/$f -a urls=http://$f`
`scrapy crawl company -L DEBUG --set JOBDIR=crawls/$f-3 --set LOG_FILE=logs/$f -a urls=http://$f -t json -o result.json`


- create a new project

`scrapy startproject first_scrapy`


- create an spider

`scrapy genspider example example.com`


- download images

`scrapy crawl images2-splash -L ERROR -a url=$f -a tag=suit --set JOBDIR=data/crawl/{name}`


