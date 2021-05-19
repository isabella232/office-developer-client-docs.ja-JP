---
title: ShowConnectionPoints 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f71dece-9b55-c36b-4424-f130c8d8916c
description: 接続ポイントがウィンドウに表示されるかどうかを指定します。
ms.openlocfilehash: 61dc32c0933a09118f95f8871419dd5a120468d0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34543011"
---
# <a name="showconnectionpoints-element-window_type-complextype-visio-xml"></a><span data-ttu-id="8c4b8-103">ShowConnectionPoints 要素 (Window_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8c4b8-103">ShowConnectionPoints element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8c4b8-104">接続ポイントがウィンドウに表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8c4b8-104">Specifies whether connection points are shown in a window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c4b8-105">要素の情報</span><span class="sxs-lookup"><span data-stu-id="8c4b8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c4b8-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8c4b8-107">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="8c4b8-107">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8c4b8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8c4b8-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8c4b8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8c4b8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8c4b8-111">**ドキュメント パーツ**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8c4b8-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="8c4b8-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c4b8-113">定義</span><span class="sxs-lookup"><span data-stu-id="8c4b8-113">Definition</span></span>

```XML
< xs:element name="ShowConnectionPoints" type="ShowConnectionPoints_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8c4b8-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="8c4b8-114">Elements and attributes</span></span>

<span data-ttu-id="8c4b8-115">スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c4b8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8c4b8-116">親要素</span><span class="sxs-lookup"><span data-stu-id="8c4b8-116">Parent elements</span></span>

|<span data-ttu-id="8c4b8-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-117">**Element**</span></span>|<span data-ttu-id="8c4b8-118">**型**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-118">**Type**</span></span>|<span data-ttu-id="8c4b8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="8c4b8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c4b8-120">Window</span><span class="sxs-lookup"><span data-stu-id="8c4b8-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c4b8-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="8c4b8-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8c4b8-122">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="8c4b8-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c4b8-123">子要素</span><span class="sxs-lookup"><span data-stu-id="8c4b8-123">Child elements</span></span>

<span data-ttu-id="8c4b8-124">なし。</span><span class="sxs-lookup"><span data-stu-id="8c4b8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c4b8-125">属性</span><span class="sxs-lookup"><span data-stu-id="8c4b8-125">Attributes</span></span>

<span data-ttu-id="8c4b8-126">なし。</span><span class="sxs-lookup"><span data-stu-id="8c4b8-126">None.</span></span>
  

