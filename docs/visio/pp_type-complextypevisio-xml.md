---
title: pp_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9259b546-4a4d-81d9-4e0d-cff693d28a56
ms.openlocfilehash: 4e86d95459e7df7c8a145459c268b647e79c6a4c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539006"
---
# <a name="pptype-complextype-visio-xml"></a><span data-ttu-id="10845-102">pp_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="10845-102">pp_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="10845-103">型情報</span><span class="sxs-lookup"><span data-stu-id="10845-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10845-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="10845-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="10845-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="10845-105">**Schema file**</span></span> <br/> |<span data-ttu-id="10845-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="10845-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="10845-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="10845-107">**Extension base**</span></span> <br/> |<span data-ttu-id="10845-108">None</span><span class="sxs-lookup"><span data-stu-id="10845-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10845-109">定義</span><span class="sxs-lookup"><span data-stu-id="10845-109">Definition</span></span>

```XML
      <xs:complexType name="pp_Type">
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10845-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="10845-110">Elements and attributes</span></span>

<span data-ttu-id="10845-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="10845-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="10845-112">子要素</span><span class="sxs-lookup"><span data-stu-id="10845-112">Child elements</span></span>

<span data-ttu-id="10845-113">なし。</span><span class="sxs-lookup"><span data-stu-id="10845-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10845-114">属性</span><span class="sxs-lookup"><span data-stu-id="10845-114">Attributes</span></span>

|<span data-ttu-id="10845-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="10845-115">**Attribute**</span></span>|<span data-ttu-id="10845-116">**型**</span><span class="sxs-lookup"><span data-stu-id="10845-116">**Type**</span></span>|<span data-ttu-id="10845-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="10845-117">**Required**</span></span>|<span data-ttu-id="10845-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="10845-118">**Description**</span></span>|<span data-ttu-id="10845-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="10845-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="10845-120">IX</span><span class="sxs-lookup"><span data-stu-id="10845-120">IX</span></span>  <br/> |<span data-ttu-id="10845-121">xsd: アン Signedint</span><span class="sxs-lookup"><span data-stu-id="10845-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="10845-122">必須</span><span class="sxs-lookup"><span data-stu-id="10845-122">required</span></span>  <br/> ||<span data-ttu-id="10845-123">Xsd:/Signedint 型の値。</span><span class="sxs-lookup"><span data-stu-id="10845-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

