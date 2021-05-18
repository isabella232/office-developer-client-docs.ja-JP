---
title: NOW 関数 (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: 現在の日付と時刻の値を返します。
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414082"
---
# <a name="now-function-visioshapesheet"></a><span data-ttu-id="bb9f9-103">NOW 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bb9f9-103">NOW Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bb9f9-104">現在の日付と時刻の値を返します。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-104">Returns the current date and time value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bb9f9-105">構文</span><span class="sxs-lookup"><span data-stu-id="bb9f9-105">Syntax</span></span>

<span data-ttu-id="bb9f9-106">NOW ( )</span><span class="sxs-lookup"><span data-stu-id="bb9f9-106">NOW ( )</span></span>
  
### <a name="return-value"></a><span data-ttu-id="bb9f9-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb9f9-107">Return value</span></span>

<span data-ttu-id="bb9f9-108">Datetime</span><span class="sxs-lookup"><span data-stu-id="bb9f9-108">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb9f9-109">注釈</span><span class="sxs-lookup"><span data-stu-id="bb9f9-109">Remarks</span></span>

<span data-ttu-id="bb9f9-110">NOW は 1 分ごとに自動的に再計算されます。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-110">NOW is automatically recalculated every minute.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bb9f9-111">例 1</span><span class="sxs-lookup"><span data-stu-id="bb9f9-111">Example 1</span></span>

<span data-ttu-id="bb9f9-112">NOW( )</span><span class="sxs-lookup"><span data-stu-id="bb9f9-112">NOW( )</span></span>
  
<span data-ttu-id="bb9f9-113">現在の日付と時刻 (9/27/2010 12:03:30 PM など) を返します。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-113">Returns the current date and time, such as 9/27/2010 12:03:30 PM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bb9f9-114">例 2</span><span class="sxs-lookup"><span data-stu-id="bb9f9-114">Example 2</span></span>

<span data-ttu-id="bb9f9-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span><span class="sxs-lookup"><span data-stu-id="bb9f9-115">FORMAT(NOW(),"dd MMM., yyyy hh:mm")</span></span>
  
<span data-ttu-id="bb9f9-116">現在の日付と時刻を 27 Sep., 2010 12:03 のように書式設定して返します。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-116">Returns the current date and time formatted as 27 Sep., 2010 12:03.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bb9f9-117">例 3</span><span class="sxs-lookup"><span data-stu-id="bb9f9-117">Example 3</span></span>

<span data-ttu-id="bb9f9-118">NOW()+2EW。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-118">NOW()+2EW.</span></span>
  
<span data-ttu-id="bb9f9-119">現在の日付と時刻から 2 週間経過した日付と時刻 (10/11/10 12:03:30 PM など) を返します。</span><span class="sxs-lookup"><span data-stu-id="bb9f9-119">Returns the current date and time plus two elapsed weeks, such as 10/11/10 12:03:30 PM.</span></span>
  

