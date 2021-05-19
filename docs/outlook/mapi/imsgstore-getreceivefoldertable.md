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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421355"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="37d61-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="37d61-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="37d61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37d61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37d61-105">メッセージ ストアのすべての受信フォルダーに関する情報を含む、受信フォルダー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="37d61-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="37d61-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37d61-106">Parameters</span></span>

 <span data-ttu-id="37d61-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37d61-107">_ulFlags_</span></span>
  
> <span data-ttu-id="37d61-108">[in]テーブル アクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="37d61-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="37d61-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37d61-109">The following flags can be set:</span></span>
    
<span data-ttu-id="37d61-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="37d61-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="37d61-111">**GetReceiveFolderTable** は、テーブルが呼び出し元で完全に使用できる前に、正常に戻ります。</span><span class="sxs-lookup"><span data-stu-id="37d61-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="37d61-112">テーブルが完全に使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="37d61-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="37d61-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37d61-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="37d61-114">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="37d61-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="37d61-115">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="37d61-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="37d61-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="37d61-116">_lppTable_</span></span>
  
> <span data-ttu-id="37d61-117">[out]受信フォルダー テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37d61-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37d61-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="37d61-118">Return value</span></span>

<span data-ttu-id="37d61-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="37d61-119">S_OK</span></span> 
  
> <span data-ttu-id="37d61-120">受信フォルダー テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="37d61-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37d61-121">注釈</span><span class="sxs-lookup"><span data-stu-id="37d61-121">Remarks</span></span>

<span data-ttu-id="37d61-122">**IMsgStore::GetReceiveFolderTable** メソッドは、メッセージ ストアのすべての受信フォルダーのプロパティ設定を示すテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="37d61-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="37d61-123">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="37d61-123">Notes to implementers</span></span>

<span data-ttu-id="37d61-124">受信フォルダー テーブルで必要な列の一覧については、「受信フォルダー テーブル [」を参照してください](receive-folder-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="37d61-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="37d61-125">受信フォルダー テーブルを実装して、プロパティ制限 [(PidTagRecordKey)](pidtagrecordkey-canonical-property.md)プロパティ **PR_RECORD_KEY設定を** サポートします。</span><span class="sxs-lookup"><span data-stu-id="37d61-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="37d61-126">これにより、特定の受信フォルダーに簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="37d61-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="37d61-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="37d61-127">Notes to callers</span></span>

<span data-ttu-id="37d61-128">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="37d61-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="37d61-129">このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="37d61-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37d61-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="37d61-130">MFCMAPI reference</span></span>

<span data-ttu-id="37d61-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37d61-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37d61-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="37d61-132">**File**</span></span>|<span data-ttu-id="37d61-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="37d61-133">**Function**</span></span>|<span data-ttu-id="37d61-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="37d61-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37d61-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="37d61-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="37d61-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="37d61-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="37d61-137">MFCMAPI は **、IMsgStore::GetReceiveFolderTable** メソッドを使用して、表示する受信フォルダー テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="37d61-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37d61-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="37d61-138">See also</span></span>



[<span data-ttu-id="37d61-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="37d61-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="37d61-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="37d61-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="37d61-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="37d61-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="37d61-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="37d61-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="37d61-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="37d61-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="37d61-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="37d61-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

