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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408825"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="26ddd-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="26ddd-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="26ddd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26ddd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26ddd-105">テーブルの現在の位置にブックマークを作成します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="26ddd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26ddd-106">Parameters</span></span>

 <span data-ttu-id="26ddd-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="26ddd-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="26ddd-108">[out]返される 32 ビットのブックマーク値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="26ddd-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="26ddd-109">このブックマークは、後で [IMAPITable::SeekRow メソッドへの呼び出しで渡](imapitable-seekrow.md) されます。</span><span class="sxs-lookup"><span data-stu-id="26ddd-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26ddd-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="26ddd-110">Return value</span></span>

<span data-ttu-id="26ddd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="26ddd-111">S_OK</span></span> 
  
> <span data-ttu-id="26ddd-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="26ddd-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="26ddd-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="26ddd-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="26ddd-114">要求された操作を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26ddd-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26ddd-115">注釈</span><span class="sxs-lookup"><span data-stu-id="26ddd-115">Remarks</span></span>

<span data-ttu-id="26ddd-116">**IMAPITable::CreateBookmark** メソッドは、ブックマークと呼ばれる値を作成して、テーブルの位置をマークします。</span><span class="sxs-lookup"><span data-stu-id="26ddd-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="26ddd-117">ブックマークを使用すると、ブックマークで識別された位置に戻ります。</span><span class="sxs-lookup"><span data-stu-id="26ddd-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="26ddd-118">ブックマークされた位置は、テーブル内のその行のオブジェクトに関連付けされます。</span><span class="sxs-lookup"><span data-stu-id="26ddd-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="26ddd-119">ブックマークは、添付ファイル テーブルではサポートされていません。 **また、CreateBookmark** 戻り値の添付ファイル テーブルの実装MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="26ddd-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="26ddd-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="26ddd-120">Notes to implementers</span></span>

<span data-ttu-id="26ddd-121">ブックマークを使用してカーソル位置を維持する場合のメモリコストが大きいので、作成できるブックマークの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="26ddd-122">その番号に達すると、それ以降のすべての呼びMAPI_E_UNABLE_TO_COMPLETEから **CreateBookmark** を返します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="26ddd-123">ブックマークは、テーブル ビューに含めなくなった行をポイントする場合があります。</span><span class="sxs-lookup"><span data-stu-id="26ddd-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="26ddd-124">呼び出し元がこのようなブックマークを使用する場合は、カーソルを次の表示行に移動して、そこで停止します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="26ddd-125">呼び出し元が、折りたたむため、表示できない行を指しているブックマークを使用しようとすると、ブックマークを移動した後MAPI_W_POSITION_CHANGEDを返します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="26ddd-126">この時点で、または **SetCollapseState** メソッドで折りたたみが発生した場合に、ブックマークを次の表示行に再配置できます。</span><span class="sxs-lookup"><span data-stu-id="26ddd-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="26ddd-127">行が折りたたみ時にブックマークを移動する場合は、ブックマークが移動された時刻を正確に示すブックマーク (最後の使用以降、または作成後に使用されたことがない場合) を示す少しを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26ddd-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26ddd-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="26ddd-128">Notes to callers</span></span>

 <span data-ttu-id="26ddd-129">**CreateBookmark は** 、作成するブックマークのメモリを割り当てる。</span><span class="sxs-lookup"><span data-stu-id="26ddd-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="26ddd-130">[IMAPITable::FreeBookmark](imapitable-freebookmark.md)メソッドを呼び出して、ブックマークのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="26ddd-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26ddd-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="26ddd-131">See also</span></span>



[<span data-ttu-id="26ddd-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="26ddd-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="26ddd-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="26ddd-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="26ddd-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26ddd-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

