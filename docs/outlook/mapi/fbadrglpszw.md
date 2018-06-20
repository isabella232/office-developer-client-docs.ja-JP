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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: da31da0ae0437e1578a681d9232b0693932b2aec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800036"
---
# <a name="fbadrglpszw"></a><span data-ttu-id="319cb-103">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="319cb-103">FBadRglpszW</span></span>

  
  
<span data-ttu-id="319cb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="319cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="319cb-105">Unicode 文字列の配列内のすべての文字列を検証します。</span><span class="sxs-lookup"><span data-stu-id="319cb-105">Validates all strings in an array of Unicode strings.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="319cb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="319cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="319cb-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="319cb-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="319cb-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="319cb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="319cb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="319cb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="319cb-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="319cb-110">Called by:</span></span>  <br/> |<span data-ttu-id="319cb-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="319cb-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpszW(
  LPWSTR FAR * lppszW,
  ULONG cStrings
);
```

## <a name="parameters"></a><span data-ttu-id="319cb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="319cb-112">Parameters</span></span>

 <span data-ttu-id="319cb-113">_lppszW_</span><span class="sxs-lookup"><span data-stu-id="319cb-113">_lppszW_</span></span>
  
> <span data-ttu-id="319cb-114">[in]Null で終わる Unicode 文字列の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="319cb-114">[in] Pointer to an array of null-terminated Unicode strings.</span></span> 
    
 <span data-ttu-id="319cb-115">_cStrings_</span><span class="sxs-lookup"><span data-stu-id="319cb-115">_cStrings_</span></span>
  
> <span data-ttu-id="319cb-116">[in]_LppszW_パラメーターが指す配列内の文字列の数です。</span><span class="sxs-lookup"><span data-stu-id="319cb-116">[in] Count of strings in the array pointed to by the  _lppszW_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="319cb-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="319cb-117">Return value</span></span>

<span data-ttu-id="319cb-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="319cb-118">TRUE</span></span> 
  
> <span data-ttu-id="319cb-119">1 つ以上の指定した配列内の文字列が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="319cb-119">One or more of the strings in the specified array are invalid.</span></span> 
    
<span data-ttu-id="319cb-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="319cb-120">FALSE</span></span> 
  
> <span data-ttu-id="319cb-121">指定した配列内の文字列は、有効です。</span><span class="sxs-lookup"><span data-stu-id="319cb-121">The strings in the specified array are valid.</span></span>
    

