---
title: USE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: 行パターン、塗りつぶしパターン、または LinePattern、FillPattern、BeginArrow、または [endarrow] セルに格納するときの図形に名前と呼ばれる線の端点を適用します。
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806732"
---
# <a name="use-function"></a><span data-ttu-id="b5599-103">USE 関数</span><span class="sxs-lookup"><span data-stu-id="b5599-103">USE Function</span></span>

<span data-ttu-id="b5599-104">行パターン、塗りつぶしパターン、または LinePattern、FillPattern、BeginArrow、または [endarrow] セルに格納するときの図形に_名前_と呼ばれる線の端点を適用します。</span><span class="sxs-lookup"><span data-stu-id="b5599-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b5599-105">構文</span><span class="sxs-lookup"><span data-stu-id="b5599-105">Syntax</span></span>

<span data-ttu-id="b5599-106">使用 ("* **名前** *")</span><span class="sxs-lookup"><span data-stu-id="b5599-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b5599-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b5599-107">Parameters</span></span>

|<span data-ttu-id="b5599-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b5599-108">**Name**</span></span>|<span data-ttu-id="b5599-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b5599-109">**Required/Optional**</span></span>|<span data-ttu-id="b5599-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b5599-110">**Data Type**</span></span>|<span data-ttu-id="b5599-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5599-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b5599-112">_name_</span><span class="sxs-lookup"><span data-stu-id="b5599-112">_name_</span></span> <br/> |<span data-ttu-id="b5599-113">必須</span><span class="sxs-lookup"><span data-stu-id="b5599-113">Required</span></span>  <br/> |<span data-ttu-id="b5599-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="b5599-114">**String**</span></span> <br/> |<span data-ttu-id="b5599-115">有効なマスター シェイプの名前である、任意の文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5599-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b5599-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b5599-116">Return value</span></span>

<span data-ttu-id="b5599-117">数値</span><span class="sxs-lookup"><span data-stu-id="b5599-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5599-118">備考</span><span class="sxs-lookup"><span data-stu-id="b5599-118">Remarks</span></span>

<span data-ttu-id="b5599-119">_Name_という名前のマスター ドキュメントの図面ステンシル上にある場合は、行パターン、塗りつぶしパターン、矢印の始点、または矢印の終点でパターンが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b5599-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="b5599-120">この関数は常に 254 を返します。</span><span class="sxs-lookup"><span data-stu-id="b5599-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="b5599-121">例</span><span class="sxs-lookup"><span data-stu-id="b5599-121">Example</span></span>

<span data-ttu-id="b5599-122">USE("線路")</span><span class="sxs-lookup"><span data-stu-id="b5599-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="b5599-123">"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="b5599-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

