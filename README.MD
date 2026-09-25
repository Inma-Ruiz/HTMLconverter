---
editor_options: 
  markdown: 
    wrap: sentence
---

# HTMLconverter

`make_qmd()` easily converts your `report.docx` into a `report.qmd` that can be rendered as HTML.

## Prior to conversion:

### Format of the word document

Your `report.docx` must use Heading 1 (H1) , Heading 2 (H2) Heading 3 (H3) , etc. for sections and subsections as they will be captured as such.
(In Word: Home/Styles/...)

All body text should use the Normal style.

You can use bulleted list.
(In Word: Home/Styles/bulleted)

Pictures and charts are better in SVG format.

Each image should be anchored to a blank line where you want the image to appear.
(In Word: right-click in the image, then set layout option to “In Line with Text” and ensure that “Move with text” is selected) 
Check in the Quarto document that the image appears as a single line of code with no text caption. Example: `![](media/image3.svg){width="100%"}`

### Header Image

The YAML the function produces includes a line that captures a banner image.

Place the image you want to use as a header, named `header_image.svg` inside the `output` folder

## Create the .qmd version of your report

Once the document is correctly formatted, place your `report.docx` file inside the `input` folder.

Run the `mainConverter.R` script in which you have entered the name of the file to be converted in the line: `make_qmd("input/ your_report_name.docx")` 
After running the code, a `report.qmd` document will appear inside the `output` folder.

Render the Quarto file to obtain the equivalent `report.html` publication.

If your document contains tables, they may need to be manually adjusted or aligned in the Quarto document after conversion and prior to rendering.

## Styling your HTML document

To customise the appearance of your document, edit the `output/style.css` file.
You can define your own style for each element, such as headings, paragraphs, colours, and font sizes.

...
work in progress
