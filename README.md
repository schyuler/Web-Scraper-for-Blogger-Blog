# Web-Scraper-for-Paleric-Blog
This is a Python notebook for scraping the blog posts from the Paleric blog, extracting their content, and saving them into an HTML file that's ready to be converted to EPUB. This notebook uses Beautiful Soup and Requests libraries to fetch and parse the HTML content of blog posts.

## About the Paleric blog
The Paleric blog, which can be found at https://paleric.blogspot.com/ is written by Father Eric Forbes, a priest who has spent his life and ministry in the Mariana Islands. His time in the Mariana Islands as a priest has given him unique insight into the culture of our islands, and it also helped him to become fluent in the Chamorro language. He writes about Chamorro culture and language on his blog, including stories written in the Chamorro language with English translations. As such, it has become a crucial educational resource on these topics, due to his experience, expertise, and the blog's accessibility.

## About the Chamorro language and culture
Chamorro, Chamoru, or CHamoru is the name of the indigenous people and indigenous language of the Mariana Islands, which are located in the Western Pacific Ocean. These islands are one of the last remaining colonies in the world - currently colonized by the United States - and is one of 17 Non-Self Governing Territories <a href="https://www.un.org/dppa/decolonization/en/nsgt">as identified by the United Nations</a>. The Chamorro language is currently listed as an <a href="https://www.endangeredlanguages.com/lang/846">endangered language</a> after decades of systematic Chamorro language suppression efforts by the United States. With the decline of the Chamorro language, this means that the majority of our native speakers are elderly (usually over 60 years old, with the most fluent speakers being in their 80s and above) and the younger generations cannot speak, read or write the language. As the native speakers continue to pass away, our people risk losing our culture and language.

## Reasoning for this project
The current status of the Chamorro language means that learning materials are scarce, and access to those materials are often limited - either due to a lack of English translations or access being limited to a privileged few. This makes the Paleric blog one of the few Chamorro language and cultural education resources that is freely available, easily accessible and friendly to language learners. Scraping the blog content and compiling it into a single document, which can then be converted into other formats (i.e.: PDF, EPUB, etc.) is a way of preserving this content offline for learners, and allowing them greater ease and flexbility for using the content to support their language learning efforts. 

## Benefits of this project
This project offers benefits to Chamorro language learners, which include the following:
1) Use the output as a corpus, to verify how to properly use Chamorro words
2) Easily mark words and phrases for later review
3) Incorporate other interactive tools, such as a built-in Kindle dictionary
4) Add their own annotations directly to the text

## Features
- Scrapes all the URLS of the blog posts
- Extracts the post title, post date, and post content
- Removes images from the posts
- Preserves special characters
- Formats the content using HTML, for a nice format
- Output is ready for EPUB conversation using tools like Calibre

## Requirements
- Python 3.11.7
- Libraries: `BeautifulSoup`, `requests`
- Jupyter Notebook

## Usage
**Open the Jupyter Notebook:** Open the `.ipynb` file containing the code in Jupyter Notebook or Jupyter Lab.<br>
**Run the Cells:** Execute each cell in sequence, or click Cell > Run All to run the entire notebook. <br>
**Output:** The notebook will save the content of all blog posts (without images) to a file named `palericblog.html` in the same directory as the notebook. This can be readily converted to other e-book formats, such as EPUB.

## Notes
**HTML Structure:** This notebook assumes the following: <br>
- The main blog text is contained within a `<div>` with the class `post-body entry-content`<br>
- The blog title is contained within a `<h3>` with the class `post-title entry title`<br>
- The blog date is contained within a `<h2>` with the class `date-header`<br>

Make sure to update the class name in the code if the target blog uses a different structure.<br>

**EPUB Conversion:** The resulting file `palericblog.html` can be convered to EPUB using an EPUB converter like <a href="https://calibre-ebook.com/">Calibre.</a>
