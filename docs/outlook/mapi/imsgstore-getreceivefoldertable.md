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
ms.openlocfilehash: 681fd68fc068633912df1cb7f060b8c4111b5de8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566538"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="963e5-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="963e5-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="963e5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="963e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="963e5-105">受信フォルダーのテーブルのすべてのメッセージ ストアの受信フォルダーに関する情報が含まれるテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="963e5-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="963e5-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="963e5-106">Parameters</span></span>

 <span data-ttu-id="963e5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="963e5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="963e5-108">[in]テーブルのアクセスを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="963e5-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="963e5-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="963e5-109">The following flags can be set:</span></span>
    
<span data-ttu-id="963e5-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="963e5-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="963e5-111">正常に戻す、可能性のあるテーブルは、呼び出し元に完全に利用できる前に**GetReceiveFolderTable**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="963e5-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="963e5-112">テーブルを完全に使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="963e5-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="963e5-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="963e5-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="963e5-114">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="963e5-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="963e5-115">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="963e5-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="963e5-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="963e5-116">_lppTable_</span></span>
  
> <span data-ttu-id="963e5-117">[out]フォルダーの受信表へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="963e5-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="963e5-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="963e5-118">Return value</span></span>

<span data-ttu-id="963e5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="963e5-119">S_OK</span></span> 
  
> <span data-ttu-id="963e5-120">受信フォルダーのテーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="963e5-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="963e5-121">注釈</span><span class="sxs-lookup"><span data-stu-id="963e5-121">Remarks</span></span>

<span data-ttu-id="963e5-122">**IMsgStore::GetReceiveFolderTable**メソッドは、すべてのメッセージ ストアのプロパティの設定値が表示されるフォルダーを表示するテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="963e5-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="963e5-123">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="963e5-123">Notes to implementers</span></span>

<span data-ttu-id="963e5-124">受信フォルダー テーブルで必要な列の一覧、[フォルダーのテーブルに表示される](receive-folder-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="963e5-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="963e5-125">実装、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティのプロパティの制限の設定をサポートするためにフォルダーのテーブルを表示します。</span><span class="sxs-lookup"><span data-stu-id="963e5-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="963e5-126">このを有効に簡単にアクセスする特定のフォルダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="963e5-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="963e5-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="963e5-127">Notes to callers</span></span>

<span data-ttu-id="963e5-128">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="963e5-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="963e5-129">このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="963e5-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="963e5-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="963e5-130">MFCMAPI reference</span></span>

<span data-ttu-id="963e5-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="963e5-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="963e5-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="963e5-132">**File**</span></span>|<span data-ttu-id="963e5-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="963e5-133">**Function**</span></span>|<span data-ttu-id="963e5-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="963e5-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="963e5-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="963e5-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="963e5-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="963e5-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="963e5-137">MFCMAPI では、 **IMsgStore::GetReceiveFolderTable**メソッドを使用して、表示する受信フォルダーのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="963e5-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="963e5-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="963e5-138">See also</span></span>



[<span data-ttu-id="963e5-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="963e5-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="963e5-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="963e5-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="963e5-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="963e5-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="963e5-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="963e5-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="963e5-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="963e5-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="963e5-144">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="963e5-144">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

