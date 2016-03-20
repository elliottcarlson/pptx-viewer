# &lt;a:chOff&gt;

Child Offset

#### Description

This element describes the position of a drawing element within a document.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_Point2D

#### Parent Elements

Name             | Type
---------------- | ----------------------------------
a:xfrm           | a:CT_GroupTransform2D

#### Child Elements

*None*

#### Attributes

Name   | Occ    | Type            | Description       | Default
------ | ------ | --------------- | ----------------- | -------
x      | [1..1] | a:ST_Coordinate | X-Axis Coordinate | 
y      | [1..1] | a:ST_Coordinate | Y-Axis Coordinate | 

#### Schema

```
<xsd:complexType name="CT_Point2D">
  <xsd:attribute name="x" type="ST_Coordinate" use="required"/>
  <xsd:attribute name="y" type="ST_Coordinate" use="required"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_off-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.spreadsheet.position.aspx
