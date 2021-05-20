---
title: PageSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 01112db1465eece9ecf5faf200a1d866ce6e332d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540589"
---
# <a name="pagesheet_type-complextype-visio-xml"></a><span data-ttu-id="eb6da-102">PageSheet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="eb6da-102">PageSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="eb6da-103">型情報</span><span class="sxs-lookup"><span data-stu-id="eb6da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb6da-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eb6da-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eb6da-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="eb6da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eb6da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="eb6da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eb6da-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="eb6da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eb6da-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="eb6da-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb6da-109">定義</span><span class="sxs-lookup"><span data-stu-id="eb6da-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eb6da-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="eb6da-110">Elements and attributes</span></span>

<span data-ttu-id="eb6da-111">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb6da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eb6da-112">子要素</span><span class="sxs-lookup"><span data-stu-id="eb6da-112">Child elements</span></span>

<span data-ttu-id="eb6da-113">なし。</span><span class="sxs-lookup"><span data-stu-id="eb6da-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb6da-114">属性</span><span class="sxs-lookup"><span data-stu-id="eb6da-114">Attributes</span></span>

|<span data-ttu-id="eb6da-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="eb6da-115">**Attribute**</span></span>|<span data-ttu-id="eb6da-116">**型**</span><span class="sxs-lookup"><span data-stu-id="eb6da-116">**Type**</span></span>|<span data-ttu-id="eb6da-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="eb6da-117">**Required**</span></span>|<span data-ttu-id="eb6da-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb6da-118">**Description**</span></span>|<span data-ttu-id="eb6da-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="eb6da-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eb6da-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="eb6da-120">UniqueID</span></span>  <br/> |<span data-ttu-id="eb6da-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="eb6da-121">xsd:string</span></span>  <br/> |<span data-ttu-id="eb6da-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="eb6da-122">optional</span></span>  <br/> ||<span data-ttu-id="eb6da-123">xsd:string 型の値。</span><span class="sxs-lookup"><span data-stu-id="eb6da-123">Values of the xsd:string type.</span></span>  <br/> |
   

