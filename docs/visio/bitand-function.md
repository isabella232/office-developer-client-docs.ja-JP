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
description: Binarynumber1 と binarynumber2 の両方に対応するビットが 1 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804873"
---
# <a name="bitand-function"></a><span data-ttu-id="c600a-104">BITAND 関数</span><span class="sxs-lookup"><span data-stu-id="c600a-104">BITAND Function</span></span>

<span data-ttu-id="c600a-105">Binarynumber1 と binarynumber2 の両方に対応するビットが 1 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="c600a-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="c600a-106">それ以外の場合、ビットが 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="c600a-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c600a-107">構文</span><span class="sxs-lookup"><span data-stu-id="c600a-107">Syntax</span></span>

<span data-ttu-id="c600a-108">BITAND (* * *binarynumber1* * *、* * *binarynumber2* * *)</span><span class="sxs-lookup"><span data-stu-id="c600a-108">BITAND(** *binarynumber1* **, ** *binarynumber2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c600a-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c600a-109">Parameters</span></span>

|<span data-ttu-id="c600a-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="c600a-110">**Name**</span></span>|<span data-ttu-id="c600a-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c600a-111">**Required/Optional**</span></span>|<span data-ttu-id="c600a-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c600a-112">**Data Type**</span></span>|<span data-ttu-id="c600a-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="c600a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c600a-114">_バイナリの数値 1_</span><span class="sxs-lookup"><span data-stu-id="c600a-114">_binary number1_</span></span> <br/> |<span data-ttu-id="c600a-115">必須</span><span class="sxs-lookup"><span data-stu-id="c600a-115">Required</span></span>  <br/> |<span data-ttu-id="c600a-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="c600a-116">**Numeric**</span></span> <br/> |<span data-ttu-id="c600a-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c600a-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="c600a-118">_バイナリ数値 2_</span><span class="sxs-lookup"><span data-stu-id="c600a-118">_binary number2_</span></span> <br/> |<span data-ttu-id="c600a-119">必須</span><span class="sxs-lookup"><span data-stu-id="c600a-119">Required</span></span>  <br/> |<span data-ttu-id="c600a-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="c600a-120">**Numeric**</span></span> <br/> |<span data-ttu-id="c600a-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c600a-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c600a-122">注釈</span><span class="sxs-lookup"><span data-stu-id="c600a-122">Remarks</span></span>

<span data-ttu-id="c600a-123">この関数を使用して、ビットマスクとして保存されている図形のプロパティ (図形の文字書式など) をテストしたり、変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="c600a-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="c600a-124">例</span><span class="sxs-lookup"><span data-stu-id="c600a-124">Example</span></span>

<span data-ttu-id="c600a-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="c600a-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="c600a-p103">4 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITAND(12,6) = 0...00100 となります。</span><span class="sxs-lookup"><span data-stu-id="c600a-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

