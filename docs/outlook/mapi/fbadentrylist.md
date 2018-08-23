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
ms.openlocfilehash: 113628ef5487bc66a07d1367c938ed178a8e32ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582911"
---
# <a name="fbadentrylist"></a><span data-ttu-id="dd49f-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="dd49f-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="dd49f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd49f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd49f-105">MAPI エントリの識別子の一覧を検証します。</span><span class="sxs-lookup"><span data-stu-id="dd49f-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd49f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="dd49f-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd49f-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="dd49f-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="dd49f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="dd49f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd49f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd49f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd49f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dd49f-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd49f-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="dd49f-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="dd49f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dd49f-112">Parameters</span></span>

 <span data-ttu-id="dd49f-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="dd49f-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="dd49f-114">[in]検証するエントリの識別子の配列を含む[ENTRYLIST](entrylist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="dd49f-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dd49f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="dd49f-115">Return value</span></span>

<span data-ttu-id="dd49f-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="dd49f-116">TRUE</span></span> 
  
> <span data-ttu-id="dd49f-117">表示されたエントリの識別子の 1 つ以上が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="dd49f-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="dd49f-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="dd49f-118">FALSE</span></span> 
  
> <span data-ttu-id="dd49f-119">すべてのエントリが一覧表示されている識別子は、有効です。</span><span class="sxs-lookup"><span data-stu-id="dd49f-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd49f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="dd49f-120">Remarks</span></span>

<span data-ttu-id="dd49f-121">**FBadEntryList**関数では、エントリの識別子] ボックスの一覧が正しく生成されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="dd49f-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="dd49f-122">無効な識別子の例は、メモリが正しく割り当てられていないか、不適切なサイズの識別子のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="dd49f-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

