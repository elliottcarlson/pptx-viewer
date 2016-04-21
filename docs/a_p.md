# &lt;a:p&gt;

Text Paragraphs

#### Description

This element specifies the presence of a paragraph of text within the containing text body. The paragraph is the highest level text separation mechanism within a text body. A paragraph can contain text paragraph properties associated with the paragraph. If no properties are listed then properties specified in the defPPr element are used.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_TextParagraph

#### Parent Elements

Name   | Type
------ | -------------
draw-chart:rich    | a:CT_TextBody
draw-chart:txPr    | a:CT_TextBody
cdr:txBody         | a:CT_TextBody
draw-diag:t        | a:CT_TextBody
a:txBody           | a:CT_TextBody
draw-ssdraw:txBody | a:CT_TextBody
p:txBody           | a:CT_TextBody

#### Child Elements

Name         | Occ    | Type                         | Description
------------ | ------ | ---------------------------- | ----------------------------
a:pPr        | [0..1] | a:CT_TextParagraphProperties | Text Paragraph Properties
a:r          | [0..*] | a:CT_RegularTextRun          | Text Run
a:br         | [0..*] | a:CT_TextLineBreak           | Text Line Break
a:fld        | [0..*] | a:CT_TextField               | Text Field
a:endParaRPr | [0..1] | a:CT_TextCharacterProperties | End Paragraph Run Properties

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_TextParagraph">
  <xsd:sequence>
    <xsd:element name="pPr" type="CT_TextParagraphProperties" minOccurs="0" />
    <xsd:group ref="EG_TextRun" minOccurs="0" maxOccurs="unbounded" />
    <xsd:element name="endParaRPr" type="CT_TextCharacterProperties" minOccurs="0" />
  </xsd:sequence>
</xsd:complexType>

<xsd:group name="EG_TextRun">
  <xsd:choice>
    <xsd:element name="r" type="CT_RegularTextRun" />
    <xsd:element name="br" type="CT_TextLineBreak" />
    <xsd:element name="fld" type="CT_TextField" />
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_p-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.paragraph.aspx
