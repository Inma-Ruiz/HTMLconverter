---
editor_options: 
  markdown: 
    wrap: sentence
---

# HTMLconverter

**make_qmd()** easily converts your **report.docx** into a **report.qmd** that can be rendered as HTML.

## Prior conversion:

### Format of the word document 

Your **report.docx** must use Heading 1 (H1) , Heading 2 (H2) Heading 3 (H3) , etcetera for sections and subsections as they will be captured as such.
(In Word: Home/Styles/...)

All body text should use the Normal style.

You can use bulled list.
(In Word: Home/Styles/bulletted)

Pictures and charts better if in SVG format.

Each image should be anchored to a blank line where you want the image to appear.
(In Word: right click in the image then set layout option to “In Line with Text” and ensure that “Move with text” is selected) and check in the quarto document that the image appears as a single line like that: ![](media/image3.svg){width="100%"}

### Header Image

The YAML the function produces include a line that captures a banner image.

Place the image you want to use as a header, named as **header_image.svg** inside the **output** folder

## Create the .qmd version of your report

Once the document is correctly formatted, place your_publication.docx file in the **input** folder.

Run the **mainConverter.R** script in which you have entered the name of the file to be converted in the line: make_qmd("input/ your_report_name.docx ") After running the code, a **report.qmd** document will appear in the output folder.

Render the Quarto file to obtain the equivalent **report.html** publication.

If your document contains tables, they may need to be manually adjusted or aligned in the Quarto document after conversion and prior to the rendering.

## Styling your HTML document

You can use your own **style.css** (place it on the **outpu**t folder)

...
I am still working on that
