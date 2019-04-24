---
title: snapextensions 要素 (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。 この値には、次の表の値の合計を指定できます。
ms.openlocfilehash: 57fde520d3dc8e0582c0062a599d5f38a73169b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334420"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>snapextensions 要素 (Window_Type complexType) (' Visio XML ')

アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。 この値には、次の表の値の合計を指定できます。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |windows .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>解説

**snapextensions**要素の値には、次の表の値の合計を指定できます。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |何もスナップしません。  <br/> |
|1-d  <br/> |図形枠の補助線にスナップします。  <br/> |
|pbm-2  <br/> |中央軸の拡張位置にスナップします。  <br/> |
|2/4  <br/> |曲線正接拡張機能にスナップします。  <br/> |
|~  <br/> |エンドポイント拡張機能にスナップします。  <br/> |
|16  <br/> |中点拡張機能にスナップします。  <br/> |
|32  <br/> |直線の延長形にスナップします。  <br/> |
|64  <br/> |曲線拡張機能にスナップします。  <br/> |
|128  <br/> |端点の垂直拡張線にスナップします。  <br/> |
|256  <br/> |中点の垂線拡張にスナップします。  <br/> |
|512  <br/> |端点の水平方向の拡張位置にスナップします。  <br/> |
|1024  <br/> |端点の垂直方向の拡張位置にスナップします。  <br/> |
|2048  <br/> |楕円形の中央拡張機能にスナップします。  <br/> |
|4096  <br/> |等角投影の角度の拡張にスナップします。  <br/> |
   

