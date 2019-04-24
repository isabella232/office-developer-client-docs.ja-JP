---
title: DEPENDSON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: セル参照の依存関係を作成します。
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360235"
---
# <a name="dependson-function"></a><span data-ttu-id="e4f8a-103">DEPENDSON 関数</span><span class="sxs-lookup"><span data-stu-id="e4f8a-103">DEPENDSON Function</span></span>

<span data-ttu-id="e4f8a-104">セル参照の依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="e4f8a-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e4f8a-105">構文</span><span class="sxs-lookup"><span data-stu-id="e4f8a-105">Syntax</span></span>

<span data-ttu-id="e4f8a-106">DEPENDSON (\* \* *cellref* \* \* [, \* \* *cellref2* \* \*,...])</span><span class="sxs-lookup"><span data-stu-id="e4f8a-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e4f8a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e4f8a-107">Parameters</span></span>

|<span data-ttu-id="e4f8a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-108">**Name**</span></span>|<span data-ttu-id="e4f8a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-109">**Required/Optional**</span></span>|<span data-ttu-id="e4f8a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-110">**Data Type**</span></span>|<span data-ttu-id="e4f8a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e4f8a-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="e4f8a-112">_cellref_</span></span> <br/> |<span data-ttu-id="e4f8a-113">必須</span><span class="sxs-lookup"><span data-stu-id="e4f8a-113">Required</span></span>  <br/> |<span data-ttu-id="e4f8a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-114">**String**</span></span> <br/> |<span data-ttu-id="e4f8a-115">最初のセル参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4f8a-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="e4f8a-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="e4f8a-116">_cellref2_</span></span> <br/> |<span data-ttu-id="e4f8a-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="e4f8a-117">Optional</span></span>  <br/> |<span data-ttu-id="e4f8a-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="e4f8a-118">**String**</span></span> <br/> |<span data-ttu-id="e4f8a-119">2 番目のセル参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4f8a-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4f8a-120">解説</span><span class="sxs-lookup"><span data-stu-id="e4f8a-120">Remarks</span></span>

<span data-ttu-id="e4f8a-p101">この関数は常に FALSE を返します。[Event] 行または [Action] セルで使用した場合には効果がありません。</span><span class="sxs-lookup"><span data-stu-id="e4f8a-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e4f8a-123">例</span><span class="sxs-lookup"><span data-stu-id="e4f8a-123">Example</span></span>

<span data-ttu-id="e4f8a-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="e4f8a-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="e4f8a-125">図形の [PinX] または [PinY] セルが変更された場合に必ず、図形のテキスト ブロックを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4f8a-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

