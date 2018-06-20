---
title: SnapExtensions 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: 特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。
ms.openlocfilehash: 4c00d8d45c1eb33f57f727779db91e358a83a969
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806516"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions 要素 (DocumentSettings_Type complexType)'Visio XML (')

特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
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
  
## <a name="remarks"></a>備考

**SnapExtensions**要素の値は、次の表の値の合計にできます。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |何もスナップしません。  <br/> |
|1  <br/> |配置ボックスの拡張機能にスナップします。  <br/> |
|2  <br/> |軸の拡張機能を中心にスナップします。  <br/> |
|4  <br/> |カーブ正接の拡張機能にスナップします。  <br/> |
|8  <br/> |拡張子の端点にスナップします。  <br/> |
|16  <br/> |拡張子の中間点にスナップします。  <br/> |
|32  <br/> |線形拡張子にスナップします。  <br/> |
|64  <br/> |拡張子のカーブにスナップします。  <br/> |
|128  <br/> |端点の垂直な拡張子にスナップします。  <br/> |
|256  <br/> |垂直な拡張機能の中間点にスナップします。  <br/> |
|512  <br/> |水平引き出し線の端点にスナップします。  <br/> |
|1024  <br/> |垂直引き出し線の端点にスナップします。  <br/> |
|2048  <br/> |楕円の中心の拡張機能にスナップします。  <br/> |
|4096  <br/> |等角図の角度の拡張機能にスナップします。  <br/> |
   

