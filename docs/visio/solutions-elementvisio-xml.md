---
title: Solutions 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75e53ad0-3ca3-11a1-9107-63ec15601c13
description: ドキュメントに格納されているソリューションのプロパティを指定します。
ms.openlocfilehash: f41e448681928c515ac7cb0d820d951b21549f76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540225"
---
# <a name="solutions-element-visio-xml"></a>Solutions 要素 (Visio XML)

ドキュメントに格納されているソリューションのプロパティを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |solutions.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Solutions" type="Solutions_Type" ></xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[Solution](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |図面に格納されているソリューション XML のインスタンスを 1 つ指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

