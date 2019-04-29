---
title: UPPER 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251509
localization_priority: Normal
ms.assetid: ef94ee0f-dbb8-a2e1-1805-8a6609830d2a
description: 大文字に変換された文字列を返します。
ms.openlocfilehash: b88958526bfb5e08839077217759f7ffb50151b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415146"
---
# <a name="upper-function"></a><span data-ttu-id="dec3a-103">UPPER 関数</span><span class="sxs-lookup"><span data-stu-id="dec3a-103">UPPER Function</span></span>

<span data-ttu-id="dec3a-104">大文字に変換された文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="dec3a-104">Returns a string converted to uppercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dec3a-105">構文</span><span class="sxs-lookup"><span data-stu-id="dec3a-105">Syntax</span></span>

<span data-ttu-id="dec3a-106">UPPER (\* \* *expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="dec3a-106">UPPER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dec3a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dec3a-107">Parameters</span></span>

|<span data-ttu-id="dec3a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dec3a-108">**Name**</span></span>|<span data-ttu-id="dec3a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dec3a-109">**Required/Optional**</span></span>|<span data-ttu-id="dec3a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dec3a-110">**Data Type**</span></span>|<span data-ttu-id="dec3a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dec3a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dec3a-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="dec3a-112">_expression_</span></span> <br/> |<span data-ttu-id="dec3a-113">必須</span><span class="sxs-lookup"><span data-stu-id="dec3a-113">Required</span></span>  <br/> |<span data-ttu-id="dec3a-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="dec3a-114">**Varies**</span></span> <br/> | <span data-ttu-id="dec3a-115">文字列、セル参照、または式を指定します。指定した引数は文字列に変換されてから、大文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="dec3a-115">A string, a cell reference, or an expression; the result is converted to a string, which is then converted to uppercase.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dec3a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="dec3a-116">Remarks</span></span>

<span data-ttu-id="dec3a-117">大文字/小文字の変換はロケールによって異なる機能であり、現在の設定に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="dec3a-117">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="dec3a-118">例</span><span class="sxs-lookup"><span data-stu-id="dec3a-118">Example</span></span>

<span data-ttu-id="dec3a-119">UPPER("mIxEd CAse")</span><span class="sxs-lookup"><span data-stu-id="dec3a-119">UPPER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="dec3a-120">"MIXED CASE" を返します。</span><span class="sxs-lookup"><span data-stu-id="dec3a-120">Returns "MIXED CASE".</span></span> 
  

