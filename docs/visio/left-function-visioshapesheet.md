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
description: 指定した文字数に基づいて、文字列の左端の文字または文字列を返します。
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805686"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="d89b0-103">LEFT 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="d89b0-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="d89b0-104">指定した文字数に基づいて、文字列の左端の文字または文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d89b0-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d89b0-105">構文</span><span class="sxs-lookup"><span data-stu-id="d89b0-105">Syntax</span></span>

<span data-ttu-id="d89b0-106">左 (* **テキスト** *、[、* * *num_chars_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="d89b0-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d89b0-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d89b0-107">Parameters</span></span>

|<span data-ttu-id="d89b0-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d89b0-108">**Name**</span></span>|<span data-ttu-id="d89b0-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d89b0-109">**Required/Optional**</span></span>|<span data-ttu-id="d89b0-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d89b0-110">**Data Type**</span></span>|<span data-ttu-id="d89b0-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d89b0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d89b0-112">_text_</span><span class="sxs-lookup"><span data-stu-id="d89b0-112">_text_</span></span> <br/> |<span data-ttu-id="d89b0-113">必須</span><span class="sxs-lookup"><span data-stu-id="d89b0-113">Required</span></span>  <br/> |<span data-ttu-id="d89b0-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d89b0-114">**String**</span></span> <br/> |<span data-ttu-id="d89b0-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="d89b0-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="d89b0-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="d89b0-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="d89b0-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="d89b0-117">Optional</span></span>  <br/> |<span data-ttu-id="d89b0-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="d89b0-118">**Numeric**</span></span> <br/> |<span data-ttu-id="d89b0-119">抽出する文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d89b0-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d89b0-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d89b0-120">Return value</span></span>

<span data-ttu-id="d89b0-121">String</span><span class="sxs-lookup"><span data-stu-id="d89b0-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d89b0-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="d89b0-122">Remarks</span></span>

<span data-ttu-id="d89b0-123">_Num_chars_opt_の値は、以上のゼロ (0) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d89b0-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="d89b0-124">_Num_chars_opt_が文字列の長さよりも大きい場合は、左側がすべてのテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="d89b0-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="d89b0-125">_Num_chars_opt_が省略された場合は 1 であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="d89b0-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d89b0-126">例</span><span class="sxs-lookup"><span data-stu-id="d89b0-126">Example</span></span>

<span data-ttu-id="d89b0-127">LEFT ("January 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="d89b0-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="d89b0-128">値 "Jan" を返します。</span><span class="sxs-lookup"><span data-stu-id="d89b0-128">Returns the value "Jan".</span></span> 
  

