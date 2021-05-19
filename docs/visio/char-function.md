---
title: CHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: 数値の ANSI 文字を返します。
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418191"
---
# <a name="char-function"></a><span data-ttu-id="e1fe5-103">CHAR 関数</span><span class="sxs-lookup"><span data-stu-id="e1fe5-103">CHAR Function</span></span>

<span data-ttu-id="e1fe5-104">数値の ANSI 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="e1fe5-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e1fe5-105">構文</span><span class="sxs-lookup"><span data-stu-id="e1fe5-105">Syntax</span></span>

<span data-ttu-id="e1fe5-106">CHAR(\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e1fe5-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1fe5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1fe5-107">Parameters</span></span>

|<span data-ttu-id="e1fe5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e1fe5-108">**Name**</span></span>|<span data-ttu-id="e1fe5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e1fe5-109">**Required/Optional**</span></span>|<span data-ttu-id="e1fe5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e1fe5-110">**Data Type**</span></span>|<span data-ttu-id="e1fe5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e1fe5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1fe5-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e1fe5-112">_number_</span></span> <br/> |<span data-ttu-id="e1fe5-113">必須</span><span class="sxs-lookup"><span data-stu-id="e1fe5-113">Required</span></span>  <br/> |<span data-ttu-id="e1fe5-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="e1fe5-114">**Number**</span></span> <br/> |<span data-ttu-id="e1fe5-115">ANSI 文字を取得する番号。</span><span class="sxs-lookup"><span data-stu-id="e1fe5-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1fe5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="e1fe5-116">Remarks</span></span>

<span data-ttu-id="e1fe5-117">結果の文字列の長さは 1 文字です。</span><span class="sxs-lookup"><span data-stu-id="e1fe5-117">The resulting string is one character in length.</span></span> <span data-ttu-id="e1fe5-118">number  _パラメーター_ は、1 ~ 255 の整数 (含む) である必要があります。または、関数はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="e1fe5-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e1fe5-119">例</span><span class="sxs-lookup"><span data-stu-id="e1fe5-119">Example</span></span>

<span data-ttu-id="e1fe5-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="e1fe5-120">CHAR(9)</span></span> 
  
<span data-ttu-id="e1fe5-121">タブ文字を返します。</span><span class="sxs-lookup"><span data-stu-id="e1fe5-121">Returns the tab character.</span></span> 
  

