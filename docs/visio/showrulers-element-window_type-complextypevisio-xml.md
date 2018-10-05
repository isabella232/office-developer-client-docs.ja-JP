---
title: ShowRulers 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bb5667b9-22d6-5913-a170-626f8c93e2f9
description: ルーラーが図面ウィンドウに表示されるかどうかを指定します。
ms.openlocfilehash: 96d50e1ad6f14ff192906c38f845dfa3881eca1d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386741"
---
# <a name="showrulers-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="a3c5e-103">ShowRulers 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="a3c5e-103">ShowRulers element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a3c5e-104">ルーラーが図面ウィンドウに表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a3c5e-104">Specifies whether rulers are shown in the drawing window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3c5e-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="a3c5e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3c5e-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a3c5e-107">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="a3c5e-107">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a3c5e-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a3c5e-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a3c5e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a3c5e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a3c5e-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a3c5e-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="a3c5e-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a3c5e-113">定義</span><span class="sxs-lookup"><span data-stu-id="a3c5e-113">Definition</span></span>

```XML
< xs:element name="ShowRulers" type="ShowRulers_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a3c5e-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="a3c5e-114">Elements and attributes</span></span>

<span data-ttu-id="a3c5e-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3c5e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a3c5e-116">親要素</span><span class="sxs-lookup"><span data-stu-id="a3c5e-116">Parent elements</span></span>

|<span data-ttu-id="a3c5e-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-117">**Element**</span></span>|<span data-ttu-id="a3c5e-118">**型**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-118">**Type**</span></span>|<span data-ttu-id="a3c5e-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="a3c5e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a3c5e-120">Window</span><span class="sxs-lookup"><span data-stu-id="a3c5e-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a3c5e-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="a3c5e-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a3c5e-122">Microsoft Visio インスタンスで開いているウィンドウを表します。
</span><span class="sxs-lookup"><span data-stu-id="a3c5e-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3c5e-123">子要素</span><span class="sxs-lookup"><span data-stu-id="a3c5e-123">Child elements</span></span>

<span data-ttu-id="a3c5e-124">なし。</span><span class="sxs-lookup"><span data-stu-id="a3c5e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3c5e-125">属性</span><span class="sxs-lookup"><span data-stu-id="a3c5e-125">Attributes</span></span>

<span data-ttu-id="a3c5e-126">なし。</span><span class="sxs-lookup"><span data-stu-id="a3c5e-126">None.</span></span>
  

