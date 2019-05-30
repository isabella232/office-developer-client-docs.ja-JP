---
title: RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542836"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a>RefreshConflict 要素 (DataRecordSet_Type complexType) (Visio XML)

データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|PageID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |競合に関係する図形のページ ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|RowID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |データが更新された後に競合していた行の元の行 ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|ShapeID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |競合に関係する図形の図形 ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
   

