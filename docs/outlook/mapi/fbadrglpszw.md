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
ms.openlocfilehash: 3b3b6b5ca0b06fc55a60e035ffd9118391cab8f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565915"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="069be-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="069be-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="069be-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="069be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="069be-105">Unicode 文字列の配列内のすべての文字列を検証します。</span><span class="sxs-lookup"><span data-stu-id="069be-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="069be-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="069be-106">Header file:</span></span>  <br/> |<span data-ttu-id="069be-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="069be-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="069be-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="069be-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="069be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="069be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="069be-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="069be-110">Called by:</span></span>  <br/> |<span data-ttu-id="069be-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="069be-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="069be-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="069be-112">Parameters</span></span>

 <span data-ttu-id="069be-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="069be-113">_lppszW_</span></span>
  
> <span data-ttu-id="069be-114">[in]Null で終わる Unicode 文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="069be-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="069be-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="069be-115">_cStrings_</span></span>
  
> <span data-ttu-id="069be-116">[in]_LppszW_パラメーターが指す配列内の文字列の数です。</span><span class="sxs-lookup"><span data-stu-id="069be-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="069be-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="069be-117">Return value</span></span>

<span data-ttu-id="069be-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="069be-118">TRUE</span></span> 
  
> <span data-ttu-id="069be-119">1 つ以上の指定した配列内の文字列が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="069be-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="069be-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="069be-120">FALSE</span></span> 
  
> <span data-ttu-id="069be-121">指定した配列内の文字列は、有効です。</span><span class="sxs-lookup"><span data-stu-id="069be-121">The strings in the specified array are valid.</span></span>
    

