---
title: ProtectMasters 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: ユーザーがマスター 図形の作成、編集、または削除を防止するかどうかを指定します。 ユーザーは、この設定に関係なく、マスター図形から新しい図形を作成できます。
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540694"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a>ProtectMasters 要素 (DocumentSettings_Type complexType) (Visio XML)

ユーザーがマスター 図形の作成、編集、または削除を防止するかどうかを指定します。 ユーザーは、この設定に関係なく、マスター図形から新しい図形を作成できます。 
  
この要素で使用できる値の範囲は、'0' または '1' です。 値 '0' は、ユーザーがマスター シェイプを作成、編集、または削除できる状態を示します。 値 '1' は、ユーザーがマスター 図形を作成、編集、または削除できないことを示します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |ドキュメント設定を指定する要素が含まれます。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  

