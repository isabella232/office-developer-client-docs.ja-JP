---
title: GETREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: セルを参照し、参照先のセルが変更されたとき、数式を再計算しません。
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805470"
---
# <a name="getref-function"></a><span data-ttu-id="20864-103">GETREF 関数</span><span class="sxs-lookup"><span data-stu-id="20864-103">GETREF Function</span></span>

<span data-ttu-id="20864-104">セルを参照し、参照先のセルが変更されたとき、数式を再計算しません。</span><span class="sxs-lookup"><span data-stu-id="20864-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="20864-105">構文</span><span class="sxs-lookup"><span data-stu-id="20864-105">Syntax</span></span>

<span data-ttu-id="20864-106">GETREF (* * *cellname* * *)</span><span class="sxs-lookup"><span data-stu-id="20864-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20864-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="20864-107">Parameters</span></span>

|<span data-ttu-id="20864-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="20864-108">**Name**</span></span>|<span data-ttu-id="20864-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="20864-109">**Required/Optional**</span></span>|<span data-ttu-id="20864-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="20864-110">**Data Type**</span></span>|<span data-ttu-id="20864-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="20864-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20864-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="20864-112">_cellname_</span></span> <br/> |<span data-ttu-id="20864-113">必須</span><span class="sxs-lookup"><span data-stu-id="20864-113">Required</span></span>  <br/> |<span data-ttu-id="20864-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="20864-114">**String**</span></span> <br/> |<span data-ttu-id="20864-115">参照を取得するセルの名前です。</span><span class="sxs-lookup"><span data-stu-id="20864-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="20864-116">例</span><span class="sxs-lookup"><span data-stu-id="20864-116">Example</span></span>

<span data-ttu-id="20864-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="20864-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="20864-118">[PinX] セルの数式を 5.1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="20864-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

