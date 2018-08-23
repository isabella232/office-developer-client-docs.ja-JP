---
title: RefreshConflict 要素 (DataRecordSet_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: データ レコード セットが更新された後に、競合がある図形にリンクされているデータ レコード セット内の行を示します。
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806170"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>RefreshConflict 要素 (DataRecordSet_Type complexType)'Visio XML (')

データ レコード セットが更新された後に、競合がある図形にリンクされているデータ レコード セット内の行を示します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[データ レコード セット](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |競合に関連する図形のページの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|RowID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |競合データが更新された後の現在の行の元の行の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |競合に関連する図形の図形 ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

