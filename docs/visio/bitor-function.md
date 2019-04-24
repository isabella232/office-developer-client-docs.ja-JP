---
title: BITOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: binary number1 または binary number2 の対応するビットが1の場合、各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方で対応するビットが0の場合にのみ、ビットが0に設定されます。
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303375"
---
# <a name="bitor-function"></a><span data-ttu-id="9205d-104">BITOR 関数</span><span class="sxs-lookup"><span data-stu-id="9205d-104">BITOR Function</span></span>

<span data-ttu-id="9205d-105">*binary number1*または*binary number2*の対応するビットが1の場合、各ビットが1に設定された16ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="9205d-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="9205d-106">*binary number1*と*binary number2*の両方で対応するビットが0の場合にのみ、ビットが0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9205d-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9205d-107">構文</span><span class="sxs-lookup"><span data-stu-id="9205d-107">Syntax</span></span>

<span data-ttu-id="9205d-108">bitor (\* \* *binary number1* \* \*, \* \* *binary number2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9205d-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9205d-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9205d-109">Parameters</span></span>

|<span data-ttu-id="9205d-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="9205d-110">**Name**</span></span>|<span data-ttu-id="9205d-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9205d-111">**Required/Optional**</span></span>|<span data-ttu-id="9205d-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9205d-112">**Data Type**</span></span>|<span data-ttu-id="9205d-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="9205d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9205d-114">_二項数値1_</span><span class="sxs-lookup"><span data-stu-id="9205d-114">_binary number1_</span></span> <br/> |<span data-ttu-id="9205d-115">必須</span><span class="sxs-lookup"><span data-stu-id="9205d-115">Required</span></span>  <br/> |<span data-ttu-id="9205d-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="9205d-116">**Numeric**</span></span> <br/> |<span data-ttu-id="9205d-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9205d-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="9205d-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="9205d-118">_binary number2_</span></span> <br/> |<span data-ttu-id="9205d-119">必須</span><span class="sxs-lookup"><span data-stu-id="9205d-119">Required</span></span>  <br/> |<span data-ttu-id="9205d-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="9205d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="9205d-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9205d-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9205d-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="9205d-122">Return value</span></span>

<span data-ttu-id="9205d-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="9205d-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="9205d-124">例</span><span class="sxs-lookup"><span data-stu-id="9205d-124">Example</span></span>

<span data-ttu-id="9205d-125">bitor (12, 6)</span><span class="sxs-lookup"><span data-stu-id="9205d-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="9205d-p103">14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。</span><span class="sxs-lookup"><span data-stu-id="9205d-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

