---
title: SnapAngle 要素 (SnapAngles_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d4f93fc5-80fb-3195-d25b-9a407de7848e
description: 浮動が含まれています、スナップ角度を度数で指定する番号をポイントします。
ms.openlocfilehash: c283be7d613c574d60412f645271d2c947ae0ffb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397003"
---
# <a name="snapangle-element-snapanglestype-complextype-visio-xml"></a><span data-ttu-id="61f47-103">SnapAngle 要素 (SnapAngles_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="61f47-103">SnapAngle element (SnapAngles_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="61f47-104">浮動が含まれています、スナップ角度を度数で指定する番号をポイントします。</span><span class="sxs-lookup"><span data-stu-id="61f47-104">Contains a floating point number that specifies a snap angle in degrees.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61f47-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="61f47-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61f47-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="61f47-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61f47-107">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="61f47-107">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61f47-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="61f47-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61f47-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="61f47-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61f47-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61f47-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61f47-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="61f47-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61f47-112">document.xml、windows.xml</span><span class="sxs-lookup"><span data-stu-id="61f47-112">document.xml, windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61f47-113">定義</span><span class="sxs-lookup"><span data-stu-id="61f47-113">Definition</span></span>

```XML
< xs:element name="SnapAngle" type="SnapAngle_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61f47-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="61f47-114">Elements and attributes</span></span>

<span data-ttu-id="61f47-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="61f47-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61f47-116">親要素</span><span class="sxs-lookup"><span data-stu-id="61f47-116">Parent elements</span></span>

|<span data-ttu-id="61f47-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="61f47-117">**Element**</span></span>|<span data-ttu-id="61f47-118">**型**</span><span class="sxs-lookup"><span data-stu-id="61f47-118">**Type**</span></span>|<span data-ttu-id="61f47-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="61f47-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61f47-120">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="61f47-120">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61f47-121">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="61f47-121">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61f47-122">**SnapAngle**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="61f47-122">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
|[<span data-ttu-id="61f47-123">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="61f47-123">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61f47-124">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="61f47-124">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61f47-125">**SnapAngle**要素のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="61f47-125">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61f47-126">子要素</span><span class="sxs-lookup"><span data-stu-id="61f47-126">Child elements</span></span>

<span data-ttu-id="61f47-127">なし。</span><span class="sxs-lookup"><span data-stu-id="61f47-127">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61f47-128">属性</span><span class="sxs-lookup"><span data-stu-id="61f47-128">Attributes</span></span>

<span data-ttu-id="61f47-129">なし。</span><span class="sxs-lookup"><span data-stu-id="61f47-129">None.</span></span>
  

