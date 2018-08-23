---
title: 「接続タイプ」の複合型 ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c0ac13b-70cc-398b-a1a3-e7d8080c8f7b
ms.openlocfilehash: d927a70a887de93609755246e879381ab884e925
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805105"
---
# <a name="connectiontype-complextype-visio-xml"></a><span data-ttu-id="df4d9-102">「接続タイプ」の複合型 ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="df4d9-102">Connection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="df4d9-103">型情報</span><span class="sxs-lookup"><span data-stu-id="df4d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df4d9-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="df4d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="df4d9-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="df4d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="df4d9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="df4d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="df4d9-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="df4d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="df4d9-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="df4d9-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df4d9-109">定義</span><span class="sxs-lookup"><span data-stu-id="df4d9-109">Definition</span></span>

```XML
          <xs:complexType name="Connection_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ConnectionRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df4d9-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="df4d9-110">Elements and attributes</span></span>

<span data-ttu-id="df4d9-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="df4d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="df4d9-112">子要素</span><span class="sxs-lookup"><span data-stu-id="df4d9-112">Child elements</span></span>

|<span data-ttu-id="df4d9-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="df4d9-113">**Element**</span></span>|<span data-ttu-id="df4d9-114">**型**</span><span class="sxs-lookup"><span data-stu-id="df4d9-114">**Type**</span></span>|<span data-ttu-id="df4d9-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="df4d9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df4d9-116">Row</span><span class="sxs-lookup"><span data-stu-id="df4d9-116">Row</span></span>](row-element-connection-sectionvisio-xml.md) <br/> |[<span data-ttu-id="df4d9-117">ConnectionRow_Type</span><span class="sxs-lookup"><span data-stu-id="df4d9-117">ConnectionRow_Type</span></span>](connectionrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="df4d9-118">属性</span><span class="sxs-lookup"><span data-stu-id="df4d9-118">Attributes</span></span>

<span data-ttu-id="df4d9-119">なし。</span><span class="sxs-lookup"><span data-stu-id="df4d9-119">None.</span></span>
  

