---
title: BITAND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: binarynumber1 と binarynumber2 の両方の対応するビットが1の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。 それ以外の場合、ビットは0に設定されます。
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409728"
---
# <a name="bitand-function"></a><span data-ttu-id="93537-104">BITAND 関数</span><span class="sxs-lookup"><span data-stu-id="93537-104">BITAND Function</span></span>

<span data-ttu-id="93537-105">binarynumber1 と binarynumber2 の両方の対応するビットが1の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="93537-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="93537-106">それ以外の場合、ビットは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="93537-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="93537-107">構文</span><span class="sxs-lookup"><span data-stu-id="93537-107">Syntax</span></span>

<span data-ttu-id="93537-108">bitand (\* \* *binarynumber1* \* \*, \* \* *binarynumber2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="93537-108">BITAND(\*\* *binarynumber1* \*\*, \*\* *binarynumber2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="93537-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93537-109">Parameters</span></span>

|<span data-ttu-id="93537-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="93537-110">**Name**</span></span>|<span data-ttu-id="93537-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="93537-111">**Required/Optional**</span></span>|<span data-ttu-id="93537-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="93537-112">**Data Type**</span></span>|<span data-ttu-id="93537-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="93537-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="93537-114">_二項数値1_</span><span class="sxs-lookup"><span data-stu-id="93537-114">_binary number1_</span></span> <br/> |<span data-ttu-id="93537-115">必須</span><span class="sxs-lookup"><span data-stu-id="93537-115">Required</span></span>  <br/> |<span data-ttu-id="93537-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="93537-116">**Numeric**</span></span> <br/> |<span data-ttu-id="93537-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="93537-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="93537-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="93537-118">_binary number2_</span></span> <br/> |<span data-ttu-id="93537-119">必須</span><span class="sxs-lookup"><span data-stu-id="93537-119">Required</span></span>  <br/> |<span data-ttu-id="93537-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="93537-120">**Numeric**</span></span> <br/> |<span data-ttu-id="93537-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="93537-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93537-122">注釈</span><span class="sxs-lookup"><span data-stu-id="93537-122">Remarks</span></span>

<span data-ttu-id="93537-123">この関数を使用して、ビットマスクとして保存されている図形のプロパティ (図形の文字書式など) をテストしたり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="93537-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="93537-124">例</span><span class="sxs-lookup"><span data-stu-id="93537-124">Example</span></span>

<span data-ttu-id="93537-125">bitand (12, 6)</span><span class="sxs-lookup"><span data-stu-id="93537-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="93537-p103">4 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITAND(12,6) = 0...00100 となります。</span><span class="sxs-lookup"><span data-stu-id="93537-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

