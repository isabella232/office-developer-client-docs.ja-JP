---
title: Windows 要素 (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: 文書のウィンドウ要素を格納します。
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339824"
---
# <a name="windows-element-visio-xml"></a>Windows 要素 (' Visio XML ')

文書の**ウィンドウ**要素を格納します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |windows .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |表示領域の高さの次元を表します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
|ClientWidth  <br/> |xsd: アン signedshort  <br/> |省略可能  <br/> |表示領域の幅の大きさを表します。  <br/> |xsd: _ signedshort 型の値。  <br/> |
   

