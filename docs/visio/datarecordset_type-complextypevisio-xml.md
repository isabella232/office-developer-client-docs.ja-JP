---
title: DataRecordSet_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360362"
---
# <a name="datarecordsettype-complextype-visio-xml"></a>DataRecordSet_Type complexType (' Visio XML ')

## <a name="type-information"></a>型情報

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15-06-05  <br/> |
|**拡張ベース** <br/> |なし  <br/> |
   
## <a name="definition"></a>定義

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> ||
|[refreshconflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
|[rowmap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|チェックサム  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|Command  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|ConnectionID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> ||xsd:/signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> ||xsd: string 型の値。  <br/> |
|nextrowid  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|Options  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|RefreshInterval  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|RefreshOverwriteAll  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|ReplaceLinks  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> ||xsd:/signedint 型の値。  <br/> |
|RowOrder  <br/> |xsd: boolean  <br/> |省略可能  <br/> ||xsd: boolean 型の値。  <br/> |
|TimeRefreshed  <br/> |xsd: dateTime  <br/> |省略可能  <br/> ||xsd: dateTime 型の値。  <br/> |
   

