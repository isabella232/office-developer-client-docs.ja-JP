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
description: 指定した文字の数に基づいて、特定の位置を指定すると、文字列から文字数を返します。
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805903"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="5ff4b-103">MID 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5ff4b-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5ff4b-104">指定した文字の数に基づいて、特定の位置を指定すると、文字列から文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5ff4b-105">構文</span><span class="sxs-lookup"><span data-stu-id="5ff4b-105">Syntax</span></span>

<span data-ttu-id="5ff4b-106">MID (* **テキスト** *、* **開始** *、* **文字数** *)</span><span class="sxs-lookup"><span data-stu-id="5ff4b-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ff4b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5ff4b-107">Parameters</span></span>

|<span data-ttu-id="5ff4b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-108">**Name**</span></span>|<span data-ttu-id="5ff4b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-109">**Required/Optional**</span></span>|<span data-ttu-id="5ff4b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-110">**Data Type**</span></span>|<span data-ttu-id="5ff4b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ff4b-112">_text_</span><span class="sxs-lookup"><span data-stu-id="5ff4b-112">_text_</span></span> <br/> |<span data-ttu-id="5ff4b-113">必須</span><span class="sxs-lookup"><span data-stu-id="5ff4b-113">Required</span></span>  <br/> |<span data-ttu-id="5ff4b-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-114">**String**</span></span> <br/> |<span data-ttu-id="5ff4b-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="5ff4b-116">_開始位置_</span><span class="sxs-lookup"><span data-stu-id="5ff4b-116">_start_num_</span></span> <br/> |<span data-ttu-id="5ff4b-117">必須</span><span class="sxs-lookup"><span data-stu-id="5ff4b-117">Required</span></span>  <br/> |<span data-ttu-id="5ff4b-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-118">**Number**</span></span> <br/> |<span data-ttu-id="5ff4b-p101">抽出する最初の文字の位置を指定します。文字列の最初の文字位置は、1 になります。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="5ff4b-121">_文字数_</span><span class="sxs-lookup"><span data-stu-id="5ff4b-121">_num_chars_</span></span> <br/> |<span data-ttu-id="5ff4b-122">必須</span><span class="sxs-lookup"><span data-stu-id="5ff4b-122">Required</span></span>  <br/> |<span data-ttu-id="5ff4b-123">**番号**</span><span class="sxs-lookup"><span data-stu-id="5ff4b-123">**Number**</span></span> <br/> |<span data-ttu-id="5ff4b-124">取り出す文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ff4b-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5ff4b-125">Return value</span></span>

<span data-ttu-id="5ff4b-126">String</span><span class="sxs-lookup"><span data-stu-id="5ff4b-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ff4b-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="5ff4b-127">Remarks</span></span>

<span data-ttu-id="5ff4b-128">*開始位置*は、次のとおりです。 場合、</span><span class="sxs-lookup"><span data-stu-id="5ff4b-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="5ff4b-129">*テキスト*を返します。 mid 関数の長さより大きい""(空の文字列) です。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="5ff4b-130">*テキスト*の長さを超える*テキスト*が、*開始位置*と*文字*の長さよりも小さく、*テキスト*の末尾までの文字が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="5ff4b-p102">start_num が 1 より小さい場合、#VALUE! エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="5ff4b-133">*文字数*が負の場合は、#VALUE が返されます。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="5ff4b-134">エラー値です。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ff4b-135">例</span><span class="sxs-lookup"><span data-stu-id="5ff4b-135">Example</span></span>

<span data-ttu-id="5ff4b-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="5ff4b-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="5ff4b-137">999-99-9999 を返します。</span><span class="sxs-lookup"><span data-stu-id="5ff4b-137">Returns 999-99-9999.</span></span> 
  

