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
description: 指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427522"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="68e38-103">LEFT 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="68e38-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="68e38-104">指定した文字数に基づいて、テキスト文字列の一番左の文字または文字を返します。</span><span class="sxs-lookup"><span data-stu-id="68e38-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="68e38-105">構文</span><span class="sxs-lookup"><span data-stu-id="68e38-105">Syntax</span></span>

<span data-ttu-id="68e38-106">LEFT(\*\* *text* \*\*, [, \*\*\*\* num_chars_opt \*\* ])</span><span class="sxs-lookup"><span data-stu-id="68e38-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="68e38-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68e38-107">Parameters</span></span>

|<span data-ttu-id="68e38-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="68e38-108">**Name**</span></span>|<span data-ttu-id="68e38-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="68e38-109">**Required/Optional**</span></span>|<span data-ttu-id="68e38-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="68e38-110">**Data Type**</span></span>|<span data-ttu-id="68e38-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="68e38-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="68e38-112">_text_</span><span class="sxs-lookup"><span data-stu-id="68e38-112">_text_</span></span> <br/> |<span data-ttu-id="68e38-113">必須</span><span class="sxs-lookup"><span data-stu-id="68e38-113">Required</span></span>  <br/> |<span data-ttu-id="68e38-114">**String**</span><span class="sxs-lookup"><span data-stu-id="68e38-114">**String**</span></span> <br/> |<span data-ttu-id="68e38-115">抽出する文字を含む文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="68e38-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="68e38-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="68e38-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="68e38-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="68e38-117">Optional</span></span>  <br/> |<span data-ttu-id="68e38-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="68e38-118">**Numeric**</span></span> <br/> |<span data-ttu-id="68e38-119">抽出する文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="68e38-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="68e38-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="68e38-120">Return value</span></span>

<span data-ttu-id="68e38-121">文字列</span><span class="sxs-lookup"><span data-stu-id="68e38-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68e38-122">注釈</span><span class="sxs-lookup"><span data-stu-id="68e38-122">Remarks</span></span>

<span data-ttu-id="68e38-123">値  _は、num_chars_opt_ 0 以上である必要があります。</span><span class="sxs-lookup"><span data-stu-id="68e38-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="68e38-124">テキスト  _num_chars_opt_ 長さより大きい場合、LEFT はすべてのテキストを返します。</span><span class="sxs-lookup"><span data-stu-id="68e38-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="68e38-125">この  _num_chars_opt_ を省略すると、1 と見なされます。</span><span class="sxs-lookup"><span data-stu-id="68e38-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="68e38-126">例</span><span class="sxs-lookup"><span data-stu-id="68e38-126">Example</span></span>

<span data-ttu-id="68e38-127">LEFT ("January 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="68e38-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="68e38-128">値 "Jan" を返します。</span><span class="sxs-lookup"><span data-stu-id="68e38-128">Returns the value "Jan".</span></span> 
  

