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
description: セルを参照します。参照されているセルが変更されても、数式は再計算されません。
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356500"
---
# <a name="getref-function"></a><span data-ttu-id="6b56d-103">GETREF 関数</span><span class="sxs-lookup"><span data-stu-id="6b56d-103">GETREF Function</span></span>

<span data-ttu-id="6b56d-104">セルを参照します。参照されているセルが変更されても、数式は再計算されません。</span><span class="sxs-lookup"><span data-stu-id="6b56d-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6b56d-105">構文</span><span class="sxs-lookup"><span data-stu-id="6b56d-105">Syntax</span></span>

<span data-ttu-id="6b56d-106">getref (\* \* *cellname* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6b56d-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6b56d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b56d-107">Parameters</span></span>

|<span data-ttu-id="6b56d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6b56d-108">**Name**</span></span>|<span data-ttu-id="6b56d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6b56d-109">**Required/Optional**</span></span>|<span data-ttu-id="6b56d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6b56d-110">**Data Type**</span></span>|<span data-ttu-id="6b56d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b56d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6b56d-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="6b56d-112">_cellname_</span></span> <br/> |<span data-ttu-id="6b56d-113">必須</span><span class="sxs-lookup"><span data-stu-id="6b56d-113">Required</span></span>  <br/> |<span data-ttu-id="6b56d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6b56d-114">**String**</span></span> <br/> |<span data-ttu-id="6b56d-115">参照を取得するセルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b56d-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="6b56d-116">例</span><span class="sxs-lookup"><span data-stu-id="6b56d-116">Example</span></span>

<span data-ttu-id="6b56d-117">setf (getref (PinX), 5.1)</span><span class="sxs-lookup"><span data-stu-id="6b56d-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="6b56d-118">[PinX] セルの数式を 5.1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b56d-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

