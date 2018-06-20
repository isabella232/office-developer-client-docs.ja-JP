---
title: ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: 作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。 ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806111"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>ProtectMasters 要素 (DocumentSettings_Type complexType)'Visio XML (')

作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。 ユーザーこの設定に関係なく、マスター シェイプから新しい図形を作成できます。 
  
この要素に指定できる値の範囲は、'0' または '1' のいずれかです。 '0' の値は、ユーザーを作成、編集、または削除できるマスター シェイプを示します。 '1' の値は、あるユーザーを作成、編集、または削除できないマスター シェイプを示します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |ドキュメントの設定を指定する要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  

