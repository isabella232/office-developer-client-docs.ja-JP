---
title: facenames 要素 (complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: facename 要素のコレクションを格納します。
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322583"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="3b924-103">facenames 要素 (complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3b924-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3b924-104">**facename**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="3b924-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3b924-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3b924-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b924-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3b924-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3b924-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="3b924-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3b924-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3b924-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3b924-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3b924-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3b924-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3b924-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3b924-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3b924-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3b924-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="3b924-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b924-113">定義</span><span class="sxs-lookup"><span data-stu-id="3b924-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3b924-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3b924-114">Elements and attributes</span></span>

<span data-ttu-id="3b924-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b924-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3b924-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3b924-116">Parent elements</span></span>

|<span data-ttu-id="3b924-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3b924-117">**Element**</span></span>|<span data-ttu-id="3b924-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3b924-118">**Type**</span></span>|<span data-ttu-id="3b924-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b924-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b924-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="3b924-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="3b924-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="3b924-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b924-122">Microsoft Visio 図面のルート要素です。</span><span class="sxs-lookup"><span data-stu-id="3b924-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3b924-123">子要素</span><span class="sxs-lookup"><span data-stu-id="3b924-123">Child elements</span></span>

|<span data-ttu-id="3b924-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b924-124">**Element**</span></span>|<span data-ttu-id="3b924-125">**型**</span><span class="sxs-lookup"><span data-stu-id="3b924-125">**Type**</span></span>|<span data-ttu-id="3b924-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b924-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b924-127">facename</span><span class="sxs-lookup"><span data-stu-id="3b924-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b924-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="3b924-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b924-129">フォントに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="3b924-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3b924-130">属性</span><span class="sxs-lookup"><span data-stu-id="3b924-130">Attributes</span></span>

<span data-ttu-id="3b924-131">なし。</span><span class="sxs-lookup"><span data-stu-id="3b924-131">None.</span></span>
  

