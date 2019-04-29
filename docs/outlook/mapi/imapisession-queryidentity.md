---
title: imapisessionqueryidentity
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
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="76c8b-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="76c8b-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="76c8b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76c8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76c8b-105">セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="76c8b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76c8b-106">Parameters</span></span>

 <span data-ttu-id="76c8b-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="76c8b-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="76c8b-108">読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="76c8b-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="76c8b-109">_lppentryid_</span><span class="sxs-lookup"><span data-stu-id="76c8b-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="76c8b-110">読み上げプライマリ id を提供するオブジェクトのエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="76c8b-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76c8b-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="76c8b-111">Return value</span></span>

<span data-ttu-id="76c8b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="76c8b-112">S_OK</span></span> 
  
> <span data-ttu-id="76c8b-113">プライマリ id が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="76c8b-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="76c8b-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="76c8b-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="76c8b-115">呼び出しは成功しましたが、セッションのプライマリ id がありません。</span><span class="sxs-lookup"><span data-stu-id="76c8b-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="76c8b-116">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="76c8b-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="76c8b-117">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="76c8b-118">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c8b-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76c8b-119">注釈</span><span class="sxs-lookup"><span data-stu-id="76c8b-119">Remarks</span></span>

<span data-ttu-id="76c8b-120">**imapisession:: queryidentity**メソッドは、現在のセッションのプライマリ id を取得し、 _lppentryid_パラメーターを使用して値を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="76c8b-121">プライマリ id は、通常、セッションのユーザーを表す、オブジェクト (通常はメッセージングユーザー) です。</span><span class="sxs-lookup"><span data-stu-id="76c8b-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="76c8b-122">_lppentryid_は、 [PidTagEntryID](pidtagentryid-canonical-property.md)プロパティとしても格納されている[imailuser](imailuserimapiprop.md)オブジェクトのプライマリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="76c8b-123">_lppentryid_で返された値を使用して、 [imapisession:: openentry](imapisession-openentry.md)を使用して**imailuser**オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="76c8b-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="76c8b-124">複数のメッセージサービスのサービスプロバイダーの多くは、セッションのプライマリ id を提供していますが、MAPI は1つのサービスプロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="76c8b-125">プライマリ id を提供するサービスプロバイダーは、次の項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="76c8b-126">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティの STATUS_PRIMARY_IDENTITY フラグ。</span><span class="sxs-lookup"><span data-stu-id="76c8b-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="76c8b-127">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="76c8b-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="76c8b-128">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="76c8b-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="76c8b-129">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="76c8b-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="76c8b-130">プライマリ id を提供するサービスプロバイダーがメッセージサービスに属している場合、メッセージサービス内の他のサービスプロバイダーも PR_IDENTITY プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="76c8b-131">これらのプロパティは、セッションの状態テーブルで公開されます。</span><span class="sxs-lookup"><span data-stu-id="76c8b-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="76c8b-132">可能であれば、 **queryidentity**は、STATUS_PRIMARY_IDENTITY でタグ付けされた状態行から**PR_IDENTITY_ENTRYID**プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="76c8b-133">**PR_IDENTITY_ENTRYID**プロパティがプライマリ id 行にない場合、 **queryidentity**はその行から他の情報で構築された、1回限りのエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="76c8b-134">STATUS_PRIMARY_IDENTITY フラグが状態テーブル内のすべての**PR_RESOURCE_FLAG**列から欠落している場合、 **queryidentity**は、検出された最初のエントリ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="76c8b-135">返される適切なエントリ識別子が存在しない場合、 **queryidentity**は警告 MAPI_W_NO_SERVICE で成功し、 _lppentryid_はハードコードされたエントリ識別子になります。</span><span class="sxs-lookup"><span data-stu-id="76c8b-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="76c8b-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="76c8b-136">Notes to callers</span></span>

<span data-ttu-id="76c8b-137">[IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出して、メッセージサービスにセッションのプライマリ id を指定するタスクを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="76c8b-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="76c8b-138">プライマリ id を取得するもう1つの方法は、 **PR_RESOURCE_FLAGS**列が STATUS_PRIMARY_IDENTITY に設定されている行の状態テーブルを検索することです。</span><span class="sxs-lookup"><span data-stu-id="76c8b-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="76c8b-139">この代替方法によって id 情報を取得する方法の詳細については、「 [status Table and status Objects](status-table-and-status-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c8b-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="76c8b-140">**queryidentity**から返されるプライマリ id のエントリ識別子の使用を終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、そのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="76c8b-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="76c8b-141">一般的な id の詳細については、「 [MAPI プライマリ id](mapi-primary-identity.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c8b-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="76c8b-142">MAPI セッション id の取得の詳細については、「[プライマリおよびプロバイダー id を取得](retrieving-primary-and-provider-identity.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c8b-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="76c8b-143">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="76c8b-143">MFCMAPI reference</span></span>

<span data-ttu-id="76c8b-144">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76c8b-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="76c8b-145">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="76c8b-145">**File**</span></span>|<span data-ttu-id="76c8b-146">**関数**</span><span class="sxs-lookup"><span data-stu-id="76c8b-146">**Function**</span></span>|<span data-ttu-id="76c8b-147">**コメント**</span><span class="sxs-lookup"><span data-stu-id="76c8b-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="76c8b-148">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="76c8b-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="76c8b-149">CMainDlg:: onqueryidentity</span><span class="sxs-lookup"><span data-stu-id="76c8b-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="76c8b-150">mfcmapi は、 **imapisession:: queryidentity**メソッドを使用して、セッションのプライマリ id のアドレス帳エントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="76c8b-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76c8b-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="76c8b-151">See also</span></span>



[<span data-ttu-id="76c8b-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="76c8b-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="76c8b-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="76c8b-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="76c8b-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="76c8b-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="76c8b-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="76c8b-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="76c8b-156">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="76c8b-156">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="76c8b-157">MAPI プライマリ id</span><span class="sxs-lookup"><span data-stu-id="76c8b-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="76c8b-158">プライマリとプロバイダー id の取得</span><span class="sxs-lookup"><span data-stu-id="76c8b-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="76c8b-159">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="76c8b-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="76c8b-160">状態テーブルと状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="76c8b-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

