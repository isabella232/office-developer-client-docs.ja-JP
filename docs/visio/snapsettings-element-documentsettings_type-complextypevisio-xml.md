---
title: SnapSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: 図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
ms.openlocfilehash: 0e784ddf9d5e04dae20a6a811557455c476b11a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806525"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>SnapSettings 要素 (DocumentSettings_Type complexType)'Visio XML (')

図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
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
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |ドキュメントの設定を指定する要素が含まれています。  <br/> |
   
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
   

