---
title: imapisessiongetmsgstorestable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428138"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="130e5-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="130e5-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="130e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="130e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="130e5-105">セッションプロファイル内のすべてのメッセージストアに関する情報を含むメッセージストアテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="130e5-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="130e5-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="130e5-106">Parameters</span></span>

 <span data-ttu-id="130e5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="130e5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="130e5-108">順番文字列の列の形式を決定するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="130e5-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="130e5-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="130e5-109">The following flag can be set:</span></span>
    
<span data-ttu-id="130e5-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="130e5-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="130e5-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="130e5-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="130e5-112">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="130e5-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="130e5-113">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="130e5-113">_lppTable_</span></span>
  
> <span data-ttu-id="130e5-114">読み上げメッセージストアテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="130e5-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="130e5-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="130e5-115">Return value</span></span>

<span data-ttu-id="130e5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="130e5-116">S_OK</span></span> 
  
> <span data-ttu-id="130e5-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="130e5-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="130e5-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="130e5-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="130e5-119">MAPI_UNICODE フラグが設定されていて、セッションは UNICODE をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="130e5-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="130e5-120">注釈</span><span class="sxs-lookup"><span data-stu-id="130e5-120">Remarks</span></span>

<span data-ttu-id="130e5-121">**imapisession:: getmsgstorestable**メソッドは、メッセージストアテーブルへのポインターを取得します。このテーブルは、プロファイル内の開いている各メッセージストアに関する情報を含む MAPI によって保持されます。</span><span class="sxs-lookup"><span data-stu-id="130e5-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="130e5-122">メッセージストアテーブルの必須およびオプションの列の完全な一覧については、「 [message store Tables](message-store-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="130e5-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="130e5-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="130e5-123">Notes to callers</span></span>

<span data-ttu-id="130e5-124">MAPI は、セッション中に変更が発生するたびにメッセージストアテーブルを更新するので、メッセージストアテーブルの**Advise**メソッドを呼び出して、これらの変更について通知されるように登録します。</span><span class="sxs-lookup"><span data-stu-id="130e5-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="130e5-125">変更できるのは、新しいメッセージストアの追加、既存のストアの削除、および既定のストアに対する変更です。</span><span class="sxs-lookup"><span data-stu-id="130e5-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="130e5-126">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="130e5-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="130e5-127">このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="130e5-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="130e5-128">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="130e5-128">MFCMAPI reference</span></span>

<span data-ttu-id="130e5-129">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="130e5-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="130e5-130">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="130e5-130">**File**</span></span>|<span data-ttu-id="130e5-131">**関数**</span><span class="sxs-lookup"><span data-stu-id="130e5-131">**Function**</span></span>|<span data-ttu-id="130e5-132">**コメント**</span><span class="sxs-lookup"><span data-stu-id="130e5-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="130e5-133">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="130e5-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="130e5-134">CMainDlg:: onopenmessagestoretable</span><span class="sxs-lookup"><span data-stu-id="130e5-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="130e5-135">mfcmapi は、 **imapisession:: getmsgstorestable**メソッドを使用して、メッセージストアテーブルを取得して、mfcmapi のメインダイアログボックスに表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="130e5-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="130e5-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="130e5-136">See also</span></span>



[<span data-ttu-id="130e5-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="130e5-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="130e5-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="130e5-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="130e5-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="130e5-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="130e5-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="130e5-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="130e5-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="130e5-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="130e5-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="130e5-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="130e5-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="130e5-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="130e5-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="130e5-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="130e5-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="130e5-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="130e5-146">メッセージストアテーブル</span><span class="sxs-lookup"><span data-stu-id="130e5-146">Message Store Tables</span></span>](message-store-tables.md)

