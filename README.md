# CSES-Solution-Extractor
A web scaper written in Python to extract accepted solutions on https://cses.fi
## Beautiful Soup
Beautiful Soup is a Python library for getting data out of HTML, XML, and other markup languages. Say you’ve found some webpages that display data relevant to your research, such as date or address information, but that do not provide any way of downloading the data directly. Beautiful Soup helps you pull particular content from a webpage, remove the HTML markup, and save the information. It is a tool for web scraping that helps you clean up and parse the documents you have pulled down from the web.
### Prerequisites
<ol>
<li>Installing Beautiful Soup is easiest if you have pip or another Python installer already in place.
  
```sh
pip install beautifulsoup4
```
You may need to preface this line with “sudo”, which gives your computer permission to write to your root directories and requires you to re-enter your password. This is the same logic behind you being prompted to enter your password when you install a new program.

With sudo, the command is:
```sh
sudo pip install beautifulsoup4
```
</li>
<li>
Additionally, you will need to install a “parser” for interpreting the HTML. To do so, run in the terminal:
  
```sh
pip install lxml
```
or

```sh
sudo pip install lxml
```
</li>

<li>
Finally, so that this code works with either Python2 or Python3, you will need one helper library. Run in the terminal:
  
```sh
pip install future
```
or
```sh
sudo pip install future
```  
</li>
</ol>

## Quick Revision/Explanation of code

<ul>
  
  ```sh
from bs4 install BeautifulSoup
with open('home.html','r') as html_file:
     content = html_file.read()
     soup = BeautifulSoup(content,'lxml')
     #print(soup.prettify())
     tags = soup.find_all('h5')
     print(tags)
```
  <li>Remember that BeautifulSoup installs in bs4 file hence we use "from bs4 import BeautifulSoup"</li>
  <li>"with open" enables us to read the contents of the file</li>
  <li>"read()" will read the file content</li>
  <li>"soup" is an instance of BeautifulSoup library with args as the file we want to scrape and the parser</li>
  <li>"prettify" method allows us to view the html file with indentations</li>
  <li>"find_all" is used because find will stop the execution after it finds the first h5. Output will be in the form of a list eg [< h5 >lorem ipsum</h5>,< h5 >lorem ipsum</h5></li>
