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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414355"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="5f35f-103">REPLACE 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5f35f-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5f35f-104">指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5f35f-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f35f-105">構文</span><span class="sxs-lookup"><span data-stu-id="5f35f-105">Syntax</span></span>

<span data-ttu-id="5f35f-106">REPLACE (\* **文字列** *、* **開始位置** *、* \*\* \* 文字数 \* *、* **置換** \*)</span><span class="sxs-lookup"><span data-stu-id="5f35f-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f35f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f35f-107">Parameters</span></span>

|<span data-ttu-id="5f35f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5f35f-108">**Name**</span></span>|<span data-ttu-id="5f35f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5f35f-109">**Required/Optional**</span></span>|<span data-ttu-id="5f35f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5f35f-110">**Data Type**</span></span>|<span data-ttu-id="5f35f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5f35f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f35f-112">_文字列_</span><span class="sxs-lookup"><span data-stu-id="5f35f-112">_old_text_</span></span> <br/> |<span data-ttu-id="5f35f-113">必須</span><span class="sxs-lookup"><span data-stu-id="5f35f-113">Required</span></span>  <br/> |<span data-ttu-id="5f35f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5f35f-114">**String**</span></span> <br/> |<span data-ttu-id="5f35f-115">置き換えを行う文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f35f-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="5f35f-116">_開始_</span><span class="sxs-lookup"><span data-stu-id="5f35f-116">_start_num_</span></span> <br/> |<span data-ttu-id="5f35f-117">必須</span><span class="sxs-lookup"><span data-stu-id="5f35f-117">Required</span></span>  <br/> |<span data-ttu-id="5f35f-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="5f35f-118">**Number**</span></span> <br/> |<span data-ttu-id="5f35f-119">置換する文字列の文字の__ 位置を指定します。 __</span><span class="sxs-lookup"><span data-stu-id="5f35f-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="5f35f-120">文字列の最初の文字位置は、1 になります。</span><span class="sxs-lookup"><span data-stu-id="5f35f-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="5f35f-121">_文字数_</span><span class="sxs-lookup"><span data-stu-id="5f35f-121">_num_chars_</span></span> <br/> |<span data-ttu-id="5f35f-122">必須</span><span class="sxs-lookup"><span data-stu-id="5f35f-122">Required</span></span>  <br/> |<span data-ttu-id="5f35f-123">**数値**</span><span class="sxs-lookup"><span data-stu-id="5f35f-123">**Number**</span></span> <br/> |<span data-ttu-id="5f35f-124">置換する_文字列_の文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f35f-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="5f35f-125">_文字列_</span><span class="sxs-lookup"><span data-stu-id="5f35f-125">_new_text_</span></span> <br/> |<span data-ttu-id="5f35f-126">必須</span><span class="sxs-lookup"><span data-stu-id="5f35f-126">Required</span></span>  <br/> |<span data-ttu-id="5f35f-127">**String**</span><span class="sxs-lookup"><span data-stu-id="5f35f-127">**String**</span></span> <br/> |<span data-ttu-id="5f35f-128">文字列を置換する文字列を入力__ します。</span><span class="sxs-lookup"><span data-stu-id="5f35f-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f35f-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="5f35f-129">Return value</span></span>

<span data-ttu-id="5f35f-130">文字列</span><span class="sxs-lookup"><span data-stu-id="5f35f-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f35f-131">注釈</span><span class="sxs-lookup"><span data-stu-id="5f35f-131">Remarks</span></span>

<span data-ttu-id="5f35f-p102">文字列内の特定の位置にある文字列を置換するときは、REPLACE 関数を使用します。文字列内の特定の文字列を置換するときは、SUBSTITUTE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="5f35f-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="5f35f-134">例</span><span class="sxs-lookup"><span data-stu-id="5f35f-134">Example</span></span>

<span data-ttu-id="5f35f-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="5f35f-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="5f35f-136">01/03/2003 を返します。</span><span class="sxs-lookup"><span data-stu-id="5f35f-136">Returns 01/03/2003.</span></span> 
  

