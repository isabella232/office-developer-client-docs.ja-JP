---
title: imapisessionsetdefaultstore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426108"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="b8385-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="b8385-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="b8385-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8385-105">セッションの既定のメッセージストアとしてメッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="b8385-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="b8385-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b8385-106">Parameters</span></span>

 <span data-ttu-id="b8385-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8385-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b8385-108">順番既定のメッセージストアの設定を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b8385-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="b8385-109">これらのフラグは相互に排他的です。設定できるのは、次に示すフラグのいずれか1つだけです。</span><span class="sxs-lookup"><span data-stu-id="b8385-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="b8385-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="b8385-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="b8385-111">セッションの既定値としてメッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="b8385-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="b8385-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 列の STATUS_DEFAULT_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="b8385-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="b8385-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="b8385-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="b8385-114">ログオン時に使用するストアとして、メッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="b8385-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="b8385-115">メッセージストアが既定のストアではない場合、クライアントは既定のストアにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8385-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="b8385-116">**PR_RESOURCE_FLAGS**列の STATUS_PRIMARY_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="b8385-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="b8385-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="b8385-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="b8385-118">プライマリメッセージストアが使用できない場合に、ログオン時に使用するストアとしてメッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="b8385-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="b8385-119">クライアントがプライマリストアを開くことができない場合は、セカンダリストアを開き、既定として設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8385-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="b8385-120">**PR_RESOURCE_FLAGS**列の STATUS_SECONDARY_STORE フラグを設定して、メッセージストアの状態テーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="b8385-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="b8385-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="b8385-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="b8385-122">[状態] テーブル行、メッセージストアテーブル行、およびセッションプロファイルで、メッセージストアの**PR_RESOURCE_FLAGS**プロパティの STATUS_SIMPLE_STORE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="b8385-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="b8385-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="b8385-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="b8385-124">STATUS_SIMPLE_STORE フラグを、状態テーブルの行とメッセージストアの表の行の**PR_RESOURCE_FLAGS**プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="b8385-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="b8385-125">プロファイルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b8385-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="b8385-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8385-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="b8385-127">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b8385-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b8385-128">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="b8385-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="b8385-129">順番既定として使用するメッセージストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b8385-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="b8385-130">クライアントが_lな tryid_で NULL を渡す場合、既定としてメッセージストアが選択されていません。</span><span class="sxs-lookup"><span data-stu-id="b8385-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8385-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="b8385-131">Return value</span></span>

<span data-ttu-id="b8385-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8385-132">S_OK</span></span> 
  
> <span data-ttu-id="b8385-133">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="b8385-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8385-134">注釈</span><span class="sxs-lookup"><span data-stu-id="b8385-134">Remarks</span></span>

<span data-ttu-id="b8385-135">**imapisession:: setdefaultstore**メソッドは、次のいずれかのようにメッセージストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="b8385-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="b8385-136">セッションの既定のメッセージストア。</span><span class="sxs-lookup"><span data-stu-id="b8385-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="b8385-137">セッションのプライマリメッセージストア。</span><span class="sxs-lookup"><span data-stu-id="b8385-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="b8385-138">セッションのセカンダリメッセージストア。</span><span class="sxs-lookup"><span data-stu-id="b8385-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="b8385-139">メッセージストアを既定として設定するには、メッセージストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに次のフラグが設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8385-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="b8385-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="b8385-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="b8385-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="b8385-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="b8385-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="b8385-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="b8385-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b8385-143">Notes to callers</span></span>

<span data-ttu-id="b8385-144">[状態] テーブルを取得し、 **PR_RESOURCE_FLAGS**列の STATUS_DEFAULT_STORE フラグの設定を検索することによって、セッションの既定のメッセージストアを判別できます。</span><span class="sxs-lookup"><span data-stu-id="b8385-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="b8385-145">この設定の行は、セッションの既定値として指定されたメッセージストアを表します。</span><span class="sxs-lookup"><span data-stu-id="b8385-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="b8385-146">MAPI_DEFAULT_STORE または MAPI_SIMPLE_STORE_PERMANENT フラグが設定されている場合は、MAPI がプロファイル、メッセージストアテーブル、および状態テーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="b8385-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="b8385-147">メッセージストアの既定の設定が変更されるたびに、次の通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b8385-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="b8385-148">**fnevTableModified**イベント通知は、メッセージストアと状態テーブルの両方の影響を受ける各行に対して発行されます。</span><span class="sxs-lookup"><span data-stu-id="b8385-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="b8385-149">MAPI スプーラーに内部通知が発行されます。</span><span class="sxs-lookup"><span data-stu-id="b8385-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="b8385-150">進行中の操作は、変更されずに完了します。既定のメッセージストア (メッセージのダウンロードなど) に関連する新しい操作は、新しい既定のストアに対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="b8385-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8385-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b8385-151">MFCMAPI reference</span></span>

<span data-ttu-id="b8385-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8385-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8385-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b8385-153">**File**</span></span>|<span data-ttu-id="b8385-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="b8385-154">**Function**</span></span>|<span data-ttu-id="b8385-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b8385-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8385-156">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="b8385-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b8385-157">CMainDlg:: OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="b8385-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="b8385-158">mfcmapi は、 **imapisession:: setdefaultstore**メソッドを使用して、選択されたストアを既定のストアとして設定します。</span><span class="sxs-lookup"><span data-stu-id="b8385-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8385-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8385-159">See also</span></span>



[<span data-ttu-id="b8385-160">PidTagResourceFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8385-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="b8385-161">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8385-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="b8385-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b8385-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="b8385-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8385-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="b8385-164">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b8385-164">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

