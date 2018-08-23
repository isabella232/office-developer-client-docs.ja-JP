---
title: cp 要素 (Text_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: 文字プロパティの最初の実行されているマークは、対応する Char 要素に従って書式設定されました。 実行は、次のタグまで、テキストの末尾に定義されています。
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805138"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a>cp 要素 (Text_Type complexType)'Visio XML (')

文字プロパティの最初の実行されているマークは、対応する Char 要素に従って書式設定されました。 実行は、次のタグまで、テキストの末尾に定義されています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[cp_Type](cp_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml のページで、マスターの # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |図形のテキストが含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |このプロパティの実行を表す Char 要素のインデックス。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

