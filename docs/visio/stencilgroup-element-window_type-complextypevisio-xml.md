---
title: StencilGroup 要素 (Window_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40e45007-e5c3-118c-1460-af83b461b014
description: 差し込み印刷のステンシル ウィンドウのうち、ウィンドウは、メンバーのグループを指定します。
ms.openlocfilehash: bcc14e5bc685cf3dc5f6308c8cc9169f7d1b99c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806556"
---
# <a name="stencilgroup-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="b64d0-103">StencilGroup 要素 (Window_Type complexType)'Visio XML (')</span><span class="sxs-lookup"><span data-stu-id="b64d0-103">StencilGroup element (Window_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b64d0-104">差し込み印刷のステンシル ウィンドウのうち、ウィンドウは、メンバーのグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="b64d0-104">Specifies the group of merged stencil windows of which the window is a member.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b64d0-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="b64d0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b64d0-106">**要素の型**</span><span class="sxs-lookup"><span data-stu-id="b64d0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b64d0-107">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="b64d0-107">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b64d0-108">**名前空間**</span><span class="sxs-lookup"><span data-stu-id="b64d0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b64d0-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="b64d0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b64d0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b64d0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b64d0-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="b64d0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b64d0-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="b64d0-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b64d0-113">定義</span><span class="sxs-lookup"><span data-stu-id="b64d0-113">Definition</span></span>

```XML
< xs:element name="StencilGroup" type="StencilGroup_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b64d0-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="b64d0-114">Elements and attributes</span></span>

<span data-ttu-id="b64d0-115">スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b64d0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b64d0-116">親要素</span><span class="sxs-lookup"><span data-stu-id="b64d0-116">Parent elements</span></span>

|<span data-ttu-id="b64d0-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="b64d0-117">**Element**</span></span>|<span data-ttu-id="b64d0-118">**型**</span><span class="sxs-lookup"><span data-stu-id="b64d0-118">**Type**</span></span>|<span data-ttu-id="b64d0-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="b64d0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b64d0-120">Window</span><span class="sxs-lookup"><span data-stu-id="b64d0-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b64d0-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="b64d0-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b64d0-122">Microsoft Visio のインスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="b64d0-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b64d0-123">子要素</span><span class="sxs-lookup"><span data-stu-id="b64d0-123">Child elements</span></span>

<span data-ttu-id="b64d0-124">なし。</span><span class="sxs-lookup"><span data-stu-id="b64d0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b64d0-125">属性</span><span class="sxs-lookup"><span data-stu-id="b64d0-125">Attributes</span></span>

<span data-ttu-id="b64d0-126">なし。</span><span class="sxs-lookup"><span data-stu-id="b64d0-126">None.</span></span>
  

