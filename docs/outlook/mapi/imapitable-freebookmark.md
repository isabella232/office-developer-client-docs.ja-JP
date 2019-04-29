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
# <a name="imapitablefreebookmark"></a><span data-ttu-id="55495-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="55495-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="55495-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55495-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55495-105">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="55495-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="55495-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="55495-106">Parameters</span></span>

 <span data-ttu-id="55495-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="55495-107">_bkPosition_</span></span>
  
> <span data-ttu-id="55495-108">順番、 [IMAPITable:: createbookmark](imapitable-createbookmark.md)メソッドを呼び出すことによって作成された、解放されるブックマーク。</span><span class="sxs-lookup"><span data-stu-id="55495-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="55495-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="55495-109">Return value</span></span>

<span data-ttu-id="55495-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="55495-110">S_OK</span></span> 
  
> <span data-ttu-id="55495-111">ブックマークが正常に解放されました。</span><span class="sxs-lookup"><span data-stu-id="55495-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="55495-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="55495-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="55495-113">指定したブックマークが存在しません。</span><span class="sxs-lookup"><span data-stu-id="55495-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55495-114">注釈</span><span class="sxs-lookup"><span data-stu-id="55495-114">Remarks</span></span>

<span data-ttu-id="55495-115">**IMAPITable:: freebookmark**メソッドは、不要になったブックマークを解放します。</span><span class="sxs-lookup"><span data-stu-id="55495-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="55495-116">この呼び出しの後、ブックマークは無効になりました。</span><span class="sxs-lookup"><span data-stu-id="55495-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="55495-117">テーブルがメモリから解放されると、それに関連付けられているすべてのブックマークも解放されます。</span><span class="sxs-lookup"><span data-stu-id="55495-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="55495-118">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="55495-118">Notes to implementers</span></span>

<span data-ttu-id="55495-119">発信者が3つの定義済みブックマークのいずれかを_bkPosition_パラメーターに渡した場合は、要求を無視し、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="55495-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55495-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="55495-120">See also</span></span>



[<span data-ttu-id="55495-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="55495-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="55495-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55495-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

