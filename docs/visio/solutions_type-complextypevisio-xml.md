---
title: Solutions_Type complexType'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: 69c5bf92bb9f72e9969f9687b42b9d583eb2a523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806545"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="1d8db-102">Solutions_Type complexType'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1d8db-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1d8db-103">型情報</span><span class="sxs-lookup"><span data-stu-id="1d8db-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d8db-104">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1d8db-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1d8db-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1d8db-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1d8db-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1d8db-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1d8db-107">**拡張機能の基本**</span><span class="sxs-lookup"><span data-stu-id="1d8db-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1d8db-108">なし</span><span class="sxs-lookup"><span data-stu-id="1d8db-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d8db-109">定義</span><span class="sxs-lookup"><span data-stu-id="1d8db-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d8db-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1d8db-110">Elements and attributes</span></span>

<span data-ttu-id="1d8db-111">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d8db-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1d8db-112">子要素</span><span class="sxs-lookup"><span data-stu-id="1d8db-112">Child elements</span></span>

|<span data-ttu-id="1d8db-113">**要素**</span><span class="sxs-lookup"><span data-stu-id="1d8db-113">**Element**</span></span>|<span data-ttu-id="1d8db-114">**型**</span><span class="sxs-lookup"><span data-stu-id="1d8db-114">**Type**</span></span>|<span data-ttu-id="1d8db-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="1d8db-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d8db-116">Solution</span><span class="sxs-lookup"><span data-stu-id="1d8db-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d8db-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="1d8db-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1d8db-118">属性</span><span class="sxs-lookup"><span data-stu-id="1d8db-118">Attributes</span></span>

<span data-ttu-id="1d8db-119">なし。</span><span class="sxs-lookup"><span data-stu-id="1d8db-119">None.</span></span>
  

