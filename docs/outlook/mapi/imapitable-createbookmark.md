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
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800822"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="ee3f6-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="ee3f6-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="ee3f6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee3f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee3f6-105">テーブルの現在の位置にブックマークを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="ee3f6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ee3f6-106">Parameters</span></span>

 <span data-ttu-id="ee3f6-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="ee3f6-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="ee3f6-108">[out]返される 32 ビットのブックマークの値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="ee3f6-109">このブックマークは、後で[IMAPITable::SeekRow](imapitable-seekrow.md)メソッドの呼び出しに渡されます。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee3f6-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ee3f6-110">Return value</span></span>

<span data-ttu-id="ee3f6-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee3f6-111">S_OK</span></span> 
  
> <span data-ttu-id="ee3f6-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ee3f6-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ee3f6-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="ee3f6-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="ee3f6-114">要求された操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee3f6-115">備考</span><span class="sxs-lookup"><span data-stu-id="ee3f6-115">Remarks</span></span>

<span data-ttu-id="ee3f6-116">**IMAPITable::CreateBookmark**メソッドは、ブックマークと呼ばれる値を作成することによって、テーブルの位置をマークします。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="ee3f6-117">ブックマークで識別される位置に戻るには、ブックマークを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="ee3f6-118">ブックマークの位置は、テーブル内で行の位置にあるオブジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="ee3f6-119">、添付ファイル テーブルのブックマークがサポートされていませんし、 **CreateBookmark**の添付ファイル テーブルの実装は、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ee3f6-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ee3f6-120">Notes to implementers</span></span>

<span data-ttu-id="ee3f6-121">ブックマークとカーソルの位置を維持するためのメモリの経費のために作成できるブックマークの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="ee3f6-122">その番号が表示されたら、以降の呼び出しは**CreateBookmark**から MAPI_E_UNABLE_TO_COMPLETE を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="ee3f6-123">ブックマークは、不要になったテーブル ・ ビュー内にある行を指しています。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="ee3f6-124">呼び出し元は、このようなブックマークを使用する場合表示されている次の行にカーソルを移動し、停止があります。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="ee3f6-125">呼び出し元が縮小されたために、非表示の行を指しているブックマークを使用しようとするときは、ブックマークに移動した後 MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="ee3f6-126">表示されている次の行にブックマークの位置を変更するにはこの時点で、または**SetCollapseState**メソッドで発生した場合、縮小します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="ee3f6-127">正確に移動するとき、ブックマークされたかを示すブックマークのビットに保持する必要があります、行が折りたたまれている時にブックマークを移動する場合: その最後の使用から、または作成されてから使用されていない場合。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee3f6-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ee3f6-128">Notes to callers</span></span>

 <span data-ttu-id="ee3f6-129">**CreateBookmark**は、ブックマークを作成するためのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="ee3f6-130">[IMAPITable::FreeBookmark](imapitable-freebookmark.md)メソッドを呼び出すことによって、ブックマークのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="ee3f6-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee3f6-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee3f6-131">See also</span></span>



[<span data-ttu-id="ee3f6-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="ee3f6-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="ee3f6-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="ee3f6-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="ee3f6-134">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee3f6-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

