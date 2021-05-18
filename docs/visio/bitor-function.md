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
description: 2 進数 1 または 2 進数の対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 ビットが 0 に設定されているのは、対応するビットがバイナリ番号 1 とバイナリ番号 2 の両方で 0 の場合のみです。
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408083"
---
# <a name="bitor-function"></a><span data-ttu-id="51aea-104">BITOR 関数</span><span class="sxs-lookup"><span data-stu-id="51aea-104">BITOR Function</span></span>

<span data-ttu-id="51aea-105">2 進数 1 または *2* 進数の対応するビットが 1 の場合、各ビットが *1* に設定されている 16 ビットのバイナリ番号を返します。</span><span class="sxs-lookup"><span data-stu-id="51aea-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="51aea-106">ビットが 0 に設定されているのは、対応するビットがバイナリ番号  *1*  とバイナリ番号 2 の両方で 0  *の場合のみです*  。</span><span class="sxs-lookup"><span data-stu-id="51aea-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="51aea-107">構文</span><span class="sxs-lookup"><span data-stu-id="51aea-107">Syntax</span></span>

<span data-ttu-id="51aea-108">BITOR(\*\* *バイナリ番号 1* \*\*, \*\* *バイナリ番号 2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="51aea-108">BITOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51aea-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="51aea-109">Parameters</span></span>

|<span data-ttu-id="51aea-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="51aea-110">**Name**</span></span>|<span data-ttu-id="51aea-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="51aea-111">**Required/Optional**</span></span>|<span data-ttu-id="51aea-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="51aea-112">**Data Type**</span></span>|<span data-ttu-id="51aea-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="51aea-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51aea-114">_バイナリ番号 1_</span><span class="sxs-lookup"><span data-stu-id="51aea-114">_binary number1_</span></span> <br/> |<span data-ttu-id="51aea-115">必須</span><span class="sxs-lookup"><span data-stu-id="51aea-115">Required</span></span>  <br/> |<span data-ttu-id="51aea-116">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="51aea-116">**Numeric**</span></span> <br/> |<span data-ttu-id="51aea-117">最初の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="51aea-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="51aea-118">_バイナリ番号 2_</span><span class="sxs-lookup"><span data-stu-id="51aea-118">_binary number2_</span></span> <br/> |<span data-ttu-id="51aea-119">必須</span><span class="sxs-lookup"><span data-stu-id="51aea-119">Required</span></span>  <br/> |<span data-ttu-id="51aea-120">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="51aea-120">**Numeric**</span></span> <br/> |<span data-ttu-id="51aea-121">2 番目の 16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="51aea-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51aea-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="51aea-122">Return value</span></span>

<span data-ttu-id="51aea-123">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="51aea-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="51aea-124">例</span><span class="sxs-lookup"><span data-stu-id="51aea-124">Example</span></span>

<span data-ttu-id="51aea-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="51aea-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="51aea-p103">14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。</span><span class="sxs-lookup"><span data-stu-id="51aea-p103">Returns 14. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITOR(12,6) = 0...01110.</span></span>
  

