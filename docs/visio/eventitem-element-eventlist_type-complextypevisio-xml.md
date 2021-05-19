---
title: EventItem 要素 (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: イベント コードをカプセル化します。
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541842"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a>EventItem 要素 (EventList_Type complexType) (Visio XML)

イベント コードをカプセル化します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |オブジェクトが応答 **するイベントごとに EventItem** 要素を含む。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Action  <br/> |xsd:unsignedShort  <br/> |必須  <br/> |親 EventItem 要素のアクション コード **を指定** します。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|有効  <br/> |xsd:boolean  <br/> |省略可能  <br/> |イベントが有効または無効かどうかを示すフラグを表します。  <br/> |xsd:boolean 型の値。  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |必須  <br/> |アドオンをトリガーするイベントを示すコード。  <br/> |xsd:unsignedShort 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |イベントの ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Target  <br/> |xsd:string  <br/> |必須  <br/> |イベントのターゲットを指定します。  <br/> |xsd:string 型の値。  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |必須  <br/> |イベントのターゲットに送信する引数を含む文字列を指定します。  <br/> |xsd:string 型の値。  <br/> |
   

