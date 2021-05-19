---
title: IMAPISessionSetDefaultStore
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
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="de903-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="de903-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="de903-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de903-105">セッションの既定のメッセージ ストアとしてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="de903-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="de903-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="de903-106">Parameters</span></span>

 <span data-ttu-id="de903-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de903-107">_ulFlags_</span></span>
  
> <span data-ttu-id="de903-108">[in]既定のメッセージ ストアの設定を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="de903-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="de903-109">これらのフラグは相互に排他的です。設定できるフラグは次の 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="de903-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="de903-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="de903-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="de903-111">セッションの既定値としてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="de903-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="de903-112">メッセージ ストアの状態テーブル行を更新するには、STATUS_DEFAULT_STORE **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 列の PR_RESOURCE_FLAGS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="de903-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="de903-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="de903-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="de903-114">ログオン時に使用するストアとしてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="de903-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="de903-115">メッセージ ストアが既定のストアではない場合、クライアントは既定のストアにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de903-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="de903-116">メッセージ ストアの状態テーブルの行を更新するには、STATUS_PRIMARY_STORE列の [PR_RESOURCE_FLAGS] **フラグをPR_RESOURCE_FLAGS** します。</span><span class="sxs-lookup"><span data-stu-id="de903-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="de903-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="de903-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="de903-118">プライマリ メッセージ ストアが使用できない場合、ログオン時に使用するストアとしてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="de903-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="de903-119">クライアントがプライマリ ストアを開けできない場合は、セカンダリ ストアを開き、既定として設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de903-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="de903-120">メッセージ ストアの状態テーブルの行を更新するには、STATUS_SECONDARY_STORE列の [PR_RESOURCE_FLAGS] **フラグをPR_RESOURCE_FLAGS** します。</span><span class="sxs-lookup"><span data-stu-id="de903-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="de903-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="de903-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="de903-122">メッセージ ストアの STATUS_SIMPLE_STORE プロパティの状態テーブル行、メッセージ ストア **テーブル行、および** セッション プロファイルの PR_RESOURCE_FLAGS フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="de903-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="de903-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="de903-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="de903-124">メッセージ ストアのSTATUS_SIMPLE_STOREのステータス テーブル行とメッセージ ストア **テーブル行** PR_RESOURCE_FLAGSプロパティのプロパティのフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="de903-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="de903-125">プロファイルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="de903-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="de903-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="de903-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="de903-127">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="de903-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="de903-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="de903-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="de903-129">[in]既定のメッセージ ストアのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="de903-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="de903-130">クライアントが  _lpEntryID_ で NULL を渡した場合、既定ではメッセージ ストアは選択されません。</span><span class="sxs-lookup"><span data-stu-id="de903-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de903-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="de903-131">Return value</span></span>

<span data-ttu-id="de903-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="de903-132">S_OK</span></span> 
  
> <span data-ttu-id="de903-133">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="de903-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de903-134">注釈</span><span class="sxs-lookup"><span data-stu-id="de903-134">Remarks</span></span>

<span data-ttu-id="de903-135">**IMAPISession::SetDefaultStore** メソッドは、次のいずれかのメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="de903-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="de903-136">セッションの既定のメッセージ ストア。</span><span class="sxs-lookup"><span data-stu-id="de903-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="de903-137">セッションのプライマリ メッセージ ストア。</span><span class="sxs-lookup"><span data-stu-id="de903-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="de903-138">セッションのセカンダリ メッセージ ストア。</span><span class="sxs-lookup"><span data-stu-id="de903-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="de903-139">メッセージ ストアを既定として確立するには、メッセージ ストアのポリシー [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)プロパティに次のフラグ **PR_STORE_SUPPORT_MASK** 設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de903-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="de903-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="de903-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="de903-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="de903-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="de903-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="de903-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="de903-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="de903-143">Notes to callers</span></span>

<span data-ttu-id="de903-144">セッションの既定のメッセージ ストアを確認するには、状態テーブルを取得し、STATUS_DEFAULT_STORE 列の STATUS_DEFAULT_STORE フラグ **の設定をPR_RESOURCE_FLAGS** します。</span><span class="sxs-lookup"><span data-stu-id="de903-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="de903-145">この設定を持つ行は、セッションの既定値として指定されているメッセージ ストアを表します。</span><span class="sxs-lookup"><span data-stu-id="de903-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="de903-146">[メッセージ ストア] MAPI_DEFAULT_STOREまたは MAPI_SIMPLE_STORE_PERMANENTフラグが設定されている場合、MAPI はプロファイル、メッセージ ストア テーブル、および状態テーブルを更新します。</span><span class="sxs-lookup"><span data-stu-id="de903-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="de903-147">メッセージ ストアの既定の設定に変更が加わるたびに、次の通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="de903-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="de903-148">**メッセージ ストアと状態テーブルの両方** の影響を受ける行ごとに、fnevTableModified イベント通知が発行されます。</span><span class="sxs-lookup"><span data-stu-id="de903-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="de903-149">内部通知が MAPI スプーラーに発行されます。</span><span class="sxs-lookup"><span data-stu-id="de903-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="de903-150">既に進行中の操作は変更なしで完了します。メッセージのダウンロードなど、既定のメッセージ ストアを含む新しい操作が、新しい既定のストアに対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="de903-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="de903-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="de903-151">MFCMAPI reference</span></span>

<span data-ttu-id="de903-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de903-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="de903-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="de903-153">**File**</span></span>|<span data-ttu-id="de903-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="de903-154">**Function**</span></span>|<span data-ttu-id="de903-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="de903-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de903-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="de903-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="de903-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="de903-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="de903-158">MFCMAPI は **IMAPISession::SetDefaultStore** メソッドを使用して、選択したストアを既定のストアとして設定します。</span><span class="sxs-lookup"><span data-stu-id="de903-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de903-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="de903-159">See also</span></span>



[<span data-ttu-id="de903-160">PidTagResourceFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de903-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="de903-161">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="de903-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="de903-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="de903-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="de903-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="de903-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="de903-164">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="de903-164">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

