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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 36d1518764985c4783d967e263ca5c05d63f935f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588483"
---
# <a name="imapitablefreebookmark"></a><span data-ttu-id="d1ab7-103">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="d1ab7-103">IMAPITable::FreeBookmark</span></span>

  
  
<span data-ttu-id="d1ab7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1ab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1ab7-105">ブックマークに関連付けられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-105">Releases the memory associated with a bookmark.</span></span>
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="d1ab7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1ab7-106">Parameters</span></span>

 <span data-ttu-id="d1ab7-107">_bkPosition_</span><span class="sxs-lookup"><span data-stu-id="d1ab7-107">_bkPosition_</span></span>
  
> <span data-ttu-id="d1ab7-108">[in]解放するには、ブックマークは、 [IMAPITable::CreateBookmark](imapitable-createbookmark.md)メソッドを呼び出すことによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-108">[in] The bookmark to be freed, created by calling the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d1ab7-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d1ab7-109">Return value</span></span>

<span data-ttu-id="d1ab7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1ab7-110">S_OK</span></span> 
  
> <span data-ttu-id="d1ab7-111">ブックマークが正常に解放されました。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-111">The bookmark was successfully freed.</span></span>
    
<span data-ttu-id="d1ab7-112">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="d1ab7-112">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="d1ab7-113">指定されたブックマークは存在しません。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-113">The specified bookmark does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1ab7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d1ab7-114">Remarks</span></span>

<span data-ttu-id="d1ab7-115">**IMAPITable::FreeBookmark**メソッドでは、不要になったブックマークを解放します。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-115">The **IMAPITable::FreeBookmark** method releases a bookmark that is no longer needed.</span></span> <span data-ttu-id="d1ab7-116">ブックマークは、この呼び出しの後は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-116">The bookmark is no longer valid after this call.</span></span> <span data-ttu-id="d1ab7-117">テーブルがメモリからリリースされる、すべての関連付けられているブックマークのも解放されます。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-117">Whenever a table is released from memory, all of its associated bookmarks are also released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d1ab7-118">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d1ab7-118">Notes to implementers</span></span>

<span data-ttu-id="d1ab7-119">呼び出し元では、 _bkPosition_パラメーターで次の 3 つの定義済みのブックマークの 1 つが成功した場合は、要求を無視して、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="d1ab7-119">If the caller passes one of the three predefined bookmarks in the  _bkPosition_ parameter, ignore the request and return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1ab7-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1ab7-120">See also</span></span>



[<span data-ttu-id="d1ab7-121">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="d1ab7-121">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="d1ab7-122">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1ab7-122">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

