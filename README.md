# ShEx Extends Paper Companion

This repository contains examples and code from the paper about ShEx+extends in order to make the contents of the paper reproducible. The folder <code>Examples</code> contains the examples from the paper.


## Running the examples using ShEx simple demo

The ShEx simple demo can be used to run the examples interactively by clicking <a href="https://shex.io/webapps/shex.js/packages/shex-webapp/doc/shex-simple?manifestURL=https://raw.githubusercontent.com/weso/shex_extends_paper_companion/master/examples/manifest.yml">this link</a>.

## Running the examples using the RDFShape playground

The https://rdfshape.weso.es playground can also be used to run the examples based on the Scala implementation:

<ul>
<li>Products
<ul>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct1%40%3CProduct%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:product1</code> as <code>&lt;Product&gt;</code></a></li>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct2%40%3CGoodProduct%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:product2</code> as <code>&lt;GoodProduct&gt;</code></a></li>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct1%40%3CGoodProduct%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Failing to validate <code>:product1</code> as <code>&lt;GoodProduct&gt;</code></a></li>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct3%40%3CExternalProduct%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:product3</code> as <code>&lt;ExternalProduct&gt;</code></a></li>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct3%40%3CProduct%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:product3</code> as <code>&lt;Product&gt;</code></a></li>
<li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aproduct1%20%3Acode%201%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2023%5D%3B%0A%20%3Arelated%20%3Aproduct2%20.%0A%0A%3Aproduct2%20%3Aname%20%22Nice%20Book%22%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2045%5D%20.%0A%0A%3Aproduct3%20%3Acode%203%20%3B%0A%20%3Areview%20%5B%3Avalue%20%3AGood%3B%20%3Atimestamp%2067%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%20%3ABad%3B%20%3Atimestamp%2078%5D%2C%20%0A%20%20%20%20%20%20%20%20%20%5B%3Avalue%205%5D%2C%20%5B%3Avalue%202%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0A%0A%3CProduct%3E%20%7B%0A%20%28%3Acode%20xsd%3Ainteger%20%7C%20%3Aname%20xsd%3Astring%20%29%3B%0A%20%3Areview%20%40%3CReview%3E%20%2A%20%3B%0A%20%3Arelated%20%40%3CProduct%3E%20%2A%20%0A%7D%0A%0A%3CReview%3E%20%7B%0A%20%3Avalue%20%20%5B%3ABad%20%3AGood%5D%3B%0A%20%3Atimestamp%20xsd%3Ainteger%0A%7D%0A%0A%3CGoodProduct%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CGoodReview%3E%20%2A%20%3B%0A%7D%0A%3CGoodReview%3E%20%7B%20%0A%20%3Avalue%20%5B%3AGood%5D%20%0A%7D%0A%0A%3CExternalProductAttempt%3E%20%40%3CProduct%3E%20AND%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%20%0A%7D%0A%3CExternalReview%3E%20%7B%20%0A%20%3Avalue%20xsd%3Ainteger%20%0A%7D%0A%0A%3CExternalProduct%3E%20extends%20%40%3CProduct%3E%20%7B%0A%20%3Areview%20%40%3CExternalReview%3E%20%2A%0A%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aproduct3%40%3CExternalProductAttempt%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Failing to validate <code>:product3</code> as <code>&lt;ExternalProductAttempt&gt;</code></a></li>
</ul>
</li>
<li>Figures
  <ul>
  <li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aorigin%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%200%5D%20%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%200%5D%20.%0A%0A%3Abad1%20%3Acomponent%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%200%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%201%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AYCoord%3B%20%3Avalue%200%3B%20%5D%20.%0A%0A%3Abad2%20%3Acomponent%20%20%20%20%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Unspecified%22%20%5D%20.%0A%20%20%20%20%0A%3Ar1%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22A%20red%20rectangle%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%202%5D%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%203%5D%2C%0A%20%5B%3Atype%20%3AColor%3B%20%3Avalue%20%3ARed%5D%2C%20%0A%20%5B%3Atype%20%3AHeight%3B%20%3Avalue%204%5D%2C%20%5B%3Atype%20%3AWidth%3B%20%3Avalue%205%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0Aabstract%20%3CFigure%3E%20%7B%0A%20%3Acomponent%20%40%3CLabel%3E%0A%7D%0A%0A%3CLabel%3E%20%7B%20%3Atype%20%5B%20%3ALabel%20%5D%3B%20%3Avalue%20xsd%3Astring%20%7D%0A%0A%3CGeoFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CPosX%3E%20%3B%0A%20%20%3Acomponent%20%40%3CPosY%3E%0A%7D%0A%0A%3CPosX%3E%20%7B%20%3Atype%20%5B%20%3AXCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CPosY%3E%20%7B%20%3Atype%20%5B%20%3AYCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%0A%3CColoredFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CColor%3E%0A%7D%0A%0A%3CRectangle%3E%20extends%20%40%3CGeoFigure%3E%20extends%20%40%3CColoredFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CHeight%3E%20%3B%0A%20%20%3Acomponent%20%40%3CWidth%3E%0A%7D%0A%0A%3CColor%3E%20%7B%3Atype%20%5B%20%3AColor%20%5D%3B%20%3Avalue%20%5B%3ARed%20%3AGreen%20%3ABlue%20%5D%20%7D%0A%3CHeight%3E%20%7B%3Atype%20%5B%20%3AHeight%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CWidth%3E%20%7B%3Atype%20%5B%20%3AWidth%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Aorigin%40%3CFigure%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:origin</code> as <code>&lt;Figure&gt;</code></a></li>

  <li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aorigin%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%200%5D%20%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%200%5D%20.%0A%0A%3Abad1%20%3Acomponent%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%200%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%201%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AYCoord%3B%20%3Avalue%200%3B%20%5D%20.%0A%0A%3Abad2%20%3Acomponent%20%20%20%20%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Unspecified%22%20%5D%20.%0A%20%20%20%20%0A%3Ar1%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22A%20red%20rectangle%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%202%5D%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%203%5D%2C%0A%20%5B%3Atype%20%3AColor%3B%20%3Avalue%20%3ARed%5D%2C%20%0A%20%5B%3Atype%20%3AHeight%3B%20%3Avalue%204%5D%2C%20%5B%3Atype%20%3AWidth%3B%20%3Avalue%205%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0Aabstract%20%3CFigure%3E%20%7B%0A%20%3Acomponent%20%40%3CLabel%3E%0A%7D%0A%0A%3CLabel%3E%20%7B%20%3Atype%20%5B%20%3ALabel%20%5D%3B%20%3Avalue%20xsd%3Astring%20%7D%0A%0A%3CGeoFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CPosX%3E%20%3B%0A%20%20%3Acomponent%20%40%3CPosY%3E%0A%7D%0A%0A%3CPosX%3E%20%7B%20%3Atype%20%5B%20%3AXCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CPosY%3E%20%7B%20%3Atype%20%5B%20%3AYCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%0A%3CColoredFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CColor%3E%0A%7D%0A%0A%3CRectangle%3E%20extends%20%40%3CGeoFigure%3E%20extends%20%40%3CColoredFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CHeight%3E%20%3B%0A%20%20%3Acomponent%20%40%3CWidth%3E%0A%7D%0A%0A%3CColor%3E%20%7B%3Atype%20%5B%20%3AColor%20%5D%3B%20%3Avalue%20%5B%3ARed%20%3AGreen%20%3ABlue%20%5D%20%7D%0A%3CHeight%3E%20%7B%3Atype%20%5B%20%3AHeight%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CWidth%3E%20%7B%3Atype%20%5B%20%3AWidth%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Ar1%40%3CRectangle%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Validating <code>:r1</code> as <code>&lt;rectangle&gt;</code></a></li>

  <li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aorigin%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%200%5D%20%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%200%5D%20.%0A%0A%3Abad1%20%3Acomponent%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%200%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%201%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AYCoord%3B%20%3Avalue%200%3B%20%5D%20.%0A%0A%3Abad2%20%3Acomponent%20%20%20%20%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Unspecified%22%20%5D%20.%0A%20%20%20%20%0A%3Ar1%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22A%20red%20rectangle%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%202%5D%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%203%5D%2C%0A%20%5B%3Atype%20%3AColor%3B%20%3Avalue%20%3ARed%5D%2C%20%0A%20%5B%3Atype%20%3AHeight%3B%20%3Avalue%204%5D%2C%20%5B%3Atype%20%3AWidth%3B%20%3Avalue%205%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0Aabstract%20%3CFigure%3E%20%7B%0A%20%3Acomponent%20%40%3CLabel%3E%0A%7D%0A%0A%3CLabel%3E%20%7B%20%3Atype%20%5B%20%3ALabel%20%5D%3B%20%3Avalue%20xsd%3Astring%20%7D%0A%0A%3CGeoFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CPosX%3E%20%3B%0A%20%20%3Acomponent%20%40%3CPosY%3E%0A%7D%0A%0A%3CPosX%3E%20%7B%20%3Atype%20%5B%20%3AXCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CPosY%3E%20%7B%20%3Atype%20%5B%20%3AYCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%0A%3CColoredFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CColor%3E%0A%7D%0A%0A%3CRectangle%3E%20extends%20%40%3CGeoFigure%3E%20extends%20%40%3CColoredFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CHeight%3E%20%3B%0A%20%20%3Acomponent%20%40%3CWidth%3E%0A%7D%0A%0A%3CColor%3E%20%7B%3Atype%20%5B%20%3AColor%20%5D%3B%20%3Avalue%20%5B%3ARed%20%3AGreen%20%3ABlue%20%5D%20%7D%0A%3CHeight%3E%20%7B%3Atype%20%5B%20%3AHeight%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CWidth%3E%20%7B%3Atype%20%5B%20%3AWidth%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Abad1%40%3CFigure%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Failing to validate <code>:bad1</code> as <code>&lt;Figure&gt;</code></a> (it has two X coordinates)</li>

  <li><a href="https://rdfshape.weso.es/shexValidate?data=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0A%0A%3Aorigin%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%200%5D%20%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%200%5D%20.%0A%0A%3Abad1%20%3Acomponent%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Origin%22%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%200%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AXCoord%3B%20%3Avalue%201%3B%20%5D%20%2C%0A%20%20%20%20%5B%20%3Atype%20%3AYCoord%3B%20%3Avalue%200%3B%20%5D%20.%0A%0A%3Abad2%20%3Acomponent%20%20%20%20%20%0A%20%20%20%20%5B%20%3Atype%20%3ALabel%3B%20%3Avalue%20%22Unspecified%22%20%5D%20.%0A%20%20%20%20%0A%3Ar1%20%3Acomponent%20%0A%20%5B%3Atype%20%3ALabel%3B%20%3Avalue%20%22A%20red%20rectangle%22%5D%20%2C%0A%20%5B%3Atype%20%3AXCoord%3B%20%3Avalue%202%5D%2C%20%5B%3Atype%20%3AYCoord%3B%20%3Avalue%203%5D%2C%0A%20%5B%3Atype%20%3AColor%3B%20%3Avalue%20%3ARed%5D%2C%20%0A%20%5B%3Atype%20%3AHeight%3B%20%3Avalue%204%5D%2C%20%5B%3Atype%20%3AWidth%3B%20%3Avalue%205%5D%20.&dataFormat=Turtle&dataInference=NONE&dataSource=byText&schema=prefix%20%3A%20%20%20%20%20%20%20%3Chttp%3A%2F%2Fexample.org%2F%3E%0Aprefix%20xsd%3A%20%20%20%20%3Chttp%3A%2F%2Fwww.w3.org%2F2001%2FXMLSchema%23%3E%0Aprefix%20schema%3A%20%3Chttp%3A%2F%2Fschema.org%2F%3E%0A%0Aabstract%20%3CFigure%3E%20%7B%0A%20%3Acomponent%20%40%3CLabel%3E%0A%7D%0A%0A%3CLabel%3E%20%7B%20%3Atype%20%5B%20%3ALabel%20%5D%3B%20%3Avalue%20xsd%3Astring%20%7D%0A%0A%3CGeoFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CPosX%3E%20%3B%0A%20%20%3Acomponent%20%40%3CPosY%3E%0A%7D%0A%0A%3CPosX%3E%20%7B%20%3Atype%20%5B%20%3AXCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CPosY%3E%20%7B%20%3Atype%20%5B%20%3AYCoord%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%0A%3CColoredFigure%3E%20extends%20%40%3CFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CColor%3E%0A%7D%0A%0A%3CRectangle%3E%20extends%20%40%3CGeoFigure%3E%20extends%20%40%3CColoredFigure%3E%20%7B%0A%20%20%3Acomponent%20%40%3CHeight%3E%20%3B%0A%20%20%3Acomponent%20%40%3CWidth%3E%0A%7D%0A%0A%3CColor%3E%20%7B%3Atype%20%5B%20%3AColor%20%5D%3B%20%3Avalue%20%5B%3ARed%20%3AGreen%20%3ABlue%20%5D%20%7D%0A%3CHeight%3E%20%7B%3Atype%20%5B%20%3AHeight%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D%0A%3CWidth%3E%20%7B%3Atype%20%5B%20%3AWidth%20%5D%3B%20%3Avalue%20xsd%3Ainteger%20%7D&schemaEngine=ShEx&schemaFormat=ShExC&schemaSource=byText&shape-map=%3Abad2%40%3CFigure%3E&shapeMapFormat=Compact&shapeMapSource=byText&triggerMode=ShapeMap">Failing to validate <code>:bad2</code> as <code>&lt;Figure&gt;</code></a> (no concrete descendant conforms to Figure, only conforms with Figure but it is an  abstract shape)</li></ul>
</li>
</ul>