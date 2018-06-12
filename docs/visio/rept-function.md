---
title: REPT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: テキストを指定した回数だけ繰り返されます。
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806251"
---
# <a name="rept-function"></a><span data-ttu-id="5e1a7-103">REPT 関数</span><span class="sxs-lookup"><span data-stu-id="5e1a7-103">REPT Function</span></span>

<span data-ttu-id="5e1a7-104">テキストを指定した回数だけ繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5e1a7-105">構文</span><span class="sxs-lookup"><span data-stu-id="5e1a7-105">Syntax</span></span>

<span data-ttu-id="5e1a7-106">REPT (* **テキスト** *、* **繰り返し** *)</span><span class="sxs-lookup"><span data-stu-id="5e1a7-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5e1a7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e1a7-107">Parameters</span></span>

|<span data-ttu-id="5e1a7-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-108">**Name**</span></span>|<span data-ttu-id="5e1a7-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-109">**Required/Optional**</span></span>|<span data-ttu-id="5e1a7-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-110">**Data Type**</span></span>|<span data-ttu-id="5e1a7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5e1a7-112">_text_</span><span class="sxs-lookup"><span data-stu-id="5e1a7-112">_text_</span></span> <br/> |<span data-ttu-id="5e1a7-113">必須</span><span class="sxs-lookup"><span data-stu-id="5e1a7-113">Required</span></span>  <br/> |<span data-ttu-id="5e1a7-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-114">**String**</span></span> <br/> | <span data-ttu-id="5e1a7-115">繰り返す文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="5e1a7-116">_繰り返し回数_</span><span class="sxs-lookup"><span data-stu-id="5e1a7-116">_number_times_</span></span> <br/> |<span data-ttu-id="5e1a7-117">必須</span><span class="sxs-lookup"><span data-stu-id="5e1a7-117">Required</span></span>  <br/> |<span data-ttu-id="5e1a7-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="5e1a7-118">**Number**</span></span> <br/> |<span data-ttu-id="5e1a7-119">文字列の繰り返す回数を、正の数値で指定します。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e1a7-120">注釈</span><span class="sxs-lookup"><span data-stu-id="5e1a7-120">Remarks</span></span>

<span data-ttu-id="5e1a7-121">場合は、*繰り返し回数*は、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="5e1a7-122">number_times がゼロ (0) の場合、"" (空文字列) を返します。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="5e1a7-123">number_times が整数でない場合、小数点以下は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="5e1a7-124">例</span><span class="sxs-lookup"><span data-stu-id="5e1a7-124">Example</span></span>

<span data-ttu-id="5e1a7-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="5e1a7-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="5e1a7-126">返します。 \* \* \* \* \*。</span><span class="sxs-lookup"><span data-stu-id="5e1a7-126">Returns \*\*\*\*\*.</span></span> 
  

