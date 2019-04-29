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
description: バイナリ数の対応するビットが0の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。 それ以外の場合、ビットは0に設定されます。
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438835"
---
# <a name="bitnot-function"></a><span data-ttu-id="0f085-104">BITNOT 関数</span><span class="sxs-lookup"><span data-stu-id="0f085-104">BITNOT Function</span></span>

<span data-ttu-id="0f085-105">バイナリ数の対応するビットが0の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。</span><span class="sxs-lookup"><span data-stu-id="0f085-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="0f085-106">それ以外の場合、ビットは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f085-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0f085-107">構文</span><span class="sxs-lookup"><span data-stu-id="0f085-107">Syntax</span></span>

<span data-ttu-id="0f085-108">bitnot (\* **バイナリ番号** \*)</span><span class="sxs-lookup"><span data-stu-id="0f085-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0f085-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0f085-109">Parameters</span></span>

|<span data-ttu-id="0f085-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="0f085-110">**Name**</span></span>|<span data-ttu-id="0f085-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0f085-111">**Required/Optional**</span></span>|<span data-ttu-id="0f085-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0f085-112">**Data Type**</span></span>|<span data-ttu-id="0f085-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="0f085-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0f085-114">_バイナリ番号_</span><span class="sxs-lookup"><span data-stu-id="0f085-114">_binary number_</span></span> <br/> |<span data-ttu-id="0f085-115">必須</span><span class="sxs-lookup"><span data-stu-id="0f085-115">Required</span></span>  <br/> |<span data-ttu-id="0f085-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="0f085-116">**Numeric**</span></span> <br/> |<span data-ttu-id="0f085-117">16 ビットのバイナリ数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f085-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0f085-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f085-118">Return value</span></span>

<span data-ttu-id="0f085-119">16 ビットのバイナリ数値</span><span class="sxs-lookup"><span data-stu-id="0f085-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="0f085-120">例</span><span class="sxs-lookup"><span data-stu-id="0f085-120">Example</span></span>

<span data-ttu-id="0f085-121">bitnot (6)</span><span class="sxs-lookup"><span data-stu-id="0f085-121">BITNOT(6)</span></span>
  
<span data-ttu-id="0f085-p103">65529 を返します。6 = 0...00110 であり、したがって BITNOT(6) = 1...11001 となります。</span><span class="sxs-lookup"><span data-stu-id="0f085-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

