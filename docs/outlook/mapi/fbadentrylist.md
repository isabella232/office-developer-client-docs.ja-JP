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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800029"
---
# <a name="fbadentrylist"></a><span data-ttu-id="cf588-103">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="cf588-103">FBadEntryList</span></span>

  
  
<span data-ttu-id="cf588-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf588-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf588-105">MAPI エントリの識別子の一覧を検証します。</span><span class="sxs-lookup"><span data-stu-id="cf588-105">Validates a list of MAPI entry identifiers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf588-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cf588-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf588-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="cf588-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="cf588-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="cf588-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf588-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf588-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf588-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cf588-110">Called by:</span></span>  <br/> |<span data-ttu-id="cf588-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cf588-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a><span data-ttu-id="cf588-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf588-112">Parameters</span></span>

 <span data-ttu-id="cf588-113">_lpEntryList_</span><span class="sxs-lookup"><span data-stu-id="cf588-113">_lpEntryList_</span></span>
  
> <span data-ttu-id="cf588-114">[in]検証するエントリの識別子の配列を含む[ENTRYLIST](entrylist.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf588-114">[in] Pointer to an [ENTRYLIST](entrylist.md) structure that contains an array of entry identifiers to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cf588-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cf588-115">Return value</span></span>

<span data-ttu-id="cf588-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf588-116">TRUE</span></span> 
  
> <span data-ttu-id="cf588-117">表示されたエントリの識別子の 1 つ以上が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="cf588-117">One or more of the listed entry identifiers are invalid.</span></span> 
    
<span data-ttu-id="cf588-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf588-118">FALSE</span></span> 
  
> <span data-ttu-id="cf588-119">すべてのエントリが一覧表示されている識別子は、有効です。</span><span class="sxs-lookup"><span data-stu-id="cf588-119">All of the listed entry identifiers are valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cf588-120">備考</span><span class="sxs-lookup"><span data-stu-id="cf588-120">Remarks</span></span>

<span data-ttu-id="cf588-121">**FBadEntryList**関数では、エントリの識別子] ボックスの一覧が正しく生成されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="cf588-121">The **FBadEntryList** function determines if the entry identifier list has been correctly generated.</span></span> <span data-ttu-id="cf588-122">無効な識別子の例は、メモリが正しく割り当てられていないか、不適切なサイズの識別子のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="cf588-122">An example of an invalid identifier is one for which memory has been incorrectly allocated or an identifier of an incorrect size.</span></span> 
  

