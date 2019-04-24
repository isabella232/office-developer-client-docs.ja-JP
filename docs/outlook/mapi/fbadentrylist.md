---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 21ed5a23b96dabdd594547109ecb1e6c048a4844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341070"
---
# <a name="fbadentrylist"></a><span data-ttu-id="c0eb9-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="c0eb9-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="c0eb9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0eb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0eb9-105">MAPI エントリ識別子の一覧を検証します。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0eb9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c0eb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0eb9-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c0eb9-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c0eb9-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c0eb9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0eb9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0eb9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0eb9-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c0eb9-110">Called by:</span></span>  <br/> |<span data-ttu-id="c0eb9-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c0eb9-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="c0eb9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0eb9-112">Parameters</span></span>

 <span data-ttu-id="c0eb9-113">_lペン trylist_</span><span class="sxs-lookup"><span data-stu-id="c0eb9-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="c0eb9-114">順番検証するエントリ識別子の配列を含む[entrylist](entrylist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0eb9-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c0eb9-115">Return value</span></span>

<span data-ttu-id="c0eb9-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0eb9-116">TRUE</span></span> 
  
> <span data-ttu-id="c0eb9-117">リストされている1つ以上のエントリ識別子が無効です。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="c0eb9-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0eb9-118">FALSE</span></span> 
  
> <span data-ttu-id="c0eb9-119">リストされているすべてのエントリ識別子が有効である。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0eb9-120">解説</span><span class="sxs-lookup"><span data-stu-id="c0eb9-120">Remarks</span></span>

<span data-ttu-id="c0eb9-121">**fbadentrylist**関数は、エントリ id の一覧が正しく生成されているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="c0eb9-122">無効な識別子の例としては、メモリが正しく割り当てられていないか、または間違ったサイズの識別子があります。</span><span class="sxs-lookup"><span data-stu-id="c0eb9-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

