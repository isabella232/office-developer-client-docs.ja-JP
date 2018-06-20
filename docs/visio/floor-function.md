---
title: FLOOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: または複数の次のインスタンスを次の整数には、数値を 0 (ゼロ) を四捨五入します。
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805397"
---
# <a name="floor-function"></a><span data-ttu-id="95b6b-103">FLOOR 関数</span><span class="sxs-lookup"><span data-stu-id="95b6b-103">FLOOR Function</span></span>

<span data-ttu-id="95b6b-104">次の整数、または_複数_の次のインスタンスには、数値を 0 (ゼロ) を丸めます。</span><span class="sxs-lookup"><span data-stu-id="95b6b-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="95b6b-105">構文</span><span class="sxs-lookup"><span data-stu-id="95b6b-105">Syntax</span></span>

<span data-ttu-id="95b6b-106">フロア (* **番号** *、* **複数** *)</span><span class="sxs-lookup"><span data-stu-id="95b6b-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95b6b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="95b6b-107">Parameters</span></span>

|<span data-ttu-id="95b6b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="95b6b-108">**Name**</span></span>|<span data-ttu-id="95b6b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="95b6b-109">**Required/Optional**</span></span>|<span data-ttu-id="95b6b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="95b6b-110">**Data Type**</span></span>|<span data-ttu-id="95b6b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="95b6b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95b6b-112">_number_</span><span class="sxs-lookup"><span data-stu-id="95b6b-112">_number_</span></span> <br/> |<span data-ttu-id="95b6b-113">必須</span><span class="sxs-lookup"><span data-stu-id="95b6b-113">Required</span></span>  <br/> |<span data-ttu-id="95b6b-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="95b6b-114">**Number**</span></span> <br/> |<span data-ttu-id="95b6b-115">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="95b6b-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="95b6b-116">_複数_</span><span class="sxs-lookup"><span data-stu-id="95b6b-116">_multiple_</span></span> <br/> |<span data-ttu-id="95b6b-117">必須</span><span class="sxs-lookup"><span data-stu-id="95b6b-117">Required</span></span>  <br/> |<span data-ttu-id="95b6b-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="95b6b-118">**Number**</span></span> <br/> |<span data-ttu-id="95b6b-119">切り上げの対象となる倍数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="95b6b-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="95b6b-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="95b6b-120">Return value</span></span>

<span data-ttu-id="95b6b-121">数値</span><span class="sxs-lookup"><span data-stu-id="95b6b-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95b6b-122">備考</span><span class="sxs-lookup"><span data-stu-id="95b6b-122">Remarks</span></span>

<span data-ttu-id="95b6b-123">_複数_を指定しない場合、数は、次の整数を 0 方向に丸めます。</span><span class="sxs-lookup"><span data-stu-id="95b6b-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="95b6b-124">_番号_と_複数_は、同一の記号、または、#NUM を持つ必要があります!</span><span class="sxs-lookup"><span data-stu-id="95b6b-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="95b6b-125">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="95b6b-125">error is returned.</span></span> <span data-ttu-id="95b6b-126">#Value! の値には、_番号_または_複数_のいずれかを変換できません! 場合、</span><span class="sxs-lookup"><span data-stu-id="95b6b-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="95b6b-127">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="95b6b-127">error is returned.</span></span> <span data-ttu-id="95b6b-128">_番号_または_複数_のいずれかが 0 の場合、結果は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="95b6b-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="95b6b-129">例 1</span><span class="sxs-lookup"><span data-stu-id="95b6b-129">Example 1</span></span>

<span data-ttu-id="95b6b-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="95b6b-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="95b6b-131">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="95b6b-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="95b6b-132">例 2</span><span class="sxs-lookup"><span data-stu-id="95b6b-132">Example 2</span></span>

<span data-ttu-id="95b6b-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="95b6b-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="95b6b-134">-3 を返します。</span><span class="sxs-lookup"><span data-stu-id="95b6b-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="95b6b-135">例 3</span><span class="sxs-lookup"><span data-stu-id="95b6b-135">Example 3</span></span>

<span data-ttu-id="95b6b-136">フロア (3.7, 0.5)</span><span class="sxs-lookup"><span data-stu-id="95b6b-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="95b6b-137">3.5 を返します。</span><span class="sxs-lookup"><span data-stu-id="95b6b-137">Returns 3.5.</span></span>
  

