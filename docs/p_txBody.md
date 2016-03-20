# &lt;p:txBody&gt;

Shape Text Body

#### Description

This element specifies the existence of text to be contained within the corresponding shape. All visible text and visible text related properties are contained within this element. There can be multiple paragraphs and within paragraphs multiple runs of text.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_TextBody

#### Parent Elements

Name   | Type
------ | ----------
p:sp   | p:CT_Shape

#### Child Elements

Name       | Occ    | Type                     | Description
---------- | ------ | ------------------------ | ----------------------------
a:bodyPr   | [1..1] | a:CT_TextBodyProperties  | Body Properties
a:lstStyle | [1..1] | a:CT_TextListStyle       | Text List Styles
a:p        | [1..*] | a:CT_TextParagraph       | Text Paragraphs

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_TextBody">
  <xsd:sequence>
    <xsd:element name="bodyPr" type="CT_TextBodyProperties" minOccurs="1" maxOccurs="1"/>
    <xsd:element name="lstStyle" type="CT_TextListStyle" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="p" type="CT_TextParagraph" minOccurs="1" maxOccurs="unbounded"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_txBody-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.spreadsheet.textbody.aspx
