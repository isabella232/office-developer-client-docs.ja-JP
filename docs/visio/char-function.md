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
description: いくつかの ANSI 文字を返します。
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804987"
---
# <a name="char-function"></a><span data-ttu-id="53d1d-103">CHAR 関数</span><span class="sxs-lookup"><span data-stu-id="53d1d-103">CHAR Function</span></span>

<span data-ttu-id="53d1d-104">いくつかの ANSI 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="53d1d-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="53d1d-105">構文</span><span class="sxs-lookup"><span data-stu-id="53d1d-105">Syntax</span></span>

<span data-ttu-id="53d1d-106">文字 (* **番号** *)</span><span class="sxs-lookup"><span data-stu-id="53d1d-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="53d1d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53d1d-107">Parameters</span></span>

|<span data-ttu-id="53d1d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="53d1d-108">**Name**</span></span>|<span data-ttu-id="53d1d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="53d1d-109">**Required/Optional**</span></span>|<span data-ttu-id="53d1d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="53d1d-110">**Data Type**</span></span>|<span data-ttu-id="53d1d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="53d1d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="53d1d-112">_number_</span><span class="sxs-lookup"><span data-stu-id="53d1d-112">_number_</span></span> <br/> |<span data-ttu-id="53d1d-113">必須</span><span class="sxs-lookup"><span data-stu-id="53d1d-113">Required</span></span>  <br/> |<span data-ttu-id="53d1d-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="53d1d-114">**Number**</span></span> <br/> |<span data-ttu-id="53d1d-115">取得する ANSI 文字の数です。</span><span class="sxs-lookup"><span data-stu-id="53d1d-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53d1d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="53d1d-116">Remarks</span></span>

<span data-ttu-id="53d1d-117">結果の文字列は、1 つの文字の長さです。</span><span class="sxs-lookup"><span data-stu-id="53d1d-117">The resulting string is one character in length.</span></span> <span data-ttu-id="53d1d-118">_数_パラメーターは 1 から 255 まで (両端を含む) の間の整数である必要がありますか、エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="53d1d-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="53d1d-119">例</span><span class="sxs-lookup"><span data-stu-id="53d1d-119">Example</span></span>

<span data-ttu-id="53d1d-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="53d1d-120">CHAR(9)</span></span> 
  
<span data-ttu-id="53d1d-121">タブ文字を返します。</span><span class="sxs-lookup"><span data-stu-id="53d1d-121">Returns the tab character.</span></span> 
  

