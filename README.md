# pandoc-toc-sidebar
A [Pandoc](http://pandoc.org/) HTML template modified from Bootstrap [dashboard example](http://getbootstrap.com/examples/dashboard/).  
It has a navbar on the top of the page for website navigation, and a TOC (table of contents) on the sidebar for page navigaion, suitable for building website with Pandoc.

## Usage
1. Download the ZIP file then unzip it, or  
  ```sh
  git clone https://github.com/Mushiyo/pandoc-toc-sidebar.git
  ```
  
2. Put the file(s) which you want to convert into HTML with Pandoc into the `pandoc-toc-sidebar` folder.
  Then
  ```sh
  cd pandoc-toc-sidebar
  ```

3. Modify the `nav` file to fit your website structure.  
   The code in the `nav` file is a Bootstrape navbar.
  
4. Assume the file to convert is `input.md`, then the command will looks like
  ```sh
  pandoc input.md --template toc-sidebar.html --toc -B nav -o outWithTOC.html
  ```
  If you want to add TOC, then the command will looks like
  ```sh
  pandoc input.md --template toc-sidebar.html --toc -B nav -o outWithoutTOC.html
  ```
  You can remove `-B nav` in the previous commands if you do not want a navbar.
  However, for the time being, this will result in a not good looking layout :(

## Output example
The following output examples are converted from [Pandoc's README file](https://github.com/jgm/pandoc/blob/master/README)
* with TOC: <https://mushiyo.github.io/pandoc-toc-sidebar/outWithTOC.html>
* without TOC: <https://mushiyo.github.io/pandoc-toc-sidebar/outWithoutTOC.html>
