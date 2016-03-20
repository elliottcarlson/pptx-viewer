# &lt;p:nvPr&gt;

Application Non-Visual Drawing Properties

#### Description

This element specifies non-visual properties for objects. These properties include multimedia content associated with an object and properties indicating how the object is to be used or displayed in different contexts.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/presentationml/2006/main
**Type**: p:CT_ApplicationNonVisualDrawingProps

#### Parent Elements

Name               | Type
------------------ | ----------------------------------
p:nvCxnSpPr        | p:CT_ConnectorNonVisual
p:nvGraphicFramePr | p:CT_GraphicalObjectFrameNonVisual
p:nvGrpSpPr        | p:CT_GroupShapeNonVisual
p:nvPicPr          | p:CT_PictureNonVisual
p:nvSpPr           | p:CT_ShapeNonVisual

#### Child Elements

Name            | Occ    | Type                      | Description
--------------- | ------ | ------------------------- | ----------------------------
p:ph            | [0..1] | p:CT_Placeholder          | Placeholder Shape
a:audioCd       | [0..1] | a:CT_AudioCD              | Audio from CD
a:wavAudioFile  | [0..1] | a:CT_EmbeddedWAVAudioFile | Audio from WAV File
a:audioFile     | [0..1] | a:CT_AudioFile            | Audio from File
a:videoFile     | [0..1] | a:CT_VideoFile            | Video from File
a:quickTimeFile | [0..1] | a:CT_QuickTimeFile        | QuickTime from File
p:custDataLst   | [0..1] | p:CT_CustomerDataList     | Customer Data List
p.extLst        | [0..1] | p:CT_ExtensionList        | Extension List

#### Attributes

Name      | Occ    | Type        | Description      | Default
--------- | ------ | ----------- | ---------------- | -------
isPhoto   | [0..1] | xsd:boolean | Is a Photo Album | "false"
userDrawn | [0..1] | xsd:boolean | Is User Drawn    | "false"

#### Schema

```
<xsd:complexType name="CT_ApplicationNonVisualDrawingProps">
  <xsd:sequence>
    <xsd:element name="ph" type="CT_Placeholder" minOccurs="0" maxOccurs="1"/>
    <xsd:group ref="a:EG_Media" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="custDataLst" type="CT_CustomerDataList" minOccurs="0" maxOccurs="1"/>
    <xsd:element name="extLst" type="CT_ExtensionList" minOccurs="0" maxOccurs="1"/>
  </xsd:sequence>
  <xsd:attribute name="isPhoto" type="xsd:boolean" use="optional" default="false"/>
  <xsd:attribute name="userDrawn" type="xsd:boolean" use="optional" default="false"/>
</xsd:complexType>

<xsd:group name="EG_Media">
  <xsd:choice>
    <xsd:element name="audioCd" type="CT_AudioCD"/>
    <xsd:element name="wavAudioFile" type="CT_EmbeddedWAVAudioFile"/>
    <xsd:element name="audioFile" type="CT_AudioFile"/>
    <xsd:element name="videoFile" type="CT_VideoFile"/>
    <xsd:element name="quickTimeFile" type="CT_QuickTimeFile"/>
  </xsd:choice>
</xsd:group>
```

#### References

http://www.datypic.com/sc/ooxml/e-p_nvPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.presentation.applicationnonvisualdrawingproperties.aspx
