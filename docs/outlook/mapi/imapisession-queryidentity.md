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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c8f05707d63f922c9ce22e6e520c6c57e686f884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800705"
---
# <a name="imapisessionqueryidentity"></a><span data-ttu-id="d9130-103">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="d9130-103">IMAPISession::QueryIdentity</span></span>

  
  
<span data-ttu-id="d9130-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9130-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9130-105">セッションのプライマリ id を提供するオブジェクトのエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-105">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="d9130-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9130-106">Parameters</span></span>

 <span data-ttu-id="d9130-107">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9130-107">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="d9130-108">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9130-108">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d9130-109">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9130-109">_lppEntryID_</span></span>
  
> <span data-ttu-id="d9130-110">[out]プライマリ id を提供するオブジェクトのエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9130-110">[out] A pointer to a pointer to the entry identifier of the object that provides the primary identity.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9130-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d9130-111">Return value</span></span>

<span data-ttu-id="d9130-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9130-112">S_OK</span></span> 
  
> <span data-ttu-id="d9130-113">プライマリ id が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="d9130-113">The primary identity was successfully returned.</span></span>
    
<span data-ttu-id="d9130-114">MAPI_W_NO_SERVICE</span><span class="sxs-lookup"><span data-stu-id="d9130-114">MAPI_W_NO_SERVICE</span></span> 
  
> <span data-ttu-id="d9130-115">呼び出しが成功したが、セッションのプライマリ id がありません。</span><span class="sxs-lookup"><span data-stu-id="d9130-115">The call succeeded, but there is no primary identity for the session.</span></span> <span data-ttu-id="d9130-116">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9130-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="d9130-117">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9130-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="d9130-118">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9130-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9130-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d9130-119">Remarks</span></span>

<span data-ttu-id="d9130-120">**IMAPISession::QueryIdentity**メソッドは、現在のセッションのプライマリ id を取得し、 _lppEntryID_パラメーターを使用して値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-120">The **IMAPISession::QueryIdentity** method retrieves the primary identity for the current session and returns the value through the  _lppEntryID_ parameter.</span></span> <span data-ttu-id="d9130-121">プライマリ id は、通常、メッセージング、ユーザー セッションのユーザーを表すオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d9130-121">The primary identity is an object, typically a messaging user, that represents the user of a session.</span></span>  <span data-ttu-id="d9130-122">_lppEntryID_は、 [IMailUser](imailuserimapiprop.md)オブジェクトは、 [PidTagEntryID](pidtagentryid-canonical-property.md)プロパティも格納されているプライマリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-122">_lppEntryID_ returns the primary identity for an [IMailUser](imailuserimapiprop.md) object, which is also stored as the [PidTagEntryID](pidtagentryid-canonical-property.md) property.</span></span> <span data-ttu-id="d9130-123">[IMAPISession::OpenEntry](imapisession-openentry.md)を使用して**IMailUser**オブジェクトを開くには、 _lppEntryID_で返される値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9130-123">You can use the value returned in  _lppEntryID_ to open an **IMailUser** object using [IMAPISession::OpenEntry](imapisession-openentry.md).</span></span>
  
<span data-ttu-id="d9130-124">複数のメッセージ サービスで多くのサービス プロバイダーは、セッションのプライマリ id を提供できます、ただし、MAPI は 1 つのサービス プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="d9130-124">Although many service providers in multiple message services can provide the primary identity for a session, MAPI designates a single service provider.</span></span> <span data-ttu-id="d9130-125">プライマリ id を提供するサービス プロバイダーは、次の項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="d9130-125">The service provider that supplies the primary identity sets the following items:</span></span>
  
- <span data-ttu-id="d9130-126">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティに STATUS_PRIMARY_IDENTITY フラグです。</span><span class="sxs-lookup"><span data-stu-id="d9130-126">The STATUS_PRIMARY_IDENTITY flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d9130-127">**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d9130-127">The **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d9130-128">**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d9130-128">The **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d9130-129">**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d9130-129">The **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="d9130-130">プライマリ id を提供するサービス プロバイダーに属する場合、メッセージ サービス、メッセージ サービスで、他のサービス ・ プロバイダーはまた PR_IDENTITY プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9130-130">If the service provider that supplies the primary identity belongs to a message service, the other service providers in the message service also set the PR_IDENTITY properties.</span></span> <span data-ttu-id="d9130-131">これらのプロパティは、セッションのステータス テーブルに発行されます。</span><span class="sxs-lookup"><span data-stu-id="d9130-131">These properties are published in the session's status table.</span></span> 
  
<span data-ttu-id="d9130-132">可能であれば、 **QueryIdentity**は、STATUS_PRIMARY_IDENTITY でタグ付けされた状態の行の**PR_IDENTITY_ENTRYID**プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-132">If possible, **QueryIdentity** returns the value for the **PR_IDENTITY_ENTRYID** property from the status row tagged with STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="d9130-133">**PR_IDENTITY_ENTRYID**プロパティがプライマリ id の行に表示されない場合は、 **QueryIdentity**はその行の他の情報で作成された一時エントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-133">If the **PR_IDENTITY_ENTRYID** property is missing from the primary identity row, **QueryIdentity** returns a one-off entry identifier built with other information from that row.</span></span> 
  
<span data-ttu-id="d9130-134">STATUS_PRIMARY_IDENTITY フラグがすべてのステータス テーブルに**PR_RESOURCE_FLAG**列に表示されない場合は、 **QueryIdentity**は、検出された最初のエントリ id を返します。</span><span class="sxs-lookup"><span data-stu-id="d9130-134">If the STATUS_PRIMARY_IDENTITY flag is missing from all of the **PR_RESOURCE_FLAG** columns in the status table, **QueryIdentity** returns the first entry identifier that it finds.</span></span> <span data-ttu-id="d9130-135">取得する適切なエントリの識別子がない場合、 **QueryIdentity**は MAPI_W_NO_SERVICE の警告は成功し、 _lppEntryID_を指すハード コーディングされたエントリの識別子。</span><span class="sxs-lookup"><span data-stu-id="d9130-135">When there is no appropriate entry identifier to return, **QueryIdentity** succeeds with the warning MAPI_W_NO_SERVICE and points  _lppEntryID_ to a hard-coded entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d9130-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d9130-136">Notes to callers</span></span>

<span data-ttu-id="d9130-137">メッセージ サービスのセッションのプライマリ id を指定するタスクを割り当てるには[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9130-137">You can call the [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) method to assign a message service the task of supplying the session's primary identity.</span></span> 
  
<span data-ttu-id="d9130-138">プライマリ id を取得する別の方法は、STATUS_PRIMARY_IDENTITY に**PR_RESOURCE_FLAGS**の列を持つ行のステータス テーブルを検索することによってです。</span><span class="sxs-lookup"><span data-stu-id="d9130-138">Another way to retrieve the primary identity is by searching the status table for the row with the **PR_RESOURCE_FLAGS** columns set to STATUS_PRIMARY_IDENTITY.</span></span> <span data-ttu-id="d9130-139">この id 情報を取得する別の方法の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9130-139">For more information about this alternate way of retrieving identity information, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  
<span data-ttu-id="d9130-140">**QueryIdentity**によって返されるプライマリ id のエントリ id を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出してメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="d9130-140">When you are finished using the entry identifier for the primary identity returned by **QueryIdentity**, free its memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="d9130-141">識別情報の詳細については一般に、 [MAPI のプライマリ Id](mapi-primary-identity.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9130-141">For more information about identity in general, see [MAPI Primary Identity](mapi-primary-identity.md).</span></span> 
  
<span data-ttu-id="d9130-142">MAPI セッションの id を取得の詳細については、[主に取得してプロバイダーの Id](retrieving-primary-and-provider-identity.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9130-142">For more information about retrieving MAPI session identity, see [Retrieving Primary and Provider Identity](retrieving-primary-and-provider-identity.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9130-143">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="d9130-143">MFCMAPI reference</span></span>

<span data-ttu-id="d9130-144">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="d9130-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9130-145">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="d9130-145">**File**</span></span>|<span data-ttu-id="d9130-146">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="d9130-146">**Function**</span></span>|<span data-ttu-id="d9130-147">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="d9130-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9130-148">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d9130-148">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="d9130-149">CMainDlg::OnQueryIdentity</span><span class="sxs-lookup"><span data-stu-id="d9130-149">CMainDlg::OnQueryIdentity</span></span>  <br/> |<span data-ttu-id="d9130-150">MFCMAPI では、 **IMAPISession::QueryIdentity**メソッドを使用して、セッションのプライマリ id のアドレス帳のエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9130-150">MFCMAPI uses the **IMAPISession::QueryIdentity** method to open the address book entry for the primary identity of the session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9130-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9130-151">See also</span></span>



[<span data-ttu-id="d9130-152">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="d9130-152">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
  
[<span data-ttu-id="d9130-153">IMsgServiceAdmin::SetPrimaryIdentity</span><span class="sxs-lookup"><span data-stu-id="d9130-153">IMsgServiceAdmin::SetPrimaryIdentity</span></span>](imsgserviceadmin-setprimaryidentity.md)
  
[<span data-ttu-id="d9130-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d9130-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d9130-155">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9130-155">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="d9130-156">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d9130-156">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="d9130-157">MAPI のプライマリ Id</span><span class="sxs-lookup"><span data-stu-id="d9130-157">MAPI Primary Identity</span></span>](mapi-primary-identity.md)
  
[<span data-ttu-id="d9130-158">プライマリとプロバイダー ID の取得</span><span class="sxs-lookup"><span data-stu-id="d9130-158">Retrieving Primary and Provider Identity</span></span>](retrieving-primary-and-provider-identity.md)
  
[<span data-ttu-id="d9130-159">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="d9130-159">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
  
[<span data-ttu-id="d9130-160">状態テーブルと状態オブジェクト</span><span class="sxs-lookup"><span data-stu-id="d9130-160">Status Table and Status Objects</span></span>](status-table-and-status-objects.md)

