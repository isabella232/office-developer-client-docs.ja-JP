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
description: バイナリ数値 1] または [バイナリの数値を 2 に対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 バイナリの数値を 1 と数値 2 のバイナリの両方に対応するビットは、0 の場合にのみ、ビットは 0 に設定します。
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804865"
---
# <a name="bitor-function"></a><span data-ttu-id="9f76f-104">BITOR 関数</span><span class="sxs-lookup"><span data-stu-id="9f76f-104">BITOR Function</span></span>

<span data-ttu-id="9f76f-105">*バイナリ数値 1* ] または [*バイナリの数値を 2*に対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="9f76f-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="9f76f-106">ビットは、対応するビットが 0 の*バイナリの数値を 1*と*数値 2 のバイナリ*の両方である場合にのみ、0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9f76f-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9f76f-107">構文</span><span class="sxs-lookup"><span data-stu-id="9f76f-107">Syntax</span></span>

<span data-ttu-id="9f76f-108">BITOR (* **バイナリ数値 1* * *、* **バイナリ数値 2* * *)</span><span class="sxs-lookup"><span data-stu-id="9f76f-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f76f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9f76f-109">Parameters</span></span>

|<span data-ttu-id="9f76f-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="9f76f-110">**Name**</span></span>|<span data-ttu-id="9f76f-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9f76f-111">**Required/Optional**</span></span>|<span data-ttu-id="9f76f-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9f76f-112">**Data Type**</span></span>|<span data-ttu-id="9f76f-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="9f76f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f76f-114">_バイナリの数値 1_</span><span class="sxs-lookup"><span data-stu-id="9f76f-114">_binary number1_</span></span> <br/> |<span data-ttu-id="9f76f-115">必須</span><span class="sxs-lookup"><span data-stu-id="9f76f-115">Required</span></span>  <br/> |<span data-ttu-id="9f76f-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="9f76f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="9f76f-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f76f-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="9f76f-118">_バイナリ数値 2_</span><span class="sxs-lookup"><span data-stu-id="9f76f-118">_binary number2_</span></span> <br/> |<span data-ttu-id="9f76f-119">必須</span><span class="sxs-lookup"><span data-stu-id="9f76f-119">Required</span></span>  <br/> |<span data-ttu-id="9f76f-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="9f76f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="9f76f-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9f76f-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9f76f-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="9f76f-122">Return value</span></span>

<span data-ttu-id="9f76f-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="9f76f-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="9f76f-124">例</span><span class="sxs-lookup"><span data-stu-id="9f76f-124">Example</span></span>

<span data-ttu-id="9f76f-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="9f76f-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="9f76f-p103">14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。</span><span class="sxs-lookup"><span data-stu-id="9f76f-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

