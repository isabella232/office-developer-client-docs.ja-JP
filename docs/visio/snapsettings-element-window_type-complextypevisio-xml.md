---
title: SnapSettings 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
ms.openlocfilehash: c3a160f289c1e08865ce3c7aa066fed4720724c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570008"
---
# <a name="snapsettings-element-window_type-complextype-visio-xml"></a>SnapSettings 要素 (Window_Type complexType) (Visio XML)

ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>注釈

値は、次の表の値の合計である場合があります。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |ルーラーのサブディビジョンにスナップします。  <br/> |
|2  <br/> |グリッドにスナップします。  <br/> |
|4   <br/> |ガイドにスナップします。  <br/> |
|8   <br/> |選択ハンドルにスナップします。  <br/> |
|16   <br/> |頂点にスナップします。  <br/> |
|32  <br/> |接続ポイントにスナップします。  <br/> |
|256  <br/> |図形の可視エッジにスナップします。  <br/> |
|512  <br/> |[配置ボックスにスナップ] をクリックします。  <br/> |
|1024  <br/> |図形の補助線オプションにスナップします。  <br/> |
|32768  <br/> |スナップが無効です。  <br/> |
|65536  <br/> |交点にスナップします。  <br/> |
   

