---
title: IMAPISessionGetMsgStoresTable
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
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="82598-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="82598-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="82598-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82598-105">セッション プロファイル内のすべてのメッセージ ストアに関する情報を含むメッセージ ストア テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="82598-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="82598-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82598-106">Parameters</span></span>

 <span data-ttu-id="82598-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82598-107">_ulFlags_</span></span>
  
> <span data-ttu-id="82598-108">[in]文字列である列の形式を決定するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="82598-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="82598-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="82598-109">The following flag can be set:</span></span>
    
<span data-ttu-id="82598-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="82598-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="82598-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="82598-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="82598-112">このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="82598-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="82598-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="82598-113">_lppTable_</span></span>
  
> <span data-ttu-id="82598-114">[out]メッセージ ストア テーブルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="82598-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82598-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="82598-115">Return value</span></span>

<span data-ttu-id="82598-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="82598-116">S_OK</span></span> 
  
> <span data-ttu-id="82598-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="82598-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="82598-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="82598-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="82598-119">このMAPI_UNICODEが設定され、セッションは Unicode をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="82598-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82598-120">注釈</span><span class="sxs-lookup"><span data-stu-id="82598-120">Remarks</span></span>

<span data-ttu-id="82598-121">**IMAPISession::GetMsgStoresTable** メソッドは、プロファイル内の開いている各メッセージ ストアに関する情報を含む MAPI によって管理されるテーブルであるメッセージ ストア テーブルへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="82598-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="82598-122">メッセージ ストア テーブルの必須列と省略可能列の完全な一覧については、「メッセージ ストア テーブル」 [を参照してください](message-store-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="82598-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82598-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="82598-123">Notes to callers</span></span>

<span data-ttu-id="82598-124">MAPI は、変更が発生するたびにセッション中にメッセージ ストア テーブルを更新しますので、メッセージ ストア テーブルの **Advise** メソッドを呼び出して、これらの変更の通知を受け取る登録を行います。</span><span class="sxs-lookup"><span data-stu-id="82598-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="82598-125">可能な変更には、新しいメッセージ ストアの追加、既存のストアの削除、既定のストアへの変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="82598-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="82598-126">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="82598-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="82598-127">このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="82598-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82598-128">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="82598-128">MFCMAPI reference</span></span>

<span data-ttu-id="82598-129">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82598-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82598-130">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="82598-130">**File**</span></span>|<span data-ttu-id="82598-131">**関数**</span><span class="sxs-lookup"><span data-stu-id="82598-131">**Function**</span></span>|<span data-ttu-id="82598-132">**コメント**</span><span class="sxs-lookup"><span data-stu-id="82598-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82598-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="82598-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="82598-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="82598-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="82598-135">MFCMAPI は **IMAPISession::GetMsgStoresTable** メソッドを使用してメッセージ ストア テーブルを取得し、MFCMAPI のメイン ダイアログ ボックスで表示できます。</span><span class="sxs-lookup"><span data-stu-id="82598-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82598-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="82598-136">See also</span></span>



[<span data-ttu-id="82598-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="82598-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="82598-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82598-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="82598-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="82598-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="82598-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="82598-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="82598-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="82598-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="82598-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="82598-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="82598-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="82598-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="82598-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82598-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="82598-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="82598-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="82598-146">メッセージ ストア テーブル</span><span class="sxs-lookup"><span data-stu-id="82598-146">Message Store Tables</span></span>](message-store-tables.md)

