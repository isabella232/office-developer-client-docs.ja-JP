---
title: SnapSettings 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: 図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385208"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>SnapSettings 要素 (Window_Type complexType)'Visio XML (')

図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。
  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>備考

次の表の値の合計値があります。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |ルーラーの目盛りにスナップします。  <br/> |
|2  <br/> |グリッドにスナップします。  <br/> |
|4  <br/> |ガイドにスナップします。  <br/> |
|8  <br/> |選択ハンドルにスナップします。  <br/> |
|16  <br/> |頂点にスナップします。  <br/> |
|32  <br/> |接続ポイントにスナップします。  <br/> |
|256  <br/> |図形の可視のエッジにスナップします。  <br/> |
|512  <br/> |図形枠にスナップします。  <br/> |
|1024  <br/> |図形の補助線オプションにスナップします。  <br/> |
|32768  <br/> |スナップが無効になります。  <br/> |
|65536  <br/> |交点にスナップします。  <br/> |
   

