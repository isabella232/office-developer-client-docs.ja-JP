---
title: SnapAngles 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5997f374-303a-92b6-6dd3-87ef81104af4
description: SnapAngle 要素のコレクションが含まれます。
ms.openlocfilehash: e069b14f4df799b5a568d2b1aa488015740529fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549596"
---
# <a name="snapangles-element-window_type-complextype-visio-xml"></a>SnapAngles 要素 (Window_Type complexType) (Visio XML)

**SnapAngle** 要素のコレクションが含まれます。 
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[SnapAngle](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[SnapAngle_Type](snapangle_type-complextypevisio-xml.md) <br/> |スナップ角度を度数で指定する浮動小数点数を含む。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

