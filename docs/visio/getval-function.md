---
title: GETVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: セルの値を取得し、セルの値が変更されたとき、数式を再計算しません。
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805472"
---
# <a name="getval-function"></a><span data-ttu-id="6d58d-103">GETVAL 関数</span><span class="sxs-lookup"><span data-stu-id="6d58d-103">GETVAL Function</span></span>

<span data-ttu-id="6d58d-104">セルの値を取得し、セルの値が変更されたとき、数式を再計算しません。</span><span class="sxs-lookup"><span data-stu-id="6d58d-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6d58d-105">構文</span><span class="sxs-lookup"><span data-stu-id="6d58d-105">Syntax</span></span>

<span data-ttu-id="6d58d-106">GETVAL (* * *cellname* * *)</span><span class="sxs-lookup"><span data-stu-id="6d58d-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6d58d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6d58d-107">Parameters</span></span>

|<span data-ttu-id="6d58d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6d58d-108">**Name**</span></span>|<span data-ttu-id="6d58d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6d58d-109">**Required/Optional**</span></span>|<span data-ttu-id="6d58d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6d58d-110">**Data Type**</span></span>|<span data-ttu-id="6d58d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6d58d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6d58d-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="6d58d-112">_cellname_</span></span> <br/> |<span data-ttu-id="6d58d-113">必須</span><span class="sxs-lookup"><span data-stu-id="6d58d-113">Required</span></span>  <br/> |<span data-ttu-id="6d58d-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6d58d-114">**String**</span></span> <br/> |<span data-ttu-id="6d58d-115">値を取得するセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d58d-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="6d58d-116">例</span><span class="sxs-lookup"><span data-stu-id="6d58d-116">Example</span></span>

<span data-ttu-id="6d58d-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="6d58d-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="6d58d-118">[PinX]、[PinY]、[Width] の各セルの値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="6d58d-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

