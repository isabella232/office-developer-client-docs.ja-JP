---
title: snapsettings 要素 (Window_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。
ms.openlocfilehash: b4793c6d9c13a922db4d3ed9504a3a08e933230a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334504"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>snapsettings 要素 (Window_Type complexType) (' Visio XML ')

ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |windows .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Microsoft Visio インスタンスで開いているウィンドウを表します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>解説

値には、次の表の値の合計を指定できます。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |何もスナップしません。  <br/> |
|1-d  <br/> |ルーラーの目盛りにスナップします。  <br/> |
|pbm-2  <br/> |グリッドにスナップします。  <br/> |
|2/4  <br/> |ガイドにスナップします。  <br/> |
|~  <br/> |選択ハンドルにスナップします。  <br/> |
|16  <br/> |頂点にスナップします。  <br/> |
|32  <br/> |接続ポイントにスナップします。  <br/> |
|256  <br/> |表示されている図形の端にスナップします。  <br/> |
|512  <br/> |整列ボックスにスナップします。  <br/> |
|1024  <br/> |図形の補助線オプションにスナップします。  <br/> |
|32768  <br/> |スナップは無効です。  <br/> |
|65536  <br/> |交点にスナップします。  <br/> |
   

