---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5e9135a52c15c18b70116aaf52e1ee63af413673
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563850"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="eb0f2-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="eb0f2-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="eb0f2-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb0f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb0f2-105">テーブルの現在の位置にブックマークを作成します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="eb0f2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eb0f2-106">Parameters</span></span>

 <span data-ttu-id="eb0f2-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="eb0f2-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="eb0f2-108">[out]返される 32 ビットのブックマークの値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="eb0f2-109">このブックマークは、後で[IMAPITable::SeekRow](imapitable-seekrow.md)メソッドの呼び出しに渡されます。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb0f2-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="eb0f2-110">Return value</span></span>

<span data-ttu-id="eb0f2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb0f2-111">S_OK</span></span> 
  
> <span data-ttu-id="eb0f2-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="eb0f2-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eb0f2-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="eb0f2-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="eb0f2-114">要求された操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb0f2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="eb0f2-115">Remarks</span></span>

<span data-ttu-id="eb0f2-116">**IMAPITable::CreateBookmark**メソッドは、ブックマークと呼ばれる値を作成することによって、テーブルの位置をマークします。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="eb0f2-117">ブックマークで識別される位置に戻るには、ブックマークを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="eb0f2-118">ブックマークの位置は、テーブル内で行の位置にあるオブジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="eb0f2-119">、添付ファイル テーブルのブックマークがサポートされていませんし、 **CreateBookmark**の添付ファイル テーブルの実装は、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eb0f2-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="eb0f2-120">Notes to implementers</span></span>

<span data-ttu-id="eb0f2-121">ブックマークとカーソルの位置を維持するためのメモリの経費のために作成できるブックマークの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="eb0f2-122">その番号が表示されたら、以降の呼び出しは**CreateBookmark**から MAPI_E_UNABLE_TO_COMPLETE を返します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="eb0f2-123">ブックマークは、不要になったテーブル ・ ビュー内にある行を指しています。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="eb0f2-124">呼び出し元は、このようなブックマークを使用する場合表示されている次の行にカーソルを移動し、停止があります。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="eb0f2-125">呼び出し元が縮小されたために、非表示の行を指しているブックマークを使用しようとするときは、ブックマークに移動した後 MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="eb0f2-126">表示されている次の行にブックマークの位置を変更するにはこの時点で、または**SetCollapseState**メソッドで発生した場合、縮小します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="eb0f2-127">正確に移動するとき、ブックマークされたかを示すブックマークのビットに保持する必要があります、行が折りたたまれている時にブックマークを移動する場合: その最後の使用から、または作成されてから使用されていない場合。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb0f2-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="eb0f2-128">Notes to callers</span></span>

 <span data-ttu-id="eb0f2-129">**CreateBookmark**は、ブックマークを作成するためのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="eb0f2-130">[IMAPITable::FreeBookmark](imapitable-freebookmark.md)メソッドを呼び出すことによって、ブックマークのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="eb0f2-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb0f2-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb0f2-131">See also</span></span>



[<span data-ttu-id="eb0f2-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="eb0f2-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="eb0f2-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="eb0f2-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="eb0f2-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb0f2-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

