# &lt;a:pPr&gt;

Text Paragraph Properties

#### Description

This element contains all paragraph level text properties for the containing paragraph. These paragraph properties should override any and all conflicting properties that are associated with the paragraph in question.

#### Element Information

**Namespace**: http://schemas.openxmlformats.org/drawingml/2006/main
**Type**: a:CT_TextParagraphProperties

#### Parent Elements

Name  | Type
----- | ------------------
a:fld | a:CT_TextField
a:p   | a:CT_TextParagraph

#### Child Elements

Name         | Occ    | Type                              | Description
------------ | ------ | --------------------------------- | ----------------------------
a:lnSpc      | [0..1] | a:CT_TextSpacing                  | Line Spacing
a:spcBef     | [0..1] | a:CT_TextSpacing                  | Space Before
a:spcAft     | [0..1] | a:CT_TextSpacing                  | Space After
a:buClrTx    | [0..1] | a:CT_TextBulletColorFollowText    | Follow Text
a:buClr      | [0..1] | a:CT_Color                        | Color Specified
a:buSzTx     | [0..1] | a:CT_TextBulletSizeFollowText     | Bullet Size Follows Text
a:buSzPct    | [0..1] | a:CT_TextBulletSizePercent        | Bullet Size Percentage
a:buSzPts    | [0..1] | a:CT_TextBulletSizePoint          | Bullet Size Points
a:buFontTx   | [0..1] | a:CT_TextBulletTypefaceFollowText | Follow Text
a:buFont     | [0..1] | a:CT_TextFont                     | Specified
a:buNone     | [0..1] | a:CT_TextNoBullet                 | No Bullet
a:buAutoNum  | [0..1] | a:CT_TextAutonumberBullet         | Auto-Numbered Bullet
a:buChar     | [0..1] | a:CT_TextCharBullet               | Character Bullet
a:buBlip     | [0..1] | a:CT_TextBlipBullet               | Picture Bullet
a:tabLst     | [0..1] | a:CT_TextTabStopList              | Tab List
a:defRPr     | [0..1] | a:CT_TextCharacterProperties      | Default Text Run Properties
a:extLst     | [0..1] | a:CT_OfficeArtExtensionList       | Extension List

#### Attributes

Name         | Occ    | Type                     | Description           | Default
------------ | ------ | ------------------------ | --------------------- | -------
marL         | [0..1] | a:ST_TextMargin          | Left Margin           | 
marR         | [0..1] | a:ST_TextMargin          | Right Margin          | 
lvl          | [0..1] | a:ST_TextIndentLevelType | Level                 | 
indent       | [0..1] | a:ST_TextIndent          | Indent                | 
algn         | [0..1] | a:ST_TextAlignType       | Alignment             | 
defTabSz     | [0..1] | a:ST_Coordinate32        | Default Tab Size      | 
rtl          | [0..1] | xsd:boolean              | Right To Left         | 
eaLnBrk      | [0..1] | xsd:boolean              | East Asian Line Break | 
fontAlgn     | [0..1] | a:ST_TextFontAlignType   | Font Alignment        | 
latinLnBrk   | [0..1] | xsd:boolean              | Latin Line Break      | 
hangingPunct | [0..1] | xsd:boolean              | Hanging Punctuation   | 

#### Schema

```
<xsd:complexType name="CT_TextParagraphProperties">
  <xsd:sequence>
    <xsd:element name="lnSpc" type="CT_TextSpacing" minOccurs="0"/>
    <xsd:element name="spcBef" type="CT_TextSpacing" minOccurs="0"/>
    <xsd:element name="spcAft" type="CT_TextSpacing" minOccurs="0"/>
    <xsd:group ref="EG_TextBulletColor" minOccurs="0"/>
    <xsd:group ref="EG_TextBulletSize" minOccurs="0"/>
    <xsd:group ref="EG_TextBulletTypeface" minOccurs="0"/>
    <xsd:group ref="EG_TextBullet" minOccurs="0"/>
    <xsd:element name="tabLst" type="CT_TextTabStopList" minOccurs="0"/>
    <xsd:element name="defRPr" type="CT_TextCharacterProperties" minOccurs="0"/>
    <xsd:element name="extLst" type="CT_OfficeArtExtensionList" minOccurs="0"/>
  </xsd:sequence>
  <xsd:attribute name="marL" type="ST_TextMargin"/>
  <xsd:attribute name="marR" type="ST_TextMargin"/>
  <xsd:attribute name="lvl" type="ST_TextIndentLevelType"/>
  <xsd:attribute name="indent" type="ST_TextIndent"/>
  <xsd:attribute name="algn" type="ST_TextAlignType"/>
  <xsd:attribute name="defTabSz" type="ST_Coordinate32"/>
  <xsd:attribute name="rtl" type="xsd:boolean"/>
  <xsd:attribute name="eaLnBrk" type="xsd:boolean"/>
  <xsd:attribute name="fontAlgn" type="ST_TextFontAlignType"/>
  <xsd:attribute name="latinLnBrk" type="xsd:boolean"/>
  <xsd:attribute name="hangingPunct" type="xsd:boolean"/>
</xsd:complexType>
```

#### References

http://www.datypic.com/sc/ooxml/e-a_pPr-1.html
https://msdn.microsoft.com/en-us/library/office/documentformat.openxml.drawing.paragraphproperties.aspx
http://python-pptx.readthedocs.org/en/develop/dev/analysis/schema/ct_textparagraph.html
