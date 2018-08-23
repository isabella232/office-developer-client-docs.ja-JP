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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587846"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="581c0-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="581c0-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="581c0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="581c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="581c0-105">セッションの既定のメッセージ ストアとしてのメッセージ ・ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="581c0-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="581c0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="581c0-106">Parameters</span></span>

 <span data-ttu-id="581c0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="581c0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="581c0-108">[in]既定のメッセージ ストアの設定を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="581c0-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="581c0-109">これらのフラグは相互に排他的です。次のフラグの 1 つだけを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="581c0-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="581c0-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="581c0-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="581c0-111">セッションのデフォルト値としては、メッセージ ・ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="581c0-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="581c0-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) の列に STATUS_DEFAULT_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="581c0-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="581c0-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="581c0-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="581c0-114">ログオン時に使用するストアとしては、メッセージ ・ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="581c0-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="581c0-115">メッセージ ストアは既定のストアではない場合、クライアントにたどれるように既定値です。</span><span class="sxs-lookup"><span data-stu-id="581c0-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="581c0-116">**PR_RESOURCE_FLAGS**列に STATUS_PRIMARY_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="581c0-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="581c0-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="581c0-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="581c0-118">プライマリ メッセージ ストアを使用できない場合に、ログオンに使用するストアとしては、メッセージ ・ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="581c0-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="581c0-119">クライアントは、プライマリ ストアを開くことができません、する場合はセカンダリ ・ ストアを開く必要があります、既定値として設定します。</span><span class="sxs-lookup"><span data-stu-id="581c0-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="581c0-120">**PR_RESOURCE_FLAGS**列に STATUS_SECONDARY_STORE フラグを設定することによって、メッセージ ストアの状態のテーブルの行を更新します。</span><span class="sxs-lookup"><span data-stu-id="581c0-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="581c0-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="581c0-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="581c0-122">その状態テーブルの行をメッセージ ストアのテーブルの行、およびセッション ・ プロファイル内のメッセージ ストアの**PR_RESOURCE_FLAGS**プロパティでは、STATUS_SIMPLE_STORE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="581c0-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="581c0-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="581c0-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="581c0-124">状態テーブルの行に、メッセージ ストアのテーブルの行に、メッセージ ストアの**PR_RESOURCE_FLAGS**プロパティに STATUS_SIMPLE_STORE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="581c0-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="581c0-125">プロファイルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="581c0-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="581c0-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="581c0-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="581c0-127">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="581c0-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="581c0-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="581c0-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="581c0-129">[in]既定では、メッセージ ・ ストアのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="581c0-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="581c0-130">場合は_lpEntryID_に NULL を渡すと、クライアント、メッセージ ・ ストアが選択されていない既定値としてします。</span><span class="sxs-lookup"><span data-stu-id="581c0-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="581c0-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="581c0-131">Return value</span></span>

<span data-ttu-id="581c0-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="581c0-132">S_OK</span></span> 
  
> <span data-ttu-id="581c0-133">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="581c0-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="581c0-134">注釈</span><span class="sxs-lookup"><span data-stu-id="581c0-134">Remarks</span></span>

<span data-ttu-id="581c0-135">**IMAPISession::SetDefaultStore**メソッドは、次のいずれかとしてメッセージ ストアを確立します。</span><span class="sxs-lookup"><span data-stu-id="581c0-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="581c0-136">セッションの既定のメッセージ ストアです。</span><span class="sxs-lookup"><span data-stu-id="581c0-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="581c0-137">セッションの主なメッセージ ・ ストアです。</span><span class="sxs-lookup"><span data-stu-id="581c0-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="581c0-138">セッションの第 2 のメッセージ ・ ストアです。</span><span class="sxs-lookup"><span data-stu-id="581c0-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="581c0-139">メッセージ ストアを確立すると、既定値として、メッセージ ・ ストアは、次のフラグで、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="581c0-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="581c0-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="581c0-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="581c0-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="581c0-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="581c0-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="581c0-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="581c0-143">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="581c0-143">Notes to callers</span></span>

<span data-ttu-id="581c0-144">状態テーブルを取得して、 **PR_RESOURCE_FLAGS**の列に STATUS_DEFAULT_STORE フラグの設定を検索して、セッションの既定のメッセージ ストアを指定できます。</span><span class="sxs-lookup"><span data-stu-id="581c0-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="581c0-145">この設定を持つ行は、セッションのデフォルト値として指定されているメッセージ ・ ストアを表します。</span><span class="sxs-lookup"><span data-stu-id="581c0-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="581c0-146">MAPI_DEFAULT_STORE または MAPI_SIMPLE_STORE_PERMANENT フラグを設定すると、MAPI は、プロファイル、メッセージ ストアのテーブル、およびテーブルのステータスを更新します。</span><span class="sxs-lookup"><span data-stu-id="581c0-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="581c0-147">メッセージ ストアの既定の設定を変更、ときに、次の通知が生成されます。</span><span class="sxs-lookup"><span data-stu-id="581c0-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="581c0-148">**FnevTableModified**イベント通知は、メッセージ ストアとステータスの表には影響を受ける行ごとに発行されます。</span><span class="sxs-lookup"><span data-stu-id="581c0-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="581c0-149">内部の通知は、MAPI スプーラーに発行されます。</span><span class="sxs-lookup"><span data-stu-id="581c0-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="581c0-150">既に進行中の操作が完了した変更です。新しい既定のストアの既定のメッセージ ストアのメッセージをダウンロードするなど、新しい操作が処理されます。</span><span class="sxs-lookup"><span data-stu-id="581c0-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="581c0-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="581c0-151">MFCMAPI reference</span></span>

<span data-ttu-id="581c0-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="581c0-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="581c0-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="581c0-153">**File**</span></span>|<span data-ttu-id="581c0-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="581c0-154">**Function**</span></span>|<span data-ttu-id="581c0-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="581c0-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="581c0-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="581c0-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="581c0-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="581c0-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="581c0-158">MFCMAPI では、 **IMAPISession::SetDefaultStore**メソッドを使用して、既定のストアとして選択されているストアを設定します。</span><span class="sxs-lookup"><span data-stu-id="581c0-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="581c0-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="581c0-159">See also</span></span>



[<span data-ttu-id="581c0-160">PidTagResourceFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="581c0-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="581c0-161">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="581c0-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="581c0-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="581c0-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="581c0-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="581c0-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="581c0-164">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="581c0-164">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

