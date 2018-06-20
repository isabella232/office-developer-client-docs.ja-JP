---
title: TabSplitterPos 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eca75ec6-3677-54ef-74ec-4a440a089e5d
description: (図面ウィンドウの幅の合計の割合) としては、図面ウィンドウのページのタブ コントロールの幅を指定します。
ms.openlocfilehash: dff8732ad96e43627e08565927edbc11dd40df49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806602"
---
# <a name="tabsplitterpos-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="89f6c-103">TabSplitterPos 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="89f6c-103">TabSplitterPos element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="89f6c-104">(図面ウィンドウの幅の合計の割合) としては、図面ウィンドウのページのタブ コントロールの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="89f6c-104">Specifies the width of the page tab control of a drawing window (as a fraction of the total width of the drawing window).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89f6c-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="89f6c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89f6c-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="89f6c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="89f6c-107">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="89f6c-107">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="89f6c-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="89f6c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="89f6c-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="89f6c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="89f6c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="89f6c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="89f6c-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="89f6c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="89f6c-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="89f6c-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="89f6c-113">定義</span><span class="sxs-lookup"><span data-stu-id="89f6c-113">Definition</span></span>

```XML
< xs:element name="TabSplitterPos" type="TabSplitterPos_Type" minOccurs="0" maxOccurs="1" ></xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="89f6c-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="89f6c-114">Elements and attributes</span></span>

<span data-ttu-id="89f6c-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89f6c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="89f6c-116">親要素</span><span class="sxs-lookup"><span data-stu-id="89f6c-116">Parent elements</span></span>

|<span data-ttu-id="89f6c-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="89f6c-117">**Element**</span></span>|<span data-ttu-id="89f6c-118">**型**</span><span class="sxs-lookup"><span data-stu-id="89f6c-118">**Type**</span></span>|<span data-ttu-id="89f6c-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="89f6c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="89f6c-120">Window</span><span class="sxs-lookup"><span data-stu-id="89f6c-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="89f6c-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="89f6c-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="89f6c-122">Visio のインスタンスで開いているウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="89f6c-122">An open window in a Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="89f6c-123">子要素</span><span class="sxs-lookup"><span data-stu-id="89f6c-123">Child elements</span></span>

<span data-ttu-id="89f6c-124">なし。</span><span class="sxs-lookup"><span data-stu-id="89f6c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89f6c-125">属性</span><span class="sxs-lookup"><span data-stu-id="89f6c-125">Attributes</span></span>

<span data-ttu-id="89f6c-126">なし。</span><span class="sxs-lookup"><span data-stu-id="89f6c-126">None.</span></span>
  

