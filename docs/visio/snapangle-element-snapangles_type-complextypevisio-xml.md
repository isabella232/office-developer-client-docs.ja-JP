---
title: snapangle 要素 (SnapAngles_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d4f93fc5-80fb-3195-d25b-9a407de7848e
description: スナップの角度を度数で指定する浮動小数点数を含みます。
ms.openlocfilehash: c283be7d613c574d60412f645271d2c947ae0ffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270064"
---
# <a name="snapangle-element-snapanglestype-complextype-visio-xml"></a><span data-ttu-id="3cb5b-103">snapangle 要素 (SnapAngles_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="3cb5b-103">SnapAngle element (SnapAngles_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3cb5b-104">スナップの角度を度数で指定する浮動小数点数を含みます。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-104">Contains a floating point number that specifies a snap angle in degrees.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3cb5b-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="3cb5b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cb5b-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3cb5b-107">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="3cb5b-107">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3cb5b-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3cb5b-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3cb5b-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="3cb5b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3cb5b-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3cb5b-112">文書 .xml、windows .xml</span><span class="sxs-lookup"><span data-stu-id="3cb5b-112">document.xml, windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3cb5b-113">定義</span><span class="sxs-lookup"><span data-stu-id="3cb5b-113">Definition</span></span>

```XML
< xs:element name="SnapAngle" type="SnapAngle_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3cb5b-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="3cb5b-114">Elements and attributes</span></span>

<span data-ttu-id="3cb5b-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3cb5b-116">親要素</span><span class="sxs-lookup"><span data-stu-id="3cb5b-116">Parent elements</span></span>

|<span data-ttu-id="3cb5b-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-117">**Element**</span></span>|<span data-ttu-id="3cb5b-118">**型**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-118">**Type**</span></span>|<span data-ttu-id="3cb5b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="3cb5b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3cb5b-120">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="3cb5b-120">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3cb5b-121">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="3cb5b-121">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3cb5b-122">**snapangle**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-122">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
|[<span data-ttu-id="3cb5b-123">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="3cb5b-123">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3cb5b-124">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="3cb5b-124">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3cb5b-125">**snapangle**要素のコレクションを格納します。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-125">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3cb5b-126">子要素</span><span class="sxs-lookup"><span data-stu-id="3cb5b-126">Child elements</span></span>

<span data-ttu-id="3cb5b-127">なし。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-127">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3cb5b-128">属性</span><span class="sxs-lookup"><span data-stu-id="3cb5b-128">Attributes</span></span>

<span data-ttu-id="3cb5b-129">なし。</span><span class="sxs-lookup"><span data-stu-id="3cb5b-129">None.</span></span>
  

