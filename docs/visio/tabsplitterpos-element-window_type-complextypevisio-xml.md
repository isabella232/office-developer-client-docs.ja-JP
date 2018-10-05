---
title: TabSplitterPos 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eca75ec6-3677-54ef-74ec-4a440a089e5d
description: (図面ウィンドウの幅の合計の割合) としては、図面ウィンドウのページのタブ コントロールの幅を指定します。
ms.openlocfilehash: 0d30c151b8ad928f271ff2d8a6332755d11a562b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390643"
---
# <a name="tabsplitterpos-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="e3e06-103">TabSplitterPos 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="e3e06-103">TabSplitterPos element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e3e06-104">(図面ウィンドウの幅の合計の割合) としては、図面ウィンドウのページのタブ コントロールの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3e06-104">Specifies the width of the page tab control of a drawing window (as a fraction of the total width of the drawing window).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3e06-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="e3e06-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3e06-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="e3e06-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e3e06-107">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="e3e06-107">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e3e06-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="e3e06-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e3e06-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="e3e06-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e3e06-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e3e06-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e3e06-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="e3e06-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e3e06-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="e3e06-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e3e06-113">定義</span><span class="sxs-lookup"><span data-stu-id="e3e06-113">Definition</span></span>

```XML
< xs:element name="TabSplitterPos" type="TabSplitterPos_Type" minOccurs="0" maxOccurs="1" ></xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e3e06-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="e3e06-114">Elements and attributes</span></span>

<span data-ttu-id="e3e06-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e3e06-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e3e06-116">親要素</span><span class="sxs-lookup"><span data-stu-id="e3e06-116">Parent elements</span></span>

|<span data-ttu-id="e3e06-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="e3e06-117">**Element**</span></span>|<span data-ttu-id="e3e06-118">**型**</span><span class="sxs-lookup"><span data-stu-id="e3e06-118">**Type**</span></span>|<span data-ttu-id="e3e06-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="e3e06-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e3e06-120">Window</span><span class="sxs-lookup"><span data-stu-id="e3e06-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e3e06-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="e3e06-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e3e06-122">Visio のインスタンスで開いているウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="e3e06-122">An open window in a Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e3e06-123">子要素</span><span class="sxs-lookup"><span data-stu-id="e3e06-123">Child elements</span></span>

<span data-ttu-id="e3e06-124">なし。</span><span class="sxs-lookup"><span data-stu-id="e3e06-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3e06-125">属性</span><span class="sxs-lookup"><span data-stu-id="e3e06-125">Attributes</span></span>

<span data-ttu-id="e3e06-126">なし。</span><span class="sxs-lookup"><span data-stu-id="e3e06-126">None.</span></span>
  

