

Run `vagrant up` to spin up a MediaWiki installation at http://192.168.33.159 .

Note: This is for testing only, this is *not a secure installation*!

Testing mwclient:

```python
from mwclient import Site
site = Site('192.168.33.159', path='/')
site.login('MW-Test', 'mw_test')

site.upload(open('test.jpg', 'rb', 'test.jpg')

page = site.pages['Test']
page.save('[[File:Test.jpg|thumb]]')
```

(CC-0 test image from https://commons.wikimedia.org/wiki/File:Coach_accident_(3467942971).jpg, Llyfrgell Genedlaethol Cymru / The National Library of Wales from Wales)

to create http://192.168.33.159/index.php?title=Test
