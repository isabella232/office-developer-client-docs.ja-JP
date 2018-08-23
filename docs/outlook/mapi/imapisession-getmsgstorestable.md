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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc0039cf2210446704d25b2156bd4ff50041a524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586278"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="6ac5c-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="6ac5c-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="6ac5c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ac5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ac5c-105">セッション ・ プロファイル内のすべてのメッセージ ・ ストアに関する情報を含むメッセージ ストアのテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6ac5c-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6ac5c-106">Parameters</span></span>

 <span data-ttu-id="6ac5c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ac5c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6ac5c-108">[in]文字の文字列の列の形式を決定するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="6ac5c-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6ac5c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ac5c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6ac5c-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6ac5c-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6ac5c-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6ac5c-113">_lppTable_</span></span>
  
> <span data-ttu-id="6ac5c-114">[out]メッセージ ストアのテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ac5c-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6ac5c-115">Return value</span></span>

<span data-ttu-id="6ac5c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ac5c-116">S_OK</span></span> 
  
> <span data-ttu-id="6ac5c-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="6ac5c-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6ac5c-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6ac5c-119">MAPI_UNICODE フラグが設定され、セッションが Unicode をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ac5c-120">注釈</span><span class="sxs-lookup"><span data-stu-id="6ac5c-120">Remarks</span></span>

<span data-ttu-id="6ac5c-121">**IMAPISession::GetMsgStoresTable**メソッドは、メッセージ ストアのテーブルへのポインターを取得、テーブルが管理している MAPI プロファイル内の各の開いているメッセージ ストアについての情報が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="6ac5c-122">テーブルを格納、メッセージの必須およびオプションの列の一覧については、[メッセージ ストアのテーブル](message-store-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6ac5c-123">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6ac5c-123">Notes to callers</span></span>

<span data-ttu-id="6ac5c-124">MAPI は、変更が発生するたびに、セッション中に、メッセージ ストアのテーブルを更新、ため **、メッセージ ストアのテーブルのこれらの変更の通知を登録するメソッド**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="6ac5c-125">行われた変更は、新しいメッセージ ストアの追加、削除、既存のストア、および、既定のストアに変更します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="6ac5c-126">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="6ac5c-127">このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6ac5c-128">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="6ac5c-128">MFCMAPI reference</span></span>

<span data-ttu-id="6ac5c-129">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="6ac5c-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6ac5c-130">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="6ac5c-130">**File**</span></span>|<span data-ttu-id="6ac5c-131">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="6ac5c-131">**Function**</span></span>|<span data-ttu-id="6ac5c-132">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="6ac5c-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ac5c-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6ac5c-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6ac5c-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="6ac5c-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="6ac5c-135">MFCMAPI では、 **IMAPISession::GetMsgStoresTable**メソッドを使用して、MFCMAPI のメイン ダイアログ ボックスでレンダリングできるように、メッセージ ストアのテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="6ac5c-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ac5c-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ac5c-136">See also</span></span>



[<span data-ttu-id="6ac5c-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="6ac5c-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="6ac5c-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ac5c-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="6ac5c-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="6ac5c-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="6ac5c-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6ac5c-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="6ac5c-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="6ac5c-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="6ac5c-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6ac5c-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6ac5c-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6ac5c-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="6ac5c-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ac5c-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="6ac5c-145">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="6ac5c-145">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="6ac5c-146">メッセージ ストア テーブル</span><span class="sxs-lookup"><span data-stu-id="6ac5c-146">Message Store Tables</span></span>](message-store-tables.md)

