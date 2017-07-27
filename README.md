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
   The code in the `nav` file is a Bootstrap navbar.
  
4. Assume the file to convert is `input.md`, then the command will look like
  ```sh
  pandoc input.md --template toc-sidebar.html -B nav -o outWithoutTOC.html
  ```
  If you want to add TOC, then the command will look like
  ```sh
  pandoc input.md --template toc-sidebar.html --toc -B nav -o outWithTOC.html
  ```
  
### Options
#### Local or self-contained css and JavaScript files
For local css and JavaScript files, or using Pandoc's `--self-contained` option, replace `toc-sidebar.html` with `toc-sidebarL.html` in step 4.  

#### `<table>` styles
The `<table>` styles here are the following Bootstrap table classes: `.table`, `table-bordered` and `table-hover`.
You can change the styles by modifying line 104 in [toc-sidebar.html](toc-sidebar.html#L104) (or [toc-sidebarL.html](toc-sidebarL.html#L104) if local css and js files are used).
For example, if you want `.table-striped`, just replace `table table-bordered table-hover` into `table table-striped`.
Read [Bootstrap documentation](http://getbootstrap.com/css/#tables) for more Bootstrap table styles.

#### No navbar
If you do not want a navbar, you can remove `-B nav` option in step 4. However, for the time being, this will result in a not good looking layout :(   

## Output examples
### A single page
The following output examples are converted from [Pandoc's README file](https://github.com/jgm/pandoc/blob/master/README) and is using `toc-sidebarL.html` template
* with TOC: <https://mushiyo.github.io/pandoc-toc-sidebar/outWithTOC.html>
* without TOC: <https://mushiyo.github.io/pandoc-toc-sidebar/outWithoutTOC.html>

### A website
[My notes](http://twilightzone.gitlab.io/note), the contents are mostly written in Chinese, you can find the markdown source files [here](https://github.com/Mushiyo/note).
