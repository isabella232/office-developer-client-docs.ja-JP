---
title: ソリューションの要素 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75e53ad0-3ca3-11a1-9107-63ec15601c13
description: ドキュメントに格納されているソリューションのプロパティを指定します。
ms.openlocfilehash: 65f6d3a34a62cd5e7b63ca0f6518a6e839b48360
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400222"
---
# <a name="solutions-element-visio-xml"></a>ソリューションの要素 ('Visio XML')

ドキュメントに格納されているソリューションのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Solutions_Type](solutions_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |solutions.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Solutions" type="Solutions_Type" ></xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

なし。
  
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Solution](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |XML は、図面に格納されているソリューションの 1 つのインスタンスを指定します。  <br/> |
   
### <a name="attributes"></a>属性

なし。
  

