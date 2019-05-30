---
title: FooterMargin_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f5838855a5c21b699c7a81849b9afc40790f3d01
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538642"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="11179-102">FooterMargin_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="11179-102">FooterMargin_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="11179-103">型情報</span><span class="sxs-lookup"><span data-stu-id="11179-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11179-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11179-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="11179-105">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="11179-105">**Schema file**</span></span> <br/> |<span data-ttu-id="11179-106">VisioSchema15-06-05</span><span class="sxs-lookup"><span data-stu-id="11179-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="11179-107">**拡張ベース**</span><span class="sxs-lookup"><span data-stu-id="11179-107">**Extension base**</span></span> <br/> |<span data-ttu-id="11179-108">xsd: double</span><span class="sxs-lookup"><span data-stu-id="11179-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="11179-109">定義</span><span class="sxs-lookup"><span data-stu-id="11179-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="11179-110">要素と属性</span><span class="sxs-lookup"><span data-stu-id="11179-110">Elements and attributes</span></span>

<span data-ttu-id="11179-111">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="11179-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="11179-112">子要素</span><span class="sxs-lookup"><span data-stu-id="11179-112">Child elements</span></span>

<span data-ttu-id="11179-113">なし。</span><span class="sxs-lookup"><span data-stu-id="11179-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11179-114">属性</span><span class="sxs-lookup"><span data-stu-id="11179-114">Attributes</span></span>

|<span data-ttu-id="11179-115">**属性**</span><span class="sxs-lookup"><span data-stu-id="11179-115">**Attribute**</span></span>|<span data-ttu-id="11179-116">**型**</span><span class="sxs-lookup"><span data-stu-id="11179-116">**Type**</span></span>|<span data-ttu-id="11179-117">**必須**</span><span class="sxs-lookup"><span data-stu-id="11179-117">**Required**</span></span>|<span data-ttu-id="11179-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="11179-118">**Description**</span></span>|<span data-ttu-id="11179-119">**可能な値**</span><span class="sxs-lookup"><span data-stu-id="11179-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="11179-120">単位</span><span class="sxs-lookup"><span data-stu-id="11179-120">Unit</span></span>  <br/> |<span data-ttu-id="11179-121">xsd: string</span><span class="sxs-lookup"><span data-stu-id="11179-121">xsd:string</span></span>  <br/> |<span data-ttu-id="11179-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="11179-122">optional</span></span>  <br/> ||<span data-ttu-id="11179-123">Xsd: string 型の値。</span><span class="sxs-lookup"><span data-stu-id="11179-123">Values of the xsd:string type.</span></span>  <br/> |
   

