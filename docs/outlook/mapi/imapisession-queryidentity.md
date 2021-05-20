---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 396320c6b39553da09aa1f45d0c755f40a939382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428222"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="2ce65-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="2ce65-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="2ce65-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ce65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ce65-105">セッションのプライマリ ID を提供するオブジェクトのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="2ce65-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ce65-106">Parameters</span></span>

 <span data-ttu-id="2ce65-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ce65-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="2ce65-108">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ce65-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2ce65-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ce65-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="2ce65-110">[out]プライマリ ID を提供するオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ce65-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ce65-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ce65-111">Return value</span></span>

<span data-ttu-id="2ce65-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ce65-112">S_OK</span></span> 
  
> <span data-ttu-id="2ce65-113">プライマリ ID が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="2ce65-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="2ce65-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="2ce65-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="2ce65-115">呼び出しは成功しましたが、セッションのプライマリ ID はありません。</span><span class="sxs-lookup"><span data-stu-id="2ce65-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="2ce65-116">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="2ce65-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2ce65-117">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2ce65-118">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="2ce65-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ce65-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2ce65-119">Remarks</span></span>

<span data-ttu-id="2ce65-120">**IMAPISession::QueryIdentity** メソッドは、現在のセッションのプライマリ ID を取得し _、lppEntryID_ パラメーターを使用して値を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="2ce65-121">プライマリ ID は、セッションのユーザーを表すオブジェクト (通常はメッセージング ユーザー) です。</span><span class="sxs-lookup"><span data-stu-id="2ce65-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="2ce65-122">_lppEntryID_ は [、PidTagEntryID](pidtagentryid-canonical-property.md)プロパティとして格納される [IMailUser](imailuserimapiprop.md)オブジェクトのプライマリ ID を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="2ce65-123">_lppEntryID_ で返される値を使用して [、IMAPISession::OpenEntry](imapisession-openentry.md)を使用して **IMailUser** オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ce65-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="2ce65-124">複数のメッセージ サービス内の多くのサービス プロバイダーは、セッションのプライマリ ID を提供することができますが、MAPI は 1 つのサービス プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="2ce65-125">プライマリ ID を提供するサービス プロバイダーは、次の項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="2ce65-126">プロパティSTATUS_PRIMARY_IDENTITY **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティPR_RESOURCE_FLAGSフラグを指定します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2ce65-127">プロパティ **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="2ce65-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2ce65-128">プロパティ **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="2ce65-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2ce65-129">プロパティ **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) プロパティです。</span><span class="sxs-lookup"><span data-stu-id="2ce65-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="2ce65-130">プライマリ ID を提供するサービス プロバイダーがメッセージ サービスに属している場合は、メッセージ サービス内の他のサービス プロバイダーも PR_IDENTITYプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="2ce65-131">これらのプロパティは、セッションの状態テーブルに公開されます。</span><span class="sxs-lookup"><span data-stu-id="2ce65-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="2ce65-132">可能な場合 **、QueryIdentity** は、PR_IDENTITY_ENTRYIDプロパティにタグ付けされた状態行の値をSTATUS_PRIMARY_IDENTITY。</span><span class="sxs-lookup"><span data-stu-id="2ce65-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="2ce65-133">プライマリ ID **行PR_IDENTITY_ENTRYID** プロパティが見つからない場合 **、QueryIdentity** は、その行の他の情報を含む 1 回のエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="2ce65-134">状態テーブルSTATUS_PRIMARY_IDENTITYのすべての PR_RESOURCE_FLAG 列に対して、STATUS_PRIMARY_IDENTITYフラグが見つからない場合 **、QueryIdentity** は最初に見つけたエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="2ce65-135">返す適切なエントリ識別子がない場合 **、QueryIdentity** は警告 MAPI_W_NO_SERVICE で成功し  _、lppEntryID_ をハードコードされたエントリ識別子にポイントします。</span><span class="sxs-lookup"><span data-stu-id="2ce65-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ce65-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2ce65-136">Notes to callers</span></span>

<span data-ttu-id="2ce65-137">[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出して、セッションのプライマリ ID を指定するタスクをメッセージ サービスに割り当てできます。</span><span class="sxs-lookup"><span data-stu-id="2ce65-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="2ce65-138">プライマリ ID を取得するもう 1 つの方法は、行の状態テーブルを検索し、列のPR_RESOURCE_FLAGSに設定STATUS_PRIMARY_IDENTITY。</span><span class="sxs-lookup"><span data-stu-id="2ce65-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="2ce65-139">ID 情報を取得するこの代替方法の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="2ce65-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="2ce65-140">**QueryIdentity** によって返されるプライマリ ID のエントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="2ce65-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="2ce65-141">一般的な ID の詳細については [、「MAPI プライマリ ID」を参照してください](mapi-primary-identity.md)。</span><span class="sxs-lookup"><span data-stu-id="2ce65-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="2ce65-142">MAPI セッション ID の取得の詳細については、「プライマリ ID とプロバイダー ID の取得 [」を参照してください](retrieving-primary-and-provider-identity.md)。</span><span class="sxs-lookup"><span data-stu-id="2ce65-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ce65-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="2ce65-143">MFCMAPI reference</span></span>

<span data-ttu-id="2ce65-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ce65-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ce65-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="2ce65-145">**File**</span></span>|<span data-ttu-id="2ce65-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="2ce65-146">**Function**</span></span>|<span data-ttu-id="2ce65-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="2ce65-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ce65-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2ce65-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="2ce65-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="2ce65-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="2ce65-150">MFCMAPI は **IMAPISession::QueryIdentity** メソッドを使用して、セッションのプライマリ ID のアドレス帳エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="2ce65-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ce65-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ce65-151">See also</span></span>



[<span data-ttu-id="2ce65-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2ce65-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="2ce65-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="2ce65-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="2ce65-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2ce65-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2ce65-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ce65-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="2ce65-156">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2ce65-156">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="2ce65-157">MAPI プライマリ ID</span><span class="sxs-lookup"><span data-stu-id="2ce65-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="2ce65-158">プライマリ ID とプロバイダー ID の取得</span><span class="sxs-lookup"><span data-stu-id="2ce65-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="2ce65-159">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="2ce65-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="2ce65-160">Status Table オブジェクトと Status オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2ce65-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

