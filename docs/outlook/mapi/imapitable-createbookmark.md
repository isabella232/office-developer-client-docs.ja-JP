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
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="7b712-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="7b712-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="7b712-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b712-105">表の現在の位置にブックマークを作成します。</span><span class="sxs-lookup"><span data-stu-id="7b712-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="7b712-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7b712-106">Parameters</span></span>

 <span data-ttu-id="7b712-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="7b712-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="7b712-108">読み上げ返される32ビットのブックマーク値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7b712-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="7b712-109">このブックマークは、後で[IMAPITable:: seekrow](imapitable-seekrow.md)メソッドを呼び出して渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7b712-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b712-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="7b712-110">Return value</span></span>

<span data-ttu-id="7b712-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b712-111">S_OK</span></span> 
  
> <span data-ttu-id="7b712-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="7b712-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7b712-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="7b712-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="7b712-114">要求された操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7b712-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b712-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7b712-115">Remarks</span></span>

<span data-ttu-id="7b712-116">**IMAPITable:: createbookmark**メソッドは、ブックマークと呼ばれる値を作成して、テーブルの位置を示します。</span><span class="sxs-lookup"><span data-stu-id="7b712-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="7b712-117">ブックマークを使用すると、ブックマークで指定した位置に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="7b712-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="7b712-118">ブックマーク位置は、テーブルのその行にあるオブジェクトに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7b712-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="7b712-119">ブックマークは、添付ファイルテーブルではサポートされておらず、 **createbookmark** return MAPI_E_NO_SUPPORT の添付ファイルテーブルの実装ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7b712-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7b712-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7b712-120">Notes to implementers</span></span>

<span data-ttu-id="7b712-121">ブックマークを使用してカーソル位置を維持するためのメモリ費用があるため、作成できるブックマークの数を制限します。</span><span class="sxs-lookup"><span data-stu-id="7b712-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="7b712-122">その番号に達すると、それ以降のすべての呼び出しから**createbookmark**に MAPI_E_UNABLE_TO_COMPLETE が返されます。</span><span class="sxs-lookup"><span data-stu-id="7b712-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="7b712-123">ブックマークがテーブルビューに表示されなくなった行を指している場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b712-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="7b712-124">呼び出し元がこのようなブックマークを使用する場合は、カーソルを次の表示行に移動し、そこで停止します。</span><span class="sxs-lookup"><span data-stu-id="7b712-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="7b712-125">非表示になっているために、呼び出し元がブックマークを使用しようとした場合は、ブックマークを移動した後に MAPI_W_POSITION_CHANGED を返します。</span><span class="sxs-lookup"><span data-stu-id="7b712-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="7b712-126">この時点で、または**SetCollapseState**メソッドで折りたたみが行われるときに、ブックマークを次の表示可能な行に再配置することができます。</span><span class="sxs-lookup"><span data-stu-id="7b712-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="7b712-127">行が折りたたまれたときにブックマークを移動した場合は、ブックマークが最後に使用された日時、または作成後に使用されていないかどうかを示す、ブックマークのビットを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b712-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7b712-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7b712-128">Notes to callers</span></span>

 <span data-ttu-id="7b712-129">**createbookmark**は、作成するブックマークのメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7b712-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="7b712-130">[IMAPITable:: freebookmark](imapitable-freebookmark.md)メソッドを呼び出して、ブックマークのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="7b712-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b712-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="7b712-131">See also</span></span>



[<span data-ttu-id="7b712-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="7b712-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="7b712-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="7b712-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="7b712-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b712-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

