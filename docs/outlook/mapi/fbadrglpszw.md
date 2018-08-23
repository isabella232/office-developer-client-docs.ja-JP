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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800036"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="11cdf-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="11cdf-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="11cdf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11cdf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11cdf-105">Unicode 文字列の配列内のすべての文字列を検証します。</span><span class="sxs-lookup"><span data-stu-id="11cdf-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11cdf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="11cdf-106">Header file:</span></span>  <br/> |<span data-ttu-id="11cdf-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="11cdf-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="11cdf-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="11cdf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11cdf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11cdf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11cdf-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="11cdf-110">Called by:</span></span>  <br/> |<span data-ttu-id="11cdf-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="11cdf-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="11cdf-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="11cdf-112">Parameters</span></span>

 <span data-ttu-id="11cdf-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="11cdf-113">_lppszW_</span></span>
  
> <span data-ttu-id="11cdf-114">[in]Null で終わる Unicode 文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="11cdf-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="11cdf-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="11cdf-115">_cStrings_</span></span>
  
> <span data-ttu-id="11cdf-116">[in]_LppszW_パラメーターが指す配列内の文字列の数です。</span><span class="sxs-lookup"><span data-stu-id="11cdf-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="11cdf-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="11cdf-117">Return value</span></span>

<span data-ttu-id="11cdf-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="11cdf-118">TRUE</span></span> 
  
> <span data-ttu-id="11cdf-119">1 つ以上の指定した配列内の文字列が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="11cdf-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="11cdf-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="11cdf-120">FALSE</span></span> 
  
> <span data-ttu-id="11cdf-121">指定した配列内の文字列は、有効です。</span><span class="sxs-lookup"><span data-stu-id="11cdf-121">The strings in the specified array are valid.</span></span>
    

