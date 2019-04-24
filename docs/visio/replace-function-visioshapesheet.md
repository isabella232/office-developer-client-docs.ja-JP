---
title: REPLACE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: 指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320161"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="0c11b-103">REPLACE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0c11b-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0c11b-104">指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="0c11b-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0c11b-105">構文</span><span class="sxs-lookup"><span data-stu-id="0c11b-105">Syntax</span></span>

<span data-ttu-id="0c11b-106">REPLACE (\* **文字列** *、* **開始位置** *、* \*\* \* 文字数 \* *、* **置換** \*)</span><span class="sxs-lookup"><span data-stu-id="0c11b-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0c11b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c11b-107">Parameters</span></span>

|<span data-ttu-id="0c11b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0c11b-108">**Name**</span></span>|<span data-ttu-id="0c11b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0c11b-109">**Required/Optional**</span></span>|<span data-ttu-id="0c11b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0c11b-110">**Data Type**</span></span>|<span data-ttu-id="0c11b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0c11b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0c11b-112">_文字列_</span><span class="sxs-lookup"><span data-stu-id="0c11b-112">_old_text_</span></span> <br/> |<span data-ttu-id="0c11b-113">必須</span><span class="sxs-lookup"><span data-stu-id="0c11b-113">Required</span></span>  <br/> |<span data-ttu-id="0c11b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0c11b-114">**String**</span></span> <br/> |<span data-ttu-id="0c11b-115">置き換えを行う文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c11b-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="0c11b-116">_開始_</span><span class="sxs-lookup"><span data-stu-id="0c11b-116">_start_num_</span></span> <br/> |<span data-ttu-id="0c11b-117">必須</span><span class="sxs-lookup"><span data-stu-id="0c11b-117">Required</span></span>  <br/> |<span data-ttu-id="0c11b-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="0c11b-118">**Number**</span></span> <br/> |<span data-ttu-id="0c11b-119">置換する文字列の文字の__ 位置を指定します。 __</span><span class="sxs-lookup"><span data-stu-id="0c11b-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="0c11b-120">文字列の最初の文字位置は、1 になります。</span><span class="sxs-lookup"><span data-stu-id="0c11b-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="0c11b-121">_文字数_</span><span class="sxs-lookup"><span data-stu-id="0c11b-121">_num_chars_</span></span> <br/> |<span data-ttu-id="0c11b-122">必須</span><span class="sxs-lookup"><span data-stu-id="0c11b-122">Required</span></span>  <br/> |<span data-ttu-id="0c11b-123">**数値**</span><span class="sxs-lookup"><span data-stu-id="0c11b-123">**Number**</span></span> <br/> |<span data-ttu-id="0c11b-124">置換する_文字列_の文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0c11b-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="0c11b-125">_文字列_</span><span class="sxs-lookup"><span data-stu-id="0c11b-125">_new_text_</span></span> <br/> |<span data-ttu-id="0c11b-126">必須</span><span class="sxs-lookup"><span data-stu-id="0c11b-126">Required</span></span>  <br/> |<span data-ttu-id="0c11b-127">**String**</span><span class="sxs-lookup"><span data-stu-id="0c11b-127">**String**</span></span> <br/> |<span data-ttu-id="0c11b-128">文字列を置換する文字列を入力__ します。</span><span class="sxs-lookup"><span data-stu-id="0c11b-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0c11b-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="0c11b-129">Return value</span></span>

<span data-ttu-id="0c11b-130">文字列</span><span class="sxs-lookup"><span data-stu-id="0c11b-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c11b-131">注釈</span><span class="sxs-lookup"><span data-stu-id="0c11b-131">Remarks</span></span>

<span data-ttu-id="0c11b-p102">文字列内の特定の位置にある文字列を置換するときは、REPLACE 関数を使用します。文字列内の特定の文字列を置換するときは、SUBSTITUTE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c11b-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="0c11b-134">例</span><span class="sxs-lookup"><span data-stu-id="0c11b-134">Example</span></span>

<span data-ttu-id="0c11b-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="0c11b-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="0c11b-136">01/03/2003 を返します。</span><span class="sxs-lookup"><span data-stu-id="0c11b-136">Returns 01/03/2003.</span></span> 
  

