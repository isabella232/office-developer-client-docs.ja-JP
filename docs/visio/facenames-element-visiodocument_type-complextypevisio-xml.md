---
title: FaceNames 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: フォント名の要素のコレクションが含まれています。
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386818"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="91c20-103">FaceNames 要素 (VisioDocument_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="91c20-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="91c20-104">**フォント名**の要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="91c20-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="91c20-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="91c20-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91c20-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="91c20-106">**Element type**</span></span> <br/> |[<span data-ttu-id="91c20-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="91c20-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="91c20-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="91c20-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="91c20-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="91c20-109">**Schema file**</span></span> <br/> |<span data-ttu-id="91c20-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="91c20-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="91c20-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="91c20-111">**Document parts**</span></span> <br/> |<span data-ttu-id="91c20-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="91c20-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="91c20-113">定義</span><span class="sxs-lookup"><span data-stu-id="91c20-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="91c20-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="91c20-114">Elements and attributes</span></span>

<span data-ttu-id="91c20-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91c20-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="91c20-116">親要素</span><span class="sxs-lookup"><span data-stu-id="91c20-116">Parent elements</span></span>

|<span data-ttu-id="91c20-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="91c20-117">**Element**</span></span>|<span data-ttu-id="91c20-118">**型**</span><span class="sxs-lookup"><span data-stu-id="91c20-118">**Type**</span></span>|<span data-ttu-id="91c20-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="91c20-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91c20-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="91c20-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="91c20-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="91c20-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="91c20-122">Microsoft Visio ドキュメントのルート要素です。</span><span class="sxs-lookup"><span data-stu-id="91c20-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="91c20-123">子要素</span><span class="sxs-lookup"><span data-stu-id="91c20-123">Child elements</span></span>

|<span data-ttu-id="91c20-124">**要素**</span><span class="sxs-lookup"><span data-stu-id="91c20-124">**Element**</span></span>|<span data-ttu-id="91c20-125">**型**</span><span class="sxs-lookup"><span data-stu-id="91c20-125">**Type**</span></span>|<span data-ttu-id="91c20-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="91c20-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91c20-127">フォント名</span><span class="sxs-lookup"><span data-stu-id="91c20-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="91c20-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="91c20-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="91c20-129">フォントに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="91c20-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="91c20-130">属性</span><span class="sxs-lookup"><span data-stu-id="91c20-130">Attributes</span></span>

<span data-ttu-id="91c20-131">なし。</span><span class="sxs-lookup"><span data-stu-id="91c20-131">None.</span></span>
  

