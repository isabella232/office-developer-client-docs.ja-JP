---
title: SnapExtensions 要素 (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。
ms.openlocfilehash: 86ff7f32d6e12b2f0d7a8387d8e5b7ae9870b5fa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540379"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>SnapExtensions 要素 (DocumentSettings_Type complexType) (Visio XML)

アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書の xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |ドキュメントの設定を指定する要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  
## <a name="remarks"></a>注釈

**Snapextensions**要素の値には、次の表の値の合計を指定できます。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |何もスナップしません。  <br/> |
|1-d  <br/> |図形枠の補助線にスナップします。  <br/> |
|pbm-2  <br/> |中央軸の拡張位置にスナップします。  <br/> |
|2/4  <br/> |曲線正接拡張機能にスナップします。  <br/> |
|8   <br/> |エンドポイント拡張機能にスナップします。  <br/> |
|16  <br/> |中点拡張機能にスナップします。  <br/> |
|32  <br/> |直線の延長形にスナップします。  <br/> |
|64  <br/> |曲線拡張機能にスナップします。  <br/> |
|128  <br/> |端点の垂直拡張線にスナップします。  <br/> |
|256  <br/> |中点の垂線拡張にスナップします。  <br/> |
|512  <br/> |端点の水平方向の拡張位置にスナップします。  <br/> |
|1024  <br/> |端点の垂直方向の拡張位置にスナップします。  <br/> |
|2048  <br/> |楕円形の中央拡張機能にスナップします。  <br/> |
|4096  <br/> |等角投影の角度の拡張にスナップします。  <br/> |
   

