---
title: StencilGroupPos 要素 (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7440a59b-1c7c-6477-32e7-35188fbd2b39
description: ウィンドウ内のグループ内のステンシルの相対位置を指定する整数型 (integer) の値を格納します。
ms.openlocfilehash: a539cd4435477f43a2e9c16b6a9b77e6e1e9d7f5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538880"
---
# <a name="stencilgrouppos-element-windowtype-complextype-visio-xml"></a><span data-ttu-id="4c0fc-103">StencilGroupPos 要素 (Window_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4c0fc-103">StencilGroupPos element (Window_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4c0fc-104">ウィンドウ内のグループ内のステンシルの相対位置を指定する整数型 (integer) の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="4c0fc-104">Contains an integer that specifies the relative position of a stencil within a group in a window.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c0fc-105">要素情報</span><span class="sxs-lookup"><span data-stu-id="4c0fc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c0fc-106">**要素の種類**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4c0fc-107">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="4c0fc-107">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4c0fc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4c0fc-109">**スキーマ ファイル**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4c0fc-110">VisioSchema15</span><span class="sxs-lookup"><span data-stu-id="4c0fc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4c0fc-111">**文書パーツ**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4c0fc-112">windows .xml</span><span class="sxs-lookup"><span data-stu-id="4c0fc-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c0fc-113">定義</span><span class="sxs-lookup"><span data-stu-id="4c0fc-113">Definition</span></span>

```XML
<xs:element name="StencilGroupPos" type="StencilGroupPos_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c0fc-114">要素と属性</span><span class="sxs-lookup"><span data-stu-id="4c0fc-114">Elements and attributes</span></span>

<span data-ttu-id="4c0fc-115">スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c0fc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4c0fc-116">親要素</span><span class="sxs-lookup"><span data-stu-id="4c0fc-116">Parent elements</span></span>

|<span data-ttu-id="4c0fc-117">**要素**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-117">**Element**</span></span>|<span data-ttu-id="4c0fc-118">**型**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-118">**Type**</span></span>|<span data-ttu-id="4c0fc-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="4c0fc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c0fc-120">Window</span><span class="sxs-lookup"><span data-stu-id="4c0fc-120">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c0fc-121">Window_Type</span><span class="sxs-lookup"><span data-stu-id="4c0fc-121">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4c0fc-122">Microsoft Visio インスタンスで開いているウィンドウを表します。</span><span class="sxs-lookup"><span data-stu-id="4c0fc-122">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c0fc-123">子要素</span><span class="sxs-lookup"><span data-stu-id="4c0fc-123">Child elements</span></span>

<span data-ttu-id="4c0fc-124">なし。</span><span class="sxs-lookup"><span data-stu-id="4c0fc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c0fc-125">属性</span><span class="sxs-lookup"><span data-stu-id="4c0fc-125">Attributes</span></span>

<span data-ttu-id="4c0fc-126">なし。</span><span class="sxs-lookup"><span data-stu-id="4c0fc-126">None.</span></span>
  

