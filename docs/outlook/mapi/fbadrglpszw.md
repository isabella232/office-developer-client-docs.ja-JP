---
title: FBadRglpszW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpszW
api_type:
- COM
ms.assetid: 880eb35d-7045-4fdd-bb33-0f14557a7316
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ca436bc83d5170d55475c1dd9702a9d54e4b9d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436441"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="2547e-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="2547e-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="2547e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2547e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2547e-105">Unicode 文字列の配列内のすべての文字列を検証します。</span><span class="sxs-lookup"><span data-stu-id="2547e-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2547e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2547e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2547e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="2547e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="2547e-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="2547e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2547e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2547e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2547e-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2547e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2547e-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="2547e-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="2547e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2547e-112">Parameters</span></span>

 <span data-ttu-id="2547e-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="2547e-113">_lppszW_</span></span>
  
> <span data-ttu-id="2547e-114">[in]Null 終端 Unicode 文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2547e-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="2547e-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="2547e-115">_cStrings_</span></span>
  
> <span data-ttu-id="2547e-116">[in]lppszW パラメーターが指す配列  _内の文字列の_ 数。</span><span class="sxs-lookup"><span data-stu-id="2547e-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2547e-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="2547e-117">Return value</span></span>

<span data-ttu-id="2547e-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="2547e-118">TRUE</span></span> 
  
> <span data-ttu-id="2547e-119">指定した配列内の 1 つ以上の文字列が無効です。</span><span class="sxs-lookup"><span data-stu-id="2547e-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="2547e-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="2547e-120">FALSE</span></span> 
  
> <span data-ttu-id="2547e-121">指定した配列内の文字列が有効です。</span><span class="sxs-lookup"><span data-stu-id="2547e-121">The strings in the specified array are valid.</span></span>
    

