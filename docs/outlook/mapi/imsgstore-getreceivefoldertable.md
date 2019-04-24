---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317354"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="a1952-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="a1952-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="a1952-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1952-105">受信フォルダーテーブル (メッセージストアのすべての受信フォルダーに関する情報を含むテーブル) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a1952-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="a1952-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1952-106">Parameters</span></span>

 <span data-ttu-id="a1952-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1952-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a1952-108">順番テーブルアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a1952-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="a1952-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a1952-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a1952-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a1952-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a1952-111">呼び出し元がテーブルを完全に使用できるようになる前に、 **getreceivefoldertable**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="a1952-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="a1952-112">テーブルが完全に使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1952-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="a1952-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1952-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a1952-114">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a1952-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a1952-115">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a1952-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a1952-116">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="a1952-116">_lppTable_</span></span>
  
> <span data-ttu-id="a1952-117">読み上げ受信フォルダーテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1952-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1952-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1952-118">Return value</span></span>

<span data-ttu-id="a1952-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1952-119">S_OK</span></span> 
  
> <span data-ttu-id="a1952-120">受信フォルダーテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="a1952-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1952-121">解説</span><span class="sxs-lookup"><span data-stu-id="a1952-121">Remarks</span></span>

<span data-ttu-id="a1952-122">**IMsgStore:: getreceivefoldertable**メソッドは、すべてのメッセージストアの受信フォルダーのプロパティ設定を示すテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a1952-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a1952-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a1952-123">Notes to implementers</span></span>

<span data-ttu-id="a1952-124">受信フォルダーテーブルに必要な列の一覧については、「[受信フォルダーテーブル](receive-folder-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1952-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="a1952-125">受信フォルダーテーブルを実装して、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティのプロパティ制限の設定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a1952-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a1952-126">これにより、特定の受信フォルダーへのアクセスが容易になります。</span><span class="sxs-lookup"><span data-stu-id="a1952-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1952-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a1952-127">Notes to callers</span></span>

<span data-ttu-id="a1952-128">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="a1952-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a1952-129">このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="a1952-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1952-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a1952-130">MFCMAPI reference</span></span>

<span data-ttu-id="a1952-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1952-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1952-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a1952-132">**File**</span></span>|<span data-ttu-id="a1952-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="a1952-133">**Function**</span></span>|<span data-ttu-id="a1952-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a1952-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1952-135">MsgStoreDlg</span><span class="sxs-lookup"><span data-stu-id="a1952-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a1952-136">CMsgStoreDlg:: ondisplayreceivefoldertable</span><span class="sxs-lookup"><span data-stu-id="a1952-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="a1952-137">mfcmapi は、 **IMsgStore:: getreceivefoldertable**メソッドを使用して、表示する受信フォルダーテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="a1952-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1952-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1952-138">See also</span></span>



[<span data-ttu-id="a1952-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a1952-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a1952-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a1952-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a1952-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a1952-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a1952-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a1952-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a1952-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a1952-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="a1952-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a1952-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

