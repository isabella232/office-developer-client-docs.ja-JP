---
title: MID 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: 指定した文字数に基づいて、指定した位置から開始して、テキスト文字列から特定の数の文字を返します。
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360663"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="fe51e-103">MID 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="fe51e-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="fe51e-104">指定した文字数に基づいて、指定した位置から開始して、テキスト文字列から特定の数の文字を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fe51e-105">構文</span><span class="sxs-lookup"><span data-stu-id="fe51e-105">Syntax</span></span>

<span data-ttu-id="fe51e-106">MID (\* \* *text* \* *、* **開始位置** *、* \*\* \* 文字数 \* \*)</span><span class="sxs-lookup"><span data-stu-id="fe51e-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fe51e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fe51e-107">Parameters</span></span>

|<span data-ttu-id="fe51e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="fe51e-108">**Name**</span></span>|<span data-ttu-id="fe51e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="fe51e-109">**Required/Optional**</span></span>|<span data-ttu-id="fe51e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="fe51e-110">**Data Type**</span></span>|<span data-ttu-id="fe51e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fe51e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fe51e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="fe51e-112">_text_</span></span> <br/> |<span data-ttu-id="fe51e-113">必須</span><span class="sxs-lookup"><span data-stu-id="fe51e-113">Required</span></span>  <br/> |<span data-ttu-id="fe51e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="fe51e-114">**String**</span></span> <br/> |<span data-ttu-id="fe51e-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="fe51e-116">_開始_</span><span class="sxs-lookup"><span data-stu-id="fe51e-116">_start_num_</span></span> <br/> |<span data-ttu-id="fe51e-117">必須</span><span class="sxs-lookup"><span data-stu-id="fe51e-117">Required</span></span>  <br/> |<span data-ttu-id="fe51e-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="fe51e-118">**Number**</span></span> <br/> |<span data-ttu-id="fe51e-119">抽出する最初の文字の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="fe51e-120">文字列の最初の文字位置は、1 になります。</span><span class="sxs-lookup"><span data-stu-id="fe51e-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="fe51e-121">_文字数_</span><span class="sxs-lookup"><span data-stu-id="fe51e-121">_num_chars_</span></span> <br/> |<span data-ttu-id="fe51e-122">必須</span><span class="sxs-lookup"><span data-stu-id="fe51e-122">Required</span></span>  <br/> |<span data-ttu-id="fe51e-123">**数値**</span><span class="sxs-lookup"><span data-stu-id="fe51e-123">**Number**</span></span> <br/> |<span data-ttu-id="fe51e-124">取り出す文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fe51e-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="fe51e-125">Return value</span></span>

<span data-ttu-id="fe51e-126">文字列</span><span class="sxs-lookup"><span data-stu-id="fe51e-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe51e-127">注釈</span><span class="sxs-lookup"><span data-stu-id="fe51e-127">Remarks</span></span>

<span data-ttu-id="fe51e-128">*開始位置*は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="fe51e-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="fe51e-129">*文字列*の長さより大きい場合、MID は "" (空の文字列) を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="fe51e-130">*文字列*の長さを超えていますが、 \*\* *開始位置*と文字数が*文字列*の長さを超えている場合、MID は*文字列*の末尾までの文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="fe51e-131">start_num が 1 より小さい場合、#VALUE!</span><span class="sxs-lookup"><span data-stu-id="fe51e-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="fe51e-132">エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-132">error value.</span></span> 
    
<span data-ttu-id="fe51e-133">文字\*\* 数が負の数である場合、MID は #VALUE を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="fe51e-134">が返されます。</span><span class="sxs-lookup"><span data-stu-id="fe51e-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="fe51e-135">例</span><span class="sxs-lookup"><span data-stu-id="fe51e-135">Example</span></span>

<span data-ttu-id="fe51e-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="fe51e-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="fe51e-137">999-99-9999 を返します。</span><span class="sxs-lookup"><span data-stu-id="fe51e-137">Returns 999-99-9999.</span></span> 
  

