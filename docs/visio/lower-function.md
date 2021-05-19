---
title: LOWER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: 小文字に変換された文字列を返します。
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421243"
---
# <a name="lower-function"></a><span data-ttu-id="81e1d-103">LOWER 関数</span><span class="sxs-lookup"><span data-stu-id="81e1d-103">LOWER Function</span></span>

<span data-ttu-id="81e1d-104">小文字に変換された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="81e1d-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="81e1d-105">構文</span><span class="sxs-lookup"><span data-stu-id="81e1d-105">Syntax</span></span>

<span data-ttu-id="81e1d-106">LOWER(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="81e1d-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="81e1d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81e1d-107">Parameters</span></span>

|<span data-ttu-id="81e1d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="81e1d-108">**Name**</span></span>|<span data-ttu-id="81e1d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="81e1d-109">**Required/Optional**</span></span>|<span data-ttu-id="81e1d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="81e1d-110">**Data Type**</span></span>|<span data-ttu-id="81e1d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="81e1d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="81e1d-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="81e1d-112">_expression_</span></span> <br/> |<span data-ttu-id="81e1d-113">必須</span><span class="sxs-lookup"><span data-stu-id="81e1d-113">Required</span></span>  <br/> |<span data-ttu-id="81e1d-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="81e1d-114">**Varies**</span></span> <br/> | <span data-ttu-id="81e1d-115">文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、小文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="81e1d-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="81e1d-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="81e1d-116">Return value</span></span>

<span data-ttu-id="81e1d-117">文字列</span><span class="sxs-lookup"><span data-stu-id="81e1d-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81e1d-118">注釈</span><span class="sxs-lookup"><span data-stu-id="81e1d-118">Remarks</span></span>

<span data-ttu-id="81e1d-119">大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="81e1d-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="81e1d-120">例</span><span class="sxs-lookup"><span data-stu-id="81e1d-120">Example</span></span>

<span data-ttu-id="81e1d-121">LOWER("mIxEd CAse")</span><span class="sxs-lookup"><span data-stu-id="81e1d-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="81e1d-122">"mixed case" を返します。</span><span class="sxs-lookup"><span data-stu-id="81e1d-122">Returns "mixed case".</span></span> 
  

