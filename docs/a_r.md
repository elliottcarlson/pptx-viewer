# &lt;a:r&gt;

Text Run

#### Description

This element specifies the presence of a run of text within the containing text body. The run element is the lowest level text separation mechanism within a text body. A text run can contain text run properties associated with the run. If no properties are listed then properties specified in the defRPr element are used.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_RegularTextRun

#### Parent Elements

Name   | Type
------ | ------------------
a:p    | a:CT_TextParagraph

#### Child Elements

Name   | Occ    | Type                         | Description
------ | ------ | ---------------------------- | ----------------------------
a:rPr  | [0..1] | a:CT_TextCharacterProperties | Text Character Properties
a:t    | [1..1] | xsd:string                   | Text String

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_RegularTextRun">
  <xsd:sequence>
    <xsd:element name="rPr" type="CT_TextCharacterProperties" minOccurs="0"/>
    <xsd:element name="t" type="xsd:string"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_r-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.run.aspx
http://python-pptx.readthedocs.org/en/develop/dev/analysis/schema/ct_textparagraph.html
