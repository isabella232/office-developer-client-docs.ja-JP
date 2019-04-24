---
title: LEFT 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: 指定した文字数に基づいて、文字列内の左端の文字または文字を返します。
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309465"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="61509-103">LEFT 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="61509-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="61509-104">指定した文字数に基づいて、文字列内の左端の文字または文字を返します。</span><span class="sxs-lookup"><span data-stu-id="61509-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="61509-105">構文</span><span class="sxs-lookup"><span data-stu-id="61509-105">Syntax</span></span>

<span data-ttu-id="61509-106">LEFT (\* \* *text* \* \*, [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="61509-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="61509-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="61509-107">Parameters</span></span>

|<span data-ttu-id="61509-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="61509-108">**Name**</span></span>|<span data-ttu-id="61509-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="61509-109">**Required/Optional**</span></span>|<span data-ttu-id="61509-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="61509-110">**Data Type**</span></span>|<span data-ttu-id="61509-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="61509-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="61509-112">_text_</span><span class="sxs-lookup"><span data-stu-id="61509-112">_text_</span></span> <br/> |<span data-ttu-id="61509-113">必須</span><span class="sxs-lookup"><span data-stu-id="61509-113">Required</span></span>  <br/> |<span data-ttu-id="61509-114">**String**</span><span class="sxs-lookup"><span data-stu-id="61509-114">**String**</span></span> <br/> |<span data-ttu-id="61509-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="61509-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="61509-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="61509-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="61509-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="61509-117">Optional</span></span>  <br/> |<span data-ttu-id="61509-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="61509-118">**Numeric**</span></span> <br/> |<span data-ttu-id="61509-119">抽出する文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="61509-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="61509-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="61509-120">Return value</span></span>

<span data-ttu-id="61509-121">文字列</span><span class="sxs-lookup"><span data-stu-id="61509-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61509-122">注釈</span><span class="sxs-lookup"><span data-stu-id="61509-122">Remarks</span></span>

<span data-ttu-id="61509-123">_num_chars_opt_の値は、ゼロ (0) 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="61509-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="61509-124">_num_chars_opt_がテキストの長さより大きい場合は、すべてのテキストが返されます。</span><span class="sxs-lookup"><span data-stu-id="61509-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="61509-125">_num_chars_opt_を省略すると、1を指定したと見なされます。</span><span class="sxs-lookup"><span data-stu-id="61509-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="61509-126">例</span><span class="sxs-lookup"><span data-stu-id="61509-126">Example</span></span>

<span data-ttu-id="61509-127">LEFT ("January 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="61509-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="61509-128">値 "Jan" を返します。</span><span class="sxs-lookup"><span data-stu-id="61509-128">Returns the value "Jan".</span></span> 
  

