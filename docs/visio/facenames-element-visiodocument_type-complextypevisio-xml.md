---
title: FaceNames 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: FaceName 要素のコレクションを含む。
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539714"
---
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="1ba6f-103">FaceNames 要素 (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1ba6f-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1ba6f-104">FaceName 要素のコレクション **を含** む。</span><span class="sxs-lookup"><span data-stu-id="1ba6f-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1ba6f-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="1ba6f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ba6f-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1ba6f-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="1ba6f-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1ba6f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1ba6f-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1ba6f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1ba6f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1ba6f-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1ba6f-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="1ba6f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1ba6f-113">定義</span><span class="sxs-lookup"><span data-stu-id="1ba6f-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1ba6f-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1ba6f-114">Elements and attributes</span></span>

<span data-ttu-id="1ba6f-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ba6f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1ba6f-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1ba6f-116">Parent elements</span></span>

|<span data-ttu-id="1ba6f-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-117">**Element**</span></span>|<span data-ttu-id="1ba6f-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-118">**Type**</span></span>|<span data-ttu-id="1ba6f-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ba6f-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="1ba6f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="1ba6f-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="1ba6f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ba6f-122">Microsoft ドキュメントのルートVisioです。</span><span class="sxs-lookup"><span data-stu-id="1ba6f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ba6f-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1ba6f-123">Child elements</span></span>

|<span data-ttu-id="1ba6f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-124">**Element**</span></span>|<span data-ttu-id="1ba6f-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-125">**Type**</span></span>|<span data-ttu-id="1ba6f-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1ba6f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ba6f-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="1ba6f-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1ba6f-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="1ba6f-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1ba6f-129">フォントに関する情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1ba6f-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1ba6f-130">属性</span><span class="sxs-lookup"><span data-stu-id="1ba6f-130">Attributes</span></span>

<span data-ttu-id="1ba6f-131">なし。</span><span class="sxs-lookup"><span data-stu-id="1ba6f-131">None.</span></span>
  

