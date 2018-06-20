---
title: EventItem 要素 (EventList_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベント コードをカプセル化します。
ms.openlocfilehash: dcdd3aa264e8ddfb1aa6f2e908f1c43a0d470872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805326"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>EventItem 要素 (EventList_Type complexType)'Visio XML (')

イベント コードをカプセル化します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |オブジェクトが応答する各イベントの**EventItem**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|アクション  <br/> |xsd:unsignedShort  <br/> |必須  <br/> |**EventItem**の親要素のアクション コードを指定します。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|Enabled  <br/> |xsd:boolean  <br/> |省略可能  <br/> |イベントが有効か無効になっているかどうかを示すフラグを表します。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |必須  <br/> |アドオンをトリガーするイベントを示すコードです。  <br/> |Xsd:unsignedShort の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |イベントの ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ターゲット  <br/> |xsd:string  <br/> |必須  <br/> |イベントのターゲットを指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |必須  <br/> |イベントのターゲットに送る引数を含む文字列を指定します。  <br/> |Xsd:string の値を入力します。  <br/> |
   

