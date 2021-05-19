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
description: 指定した文字数に基づいて、指定した位置から始まる、テキスト文字列の特定の文字数を返します。
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410267"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="82c03-103">MID 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="82c03-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="82c03-104">指定した文字数に基づいて、指定した位置から始まる、テキスト文字列の特定の文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="82c03-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="82c03-105">構文</span><span class="sxs-lookup"><span data-stu-id="82c03-105">Syntax</span></span>

<span data-ttu-id="82c03-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\*\*\* num_chars \*\* )</span><span class="sxs-lookup"><span data-stu-id="82c03-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82c03-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82c03-107">Parameters</span></span>

|<span data-ttu-id="82c03-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="82c03-108">**Name**</span></span>|<span data-ttu-id="82c03-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="82c03-109">**Required/Optional**</span></span>|<span data-ttu-id="82c03-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="82c03-110">**Data Type**</span></span>|<span data-ttu-id="82c03-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="82c03-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82c03-112">_text_</span><span class="sxs-lookup"><span data-stu-id="82c03-112">_text_</span></span> <br/> |<span data-ttu-id="82c03-113">必須</span><span class="sxs-lookup"><span data-stu-id="82c03-113">Required</span></span>  <br/> |<span data-ttu-id="82c03-114">**String**</span><span class="sxs-lookup"><span data-stu-id="82c03-114">**String**</span></span> <br/> |<span data-ttu-id="82c03-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="82c03-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="82c03-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="82c03-116">_start_num_</span></span> <br/> |<span data-ttu-id="82c03-117">必須</span><span class="sxs-lookup"><span data-stu-id="82c03-117">Required</span></span>  <br/> |<span data-ttu-id="82c03-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="82c03-118">**Number**</span></span> <br/> |<span data-ttu-id="82c03-p101">抽出する最初の文字の位置を指定します。文字列の最初の文字位置は、1 になります。</span><span class="sxs-lookup"><span data-stu-id="82c03-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="82c03-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="82c03-121">_num_chars_</span></span> <br/> |<span data-ttu-id="82c03-122">必須</span><span class="sxs-lookup"><span data-stu-id="82c03-122">Required</span></span>  <br/> |<span data-ttu-id="82c03-123">**数値**</span><span class="sxs-lookup"><span data-stu-id="82c03-123">**Number**</span></span> <br/> |<span data-ttu-id="82c03-124">取り出す文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="82c03-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="82c03-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="82c03-125">Return value</span></span>

<span data-ttu-id="82c03-126">文字列</span><span class="sxs-lookup"><span data-stu-id="82c03-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82c03-127">注釈</span><span class="sxs-lookup"><span data-stu-id="82c03-127">Remarks</span></span>

<span data-ttu-id="82c03-128">次  *start_num*  場合:</span><span class="sxs-lookup"><span data-stu-id="82c03-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="82c03-129">テキストの長さより大  *きい*  場合、MID は "" (空のテキスト) を返します。</span><span class="sxs-lookup"><span data-stu-id="82c03-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="82c03-130">テキストの長さより小さいが *、start_numテキストnum_chars* を超えると、テキストの末尾までの文字が戻 *されます*。</span><span class="sxs-lookup"><span data-stu-id="82c03-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="82c03-p102">start_num が 1 より小さい場合、#VALUE! エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="82c03-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="82c03-133">負  *num_chars*  場合、MID は値を返#VALUE!</span><span class="sxs-lookup"><span data-stu-id="82c03-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="82c03-134">が返されます。</span><span class="sxs-lookup"><span data-stu-id="82c03-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="82c03-135">例</span><span class="sxs-lookup"><span data-stu-id="82c03-135">Example</span></span>

<span data-ttu-id="82c03-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="82c03-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="82c03-137">999-99-9999 を返します。</span><span class="sxs-lookup"><span data-stu-id="82c03-137">Returns 999-99-9999.</span></span> 
  

