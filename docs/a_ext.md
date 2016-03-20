# &lt;a:ext&gt;

Extents

#### Description

This element describes the length and width properties for how far a drawing element should extend for.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_PositiveSize2D

#### Parent Elements

Name             | Type
---------------- | ----------------------------------
a:xfrm           | a:CT_GroupTransform2D
cdr:xfrm         | a:CT_Transform2D
a:xfrm           | a:CT_Transform2D
draw-ssdraw:xfrm | a:CT_Transform2D
p:xfrm           | a:CT_Transform2D

#### Child Elements

*None*

#### Attributes

Name   | Occ    | Type                    | Description   | Default
------ | ------ | ----------------------- | ------------- | -------
cx     | [1..1] | a:ST_PositiveCoordinate | Extent Length | 
cy     | [1..1] | a:ST_PositiveCoordinate | Extent Width  | 

#### Schema

```
<xsd:complexType name="CT_PositiveSize2D">
  <xsd:attribute name="cx" type="ST_PositiveCoordinate" use="required"/>
  <xsd:attribute name="cy" type="ST_PositiveCoordinate" use="required"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_ext-2.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.chartdrawing.extent.aspx
