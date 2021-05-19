---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409455"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="c1c94-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="c1c94-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="c1c94-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1c94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1c94-105">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="c1c94-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="c1c94-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1c94-106">Parameters</span></span>

 <span data-ttu-id="c1c94-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="c1c94-107">_bkPosition_</span></span>
  
> <span data-ttu-id="c1c94-108">[in] [IMAPITable::CreateBookmark](imapitable-createbookmark.md) メソッドを呼び出して作成される、解放するブックマーク。</span><span class="sxs-lookup"><span data-stu-id="c1c94-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c1c94-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="c1c94-109">Return value</span></span>

<span data-ttu-id="c1c94-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1c94-110">S_OK</span></span> 
  
> <span data-ttu-id="c1c94-111">ブックマークが正常に解放されました。</span><span class="sxs-lookup"><span data-stu-id="c1c94-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="c1c94-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="c1c94-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="c1c94-113">指定したブックマークが存在しません。</span><span class="sxs-lookup"><span data-stu-id="c1c94-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1c94-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c1c94-114">Remarks</span></span>

<span data-ttu-id="c1c94-115">**IMAPITable::FreeBookmark** メソッドは、不要になったブックマークを解放します。</span><span class="sxs-lookup"><span data-stu-id="c1c94-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="c1c94-116">ブックマークは、この呼び出し後に無効になります。</span><span class="sxs-lookup"><span data-stu-id="c1c94-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="c1c94-117">テーブルがメモリから解放されると、関連付けられたブックマークもすべて解放されます。</span><span class="sxs-lookup"><span data-stu-id="c1c94-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c1c94-118">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="c1c94-118">Notes to implementers</span></span>

<span data-ttu-id="c1c94-119">呼び出し元が  _bkPosition_ パラメーターで 3 つの定義済みのブックマークのいずれかを渡した場合は、要求を無視して、S_OK。</span><span class="sxs-lookup"><span data-stu-id="c1c94-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1c94-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1c94-120">See also</span></span>



[<span data-ttu-id="c1c94-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="c1c94-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="c1c94-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1c94-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

