---
title: SnapExtensions 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。 値には、次の表の値の合計を指定できます。
ms.openlocfilehash: b1cf16a59480c9a800309f4a8c1411dfba52f4dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598025"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>SnapExtensions 要素 (Window_Type complexType) (Visio XML)

アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。 値には、次の表の値の合計を指定できます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>注釈

**SnapExtensions** 要素の値は、次の表の値の合計になります。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |配置ボックスの拡張機能にスナップします。  <br/> |
|2  <br/> |中心軸の拡張子にスナップします。  <br/> |
|4   <br/> |曲線の接線の拡張子にスナップします。  <br/> |
|8   <br/> |エンドポイント拡張機能にスナップします。  <br/> |
|16   <br/> |中点の拡張機能にスナップします。  <br/> |
|32  <br/> |線形拡張にスナップします。  <br/> |
|64  <br/> |曲線の拡張子にスナップします。  <br/> |
|128  <br/> |端点垂直拡張にスナップします。  <br/> |
|256  <br/> |垂直な中点の内線にスナップします。  <br/> |
|512  <br/> |端点の水平方向の拡張機能にスナップします。  <br/> |
|1024  <br/> |端点垂直拡張にスナップします。  <br/> |
|2048  <br/> |楕円の中心の拡張機能にスナップします。  <br/> |
|4096  <br/> |等角角度の拡張にスナップします。  <br/> |
   

