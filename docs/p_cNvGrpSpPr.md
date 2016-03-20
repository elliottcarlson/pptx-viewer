# &lt;p:cNvGrpSpPr&gt;

Non-Visual Group Shape Drawing Properties

#### Description

This element specifies the non-visual properties of a hierarchical grouping of shapes, graphical object frames, and child groups. These are the set of properties of a group which do not affect its display within a spreadsheet.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: a:CT_NonVisualGroupDrawingShapeProps

#### Parent Elements

- Type p:CT_GroupShapeNonVisual (`<p:nvGrpSpPr>`)

#### Child Elements

Name         | Occ    | Type                        | Description
------------ | ------ | --------------------------- | ----------------------------
a:grpSpLocks | [0..1] | a:CT_GroupLocking           | Group Shape Locks
a:extLst     | [0..1] | a:CT_OfficeArtExtensionList | Extension List

#### Attributes

*None*

#### Schema

```
<xsd:complexType name="CT_NonVisualGroupDrawingShapeProps">
  <xsd:sequence>
    <xsd:element name="grpSpLocks" type="CT_GroupLocking" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_cNvGrpSpPr-1.html
https://msdn.microsoft.com/en-us/library/documentformat.openxml.drawing.spreadsheet.nonvisualgroupshapedrawingproperties(v=office.15).aspx
