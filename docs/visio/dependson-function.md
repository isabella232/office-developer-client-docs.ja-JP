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
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805212"
---
# <a name="dependson-function"></a><span data-ttu-id="98a9d-103">DEPENDSON 関数</span><span class="sxs-lookup"><span data-stu-id="98a9d-103">DEPENDSON Function</span></span>

<span data-ttu-id="98a9d-104">セル参照の依存関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="98a9d-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="98a9d-105">構文</span><span class="sxs-lookup"><span data-stu-id="98a9d-105">Syntax</span></span>

<span data-ttu-id="98a9d-106">DEPENDSON (* * *cellref* * * [、* * *cellref2* * *,...])</span><span class="sxs-lookup"><span data-stu-id="98a9d-106">DEPENDSON(** *cellref* ** [, ** *cellref2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="98a9d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98a9d-107">Parameters</span></span>

|<span data-ttu-id="98a9d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="98a9d-108">**Name**</span></span>|<span data-ttu-id="98a9d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="98a9d-109">**Required/Optional**</span></span>|<span data-ttu-id="98a9d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="98a9d-110">**Data Type**</span></span>|<span data-ttu-id="98a9d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="98a9d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="98a9d-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="98a9d-112">_cellref_</span></span> <br/> |<span data-ttu-id="98a9d-113">必須</span><span class="sxs-lookup"><span data-stu-id="98a9d-113">Required</span></span>  <br/> |<span data-ttu-id="98a9d-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="98a9d-114">**String**</span></span> <br/> |<span data-ttu-id="98a9d-115">最初のセル参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="98a9d-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="98a9d-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="98a9d-116">_cellref2_</span></span> <br/> |<span data-ttu-id="98a9d-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="98a9d-117">Optional</span></span>  <br/> |<span data-ttu-id="98a9d-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="98a9d-118">**String**</span></span> <br/> |<span data-ttu-id="98a9d-119">2 番目のセル参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="98a9d-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98a9d-120">注釈</span><span class="sxs-lookup"><span data-stu-id="98a9d-120">Remarks</span></span>

<span data-ttu-id="98a9d-p101">この関数は常に FALSE を返します。[Event] 行または [Action] セルで使用した場合には効果がありません。</span><span class="sxs-lookup"><span data-stu-id="98a9d-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="98a9d-123">例</span><span class="sxs-lookup"><span data-stu-id="98a9d-123">Example</span></span>

<span data-ttu-id="98a9d-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="98a9d-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="98a9d-125">図形の [PinX] または [PinY] セルが変更された場合に必ず、図形のテキスト ブロックを開きます。</span><span class="sxs-lookup"><span data-stu-id="98a9d-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

