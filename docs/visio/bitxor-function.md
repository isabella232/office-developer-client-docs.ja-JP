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
description: バイナリの数値を 1 とバイナリの数値 2 のどちらかがどちらに対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804884"
---
# <a name="bitxor-function"></a><span data-ttu-id="5050f-104">BITXOR 関数</span><span class="sxs-lookup"><span data-stu-id="5050f-104">BITXOR Function</span></span>

<span data-ttu-id="5050f-105">バイナリの数値を 1 とバイナリの数値 2 のどちらかがどちらに対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="5050f-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="5050f-106">それ以外の場合、ビットが 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5050f-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5050f-107">構文</span><span class="sxs-lookup"><span data-stu-id="5050f-107">Syntax</span></span>

<span data-ttu-id="5050f-108">BITXOR (* **バイナリ数値 1* * *、* **バイナリ数値 2* * *)</span><span class="sxs-lookup"><span data-stu-id="5050f-108">BITXOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5050f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5050f-109">Parameters</span></span>

|<span data-ttu-id="5050f-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="5050f-110">**Name**</span></span>|<span data-ttu-id="5050f-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5050f-111">**Required/Optional**</span></span>|<span data-ttu-id="5050f-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5050f-112">**Data Type**</span></span>|<span data-ttu-id="5050f-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="5050f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5050f-114">_バイナリの数値 1_</span><span class="sxs-lookup"><span data-stu-id="5050f-114">_binary number1_</span></span> <br/> |<span data-ttu-id="5050f-115">必須</span><span class="sxs-lookup"><span data-stu-id="5050f-115">Required</span></span>  <br/> |<span data-ttu-id="5050f-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="5050f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="5050f-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5050f-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="5050f-118">_バイナリ数値 2_</span><span class="sxs-lookup"><span data-stu-id="5050f-118">_binary number2_</span></span> <br/> |<span data-ttu-id="5050f-119">必須</span><span class="sxs-lookup"><span data-stu-id="5050f-119">Required</span></span>  <br/> |<span data-ttu-id="5050f-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="5050f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="5050f-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5050f-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5050f-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="5050f-122">Return value</span></span>

<span data-ttu-id="5050f-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="5050f-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="5050f-124">例</span><span class="sxs-lookup"><span data-stu-id="5050f-124">Example</span></span>

<span data-ttu-id="5050f-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="5050f-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="5050f-p103">10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。</span><span class="sxs-lookup"><span data-stu-id="5050f-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

