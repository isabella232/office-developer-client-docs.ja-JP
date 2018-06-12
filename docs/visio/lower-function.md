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
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805808"
---
# <a name="lower-function"></a><span data-ttu-id="4b9cb-103">LOWER 関数</span><span class="sxs-lookup"><span data-stu-id="4b9cb-103">LOWER Function</span></span>

<span data-ttu-id="4b9cb-104">小文字に変換された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4b9cb-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4b9cb-105">構文</span><span class="sxs-lookup"><span data-stu-id="4b9cb-105">Syntax</span></span>

<span data-ttu-id="4b9cb-106">下 (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="4b9cb-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4b9cb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4b9cb-107">Parameters</span></span>

|<span data-ttu-id="4b9cb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="4b9cb-108">**Name**</span></span>|<span data-ttu-id="4b9cb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4b9cb-109">**Required/Optional**</span></span>|<span data-ttu-id="4b9cb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4b9cb-110">**Data Type**</span></span>|<span data-ttu-id="4b9cb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4b9cb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4b9cb-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="4b9cb-112">_expression_</span></span> <br/> |<span data-ttu-id="4b9cb-113">必須</span><span class="sxs-lookup"><span data-stu-id="4b9cb-113">Required</span></span>  <br/> |<span data-ttu-id="4b9cb-114">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="4b9cb-114">**Varies**</span></span> <br/> | <span data-ttu-id="4b9cb-115">文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、小文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="4b9cb-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4b9cb-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4b9cb-116">Return value</span></span>

<span data-ttu-id="4b9cb-117">文字列</span><span class="sxs-lookup"><span data-stu-id="4b9cb-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4b9cb-118">注釈</span><span class="sxs-lookup"><span data-stu-id="4b9cb-118">Remarks</span></span>

<span data-ttu-id="4b9cb-119">大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="4b9cb-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4b9cb-120">例</span><span class="sxs-lookup"><span data-stu-id="4b9cb-120">Example</span></span>

<span data-ttu-id="4b9cb-121">LOWER("mIxEd CAse")</span><span class="sxs-lookup"><span data-stu-id="4b9cb-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="4b9cb-122">"mixed case" を返します。</span><span class="sxs-lookup"><span data-stu-id="4b9cb-122">Returns "mixed case".</span></span> 
  
