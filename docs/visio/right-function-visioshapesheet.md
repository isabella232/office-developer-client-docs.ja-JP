---
title: RIGHT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: 指定した文字数に基づいて、文字列内の最後の文字または文字を返します。
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411457"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="a7575-103">RIGHT 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a7575-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a7575-104">指定した文字数に基づいて、文字列内の最後の文字または文字を返します。</span><span class="sxs-lookup"><span data-stu-id="a7575-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a7575-105">構文</span><span class="sxs-lookup"><span data-stu-id="a7575-105">Syntax</span></span>

<span data-ttu-id="a7575-106">RIGHT (\* \* *text* \* \* [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="a7575-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7575-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a7575-107">Parameters</span></span>

|<span data-ttu-id="a7575-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a7575-108">**Name**</span></span>|<span data-ttu-id="a7575-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a7575-109">**Required/Optional**</span></span>|<span data-ttu-id="a7575-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a7575-110">**Data Type**</span></span>|<span data-ttu-id="a7575-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a7575-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7575-112">_text_</span><span class="sxs-lookup"><span data-stu-id="a7575-112">_text_</span></span> <br/> |<span data-ttu-id="a7575-113">必須</span><span class="sxs-lookup"><span data-stu-id="a7575-113">Required</span></span>  <br/> |<span data-ttu-id="a7575-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a7575-114">**String**</span></span> <br/> | <span data-ttu-id="a7575-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7575-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="a7575-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="a7575-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="a7575-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="a7575-117">Optional</span></span>  <br/> |<span data-ttu-id="a7575-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="a7575-118">**Number**</span></span> <br/> |<span data-ttu-id="a7575-119">抽出する文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7575-119">The number of characters you want to extract.</span></span> <span data-ttu-id="a7575-120">既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="a7575-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a7575-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a7575-121">Return value</span></span>

<span data-ttu-id="a7575-122">文字列</span><span class="sxs-lookup"><span data-stu-id="a7575-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7575-123">注釈</span><span class="sxs-lookup"><span data-stu-id="a7575-123">Remarks</span></span>

<span data-ttu-id="a7575-124">_num_chars_opt_の値は、ゼロ (0) 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7575-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="a7575-125">_num_chars_opt_がテキストの長さを超える場合は、すべてのテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="a7575-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="a7575-126">_num_chars_opt_を省略すると、1を指定したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="a7575-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a7575-127">例</span><span class="sxs-lookup"><span data-stu-id="a7575-127">Example</span></span>

<span data-ttu-id="a7575-128">RIGHT ("January 1, 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="a7575-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="a7575-129">値 2004 を返します。</span><span class="sxs-lookup"><span data-stu-id="a7575-129">Returns the value 2004.</span></span> 
  

