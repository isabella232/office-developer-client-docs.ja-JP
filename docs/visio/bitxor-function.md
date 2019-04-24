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
description: 各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方ではなく対応するビットが1に設定されています。 それ以外の場合、ビットは0に設定されます。
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302990"
---
# <a name="bitxor-function"></a><span data-ttu-id="d38a4-104">BITXOR 関数</span><span class="sxs-lookup"><span data-stu-id="d38a4-104">BITXOR Function</span></span>

<span data-ttu-id="d38a4-105">各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方ではなく対応するビットが1に設定されています。</span><span class="sxs-lookup"><span data-stu-id="d38a4-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="d38a4-106">それ以外の場合、ビットは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d38a4-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d38a4-107">構文</span><span class="sxs-lookup"><span data-stu-id="d38a4-107">Syntax</span></span>

<span data-ttu-id="d38a4-108">bitxor (\* \* *binary number1* \* \*, \* \* *binary number2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d38a4-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d38a4-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d38a4-109">Parameters</span></span>

|<span data-ttu-id="d38a4-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="d38a4-110">**Name**</span></span>|<span data-ttu-id="d38a4-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d38a4-111">**Required/Optional**</span></span>|<span data-ttu-id="d38a4-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d38a4-112">**Data Type**</span></span>|<span data-ttu-id="d38a4-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="d38a4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d38a4-114">_二項数値1_</span><span class="sxs-lookup"><span data-stu-id="d38a4-114">_binary number1_</span></span> <br/> |<span data-ttu-id="d38a4-115">必須</span><span class="sxs-lookup"><span data-stu-id="d38a4-115">Required</span></span>  <br/> |<span data-ttu-id="d38a4-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="d38a4-116">**Numeric**</span></span> <br/> |<span data-ttu-id="d38a4-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d38a4-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="d38a4-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="d38a4-118">_binary number2_</span></span> <br/> |<span data-ttu-id="d38a4-119">必須</span><span class="sxs-lookup"><span data-stu-id="d38a4-119">Required</span></span>  <br/> |<span data-ttu-id="d38a4-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="d38a4-120">**Numeric**</span></span> <br/> |<span data-ttu-id="d38a4-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d38a4-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d38a4-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="d38a4-122">Return value</span></span>

<span data-ttu-id="d38a4-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="d38a4-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="d38a4-124">例</span><span class="sxs-lookup"><span data-stu-id="d38a4-124">Example</span></span>

<span data-ttu-id="d38a4-125">bitxor (12, 6)</span><span class="sxs-lookup"><span data-stu-id="d38a4-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="d38a4-p103">10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。</span><span class="sxs-lookup"><span data-stu-id="d38a4-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

