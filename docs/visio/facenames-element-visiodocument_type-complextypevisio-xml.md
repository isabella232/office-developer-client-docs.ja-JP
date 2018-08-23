---
title: FaceNames 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: フォント名の要素のコレクションが含まれています。
ms.openlocfilehash: 1c031d589883f34bbf9d69a3d537b82e1ecf3129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805361"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="1983b-103">FaceNames 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="1983b-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1983b-104">**フォント名**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1983b-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1983b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="1983b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1983b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="1983b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1983b-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="1983b-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1983b-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="1983b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1983b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="1983b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1983b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1983b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1983b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="1983b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1983b-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="1983b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1983b-113">定義</span><span class="sxs-lookup"><span data-stu-id="1983b-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1983b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="1983b-114">Elements and attributes</span></span>

<span data-ttu-id="1983b-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1983b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1983b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="1983b-116">Parent elements</span></span>

|<span data-ttu-id="1983b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="1983b-117">**Element**</span></span>|<span data-ttu-id="1983b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="1983b-118">**Type**</span></span>|<span data-ttu-id="1983b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1983b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1983b-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="1983b-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="1983b-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="1983b-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1983b-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="1983b-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1983b-123">子要素</span><span class="sxs-lookup"><span data-stu-id="1983b-123">Child elements</span></span>

|<span data-ttu-id="1983b-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="1983b-124">**Element**</span></span>|<span data-ttu-id="1983b-125">**型**</span><span class="sxs-lookup"><span data-stu-id="1983b-125">**Type**</span></span>|<span data-ttu-id="1983b-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="1983b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1983b-127">フォント名</span><span class="sxs-lookup"><span data-stu-id="1983b-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1983b-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="1983b-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1983b-129">フォントに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1983b-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1983b-130">属性</span><span class="sxs-lookup"><span data-stu-id="1983b-130">Attributes</span></span>

<span data-ttu-id="1983b-131">なし。</span><span class="sxs-lookup"><span data-stu-id="1983b-131">None.</span></span>
  

