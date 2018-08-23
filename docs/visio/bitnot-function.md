---
title: BITNOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: 2 進数に対応するビットが 0 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804848"
---
# <a name="bitnot-function"></a><span data-ttu-id="f7600-104">BITNOT 関数</span><span class="sxs-lookup"><span data-stu-id="f7600-104">BITNOT Function</span></span>

<span data-ttu-id="f7600-105">2 進数に対応するビットが 0 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7600-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="f7600-106">それ以外の場合、ビットが 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="f7600-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f7600-107">構文</span><span class="sxs-lookup"><span data-stu-id="f7600-107">Syntax</span></span>

<span data-ttu-id="f7600-108">BITNOT (* * *2 進数** *)</span><span class="sxs-lookup"><span data-stu-id="f7600-108">BITNOT(** *binary number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f7600-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7600-109">Parameters</span></span>

|<span data-ttu-id="f7600-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="f7600-110">**Name**</span></span>|<span data-ttu-id="f7600-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f7600-111">**Required/Optional**</span></span>|<span data-ttu-id="f7600-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f7600-112">**Data Type**</span></span>|<span data-ttu-id="f7600-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="f7600-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f7600-114">_2 進数_</span><span class="sxs-lookup"><span data-stu-id="f7600-114">_binary number_</span></span> <br/> |<span data-ttu-id="f7600-115">必須</span><span class="sxs-lookup"><span data-stu-id="f7600-115">Required</span></span>  <br/> |<span data-ttu-id="f7600-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="f7600-116">**Numeric**</span></span> <br/> |<span data-ttu-id="f7600-117">16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7600-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f7600-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7600-118">Return value</span></span>

<span data-ttu-id="f7600-119">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="f7600-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="f7600-120">例</span><span class="sxs-lookup"><span data-stu-id="f7600-120">Example</span></span>

<span data-ttu-id="f7600-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="f7600-121">BITNOT(6)</span></span>
  
<span data-ttu-id="f7600-p103">65529 を返します。6 = 0...00110 であり、したがって BITNOT(6) = 1...11001 となります。</span><span class="sxs-lookup"><span data-stu-id="f7600-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

