---
title: BITXOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: 2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439234"
---
# <a name="bitxor-function"></a><span data-ttu-id="371c5-104">BITXOR 関数</span><span class="sxs-lookup"><span data-stu-id="371c5-104">BITXOR Function</span></span>

<span data-ttu-id="371c5-105">2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。</span><span class="sxs-lookup"><span data-stu-id="371c5-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="371c5-106">それ以外の場合、ビットは 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="371c5-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="371c5-107">構文</span><span class="sxs-lookup"><span data-stu-id="371c5-107">Syntax</span></span>

<span data-ttu-id="371c5-108">BITXOR(\*\* *バイナリ番号 1* \*\*, \*\* *バイナリ番号 2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="371c5-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="371c5-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="371c5-109">Parameters</span></span>

|<span data-ttu-id="371c5-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="371c5-110">**Name**</span></span>|<span data-ttu-id="371c5-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="371c5-111">**Required/Optional**</span></span>|<span data-ttu-id="371c5-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="371c5-112">**Data Type**</span></span>|<span data-ttu-id="371c5-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="371c5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="371c5-114">_バイナリ番号 1_</span><span class="sxs-lookup"><span data-stu-id="371c5-114">_binary number1_</span></span> <br/> |<span data-ttu-id="371c5-115">必須</span><span class="sxs-lookup"><span data-stu-id="371c5-115">Required</span></span>  <br/> |<span data-ttu-id="371c5-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="371c5-116">**Numeric**</span></span> <br/> |<span data-ttu-id="371c5-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="371c5-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="371c5-118">_バイナリ番号 2_</span><span class="sxs-lookup"><span data-stu-id="371c5-118">_binary number2_</span></span> <br/> |<span data-ttu-id="371c5-119">必須</span><span class="sxs-lookup"><span data-stu-id="371c5-119">Required</span></span>  <br/> |<span data-ttu-id="371c5-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="371c5-120">**Numeric**</span></span> <br/> |<span data-ttu-id="371c5-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="371c5-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="371c5-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="371c5-122">Return value</span></span>

<span data-ttu-id="371c5-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="371c5-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="371c5-124">例</span><span class="sxs-lookup"><span data-stu-id="371c5-124">Example</span></span>

<span data-ttu-id="371c5-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="371c5-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="371c5-p103">10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。</span><span class="sxs-lookup"><span data-stu-id="371c5-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

