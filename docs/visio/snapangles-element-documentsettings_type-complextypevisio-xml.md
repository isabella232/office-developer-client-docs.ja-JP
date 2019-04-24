---
title: snapangles 要素 (DocumentSettings_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 803ddfc1-b7d3-736f-2d85-7b8780ef9278
description: snapangle 要素のコレクションを格納します。
ms.openlocfilehash: 8121a65505c5283ea3cc4ff93a94fdae4c64d7a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334658"
---
# <a name="snapangles-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="68da4-103">snapangles 要素 (DocumentSettings_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="68da4-103">SnapAngles element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="68da4-104">**snapangle**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="68da4-104">Contains a collection of **SnapAngle** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="68da4-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="68da4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68da4-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="68da4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68da4-107">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="68da4-107">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68da4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68da4-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68da4-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="68da4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68da4-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="68da4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68da4-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="68da4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68da4-112">文書の xml</span><span class="sxs-lookup"><span data-stu-id="68da4-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68da4-113">定義</span><span class="sxs-lookup"><span data-stu-id="68da4-113">Definition</span></span>

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68da4-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="68da4-114">Elements and attributes</span></span>

<span data-ttu-id="68da4-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="68da4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68da4-116">親要素</span><span class="sxs-lookup"><span data-stu-id="68da4-116">Parent elements</span></span>

|<span data-ttu-id="68da4-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="68da4-117">**Element**</span></span>|<span data-ttu-id="68da4-118">**型**</span><span class="sxs-lookup"><span data-stu-id="68da4-118">**Type**</span></span>|<span data-ttu-id="68da4-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="68da4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68da4-120">documentsettings</span><span class="sxs-lookup"><span data-stu-id="68da4-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68da4-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="68da4-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68da4-122">ドキュメントの設定を指定する要素を格納します。</span><span class="sxs-lookup"><span data-stu-id="68da4-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68da4-123">子要素</span><span class="sxs-lookup"><span data-stu-id="68da4-123">Child elements</span></span>

|<span data-ttu-id="68da4-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="68da4-124">**Element**</span></span>|<span data-ttu-id="68da4-125">**型**</span><span class="sxs-lookup"><span data-stu-id="68da4-125">**Type**</span></span>|<span data-ttu-id="68da4-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="68da4-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68da4-127">snapangle</span><span class="sxs-lookup"><span data-stu-id="68da4-127">SnapAngle</span></span>](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68da4-128">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="68da4-128">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68da4-129">スナップの角度を度数で指定する浮動小数点数を含みます。</span><span class="sxs-lookup"><span data-stu-id="68da4-129">Contains a floating point number that specifies a snap angle in degrees.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68da4-130">属性</span><span class="sxs-lookup"><span data-stu-id="68da4-130">Attributes</span></span>

<span data-ttu-id="68da4-131">なし。</span><span class="sxs-lookup"><span data-stu-id="68da4-131">None.</span></span>
  

