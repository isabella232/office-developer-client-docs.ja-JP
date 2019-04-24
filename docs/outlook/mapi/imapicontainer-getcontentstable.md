---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349288"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="9c900-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="9c900-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="9c900-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c900-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c900-105">コンテナーの contents テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9c900-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9c900-106">Parameters</span></span>

 <span data-ttu-id="9c900-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c900-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9c900-108">順番コンテンツテーブルがどのように返されるかを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9c900-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="9c900-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c900-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9c900-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="9c900-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="9c900-111">コンテナーの関連する contents テーブルは、標準の contents テーブルの代わりに返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="9c900-112">このフラグは、フォルダーでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c900-112">This flag is used only with folders.</span></span> <span data-ttu-id="9c900-113">MAPI_ASSOCIATED フラグが[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドの呼び出しで設定された状態で、関連付けられたコンテンツテーブルに含まれているメッセージが作成されました。</span><span class="sxs-lookup"><span data-stu-id="9c900-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="9c900-114">通常、クライアントは関連付けられた contents テーブルを使用して、フォーム、ビュー、およびその他の非表示のメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="9c900-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="9c900-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="9c900-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="9c900-116">**PR_MEMBER_RIGHTS**の frightsFreeBusySimple および frightsFreeBusyDetailed 権限へのアクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="9c900-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="9c900-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9c900-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9c900-118">**getcontentstable**は、呼び出し元がテーブルを使用できるようになる前に、正常に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c900-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="9c900-119">テーブルが使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="9c900-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c900-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9c900-121">文字列データを含む列が Unicode 形式で返されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="9c900-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="9c900-122">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式で返されます。</span><span class="sxs-lookup"><span data-stu-id="9c900-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="9c900-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="9c900-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="9c900-124">現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="9c900-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="9c900-125">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="9c900-125">_lppTable_</span></span>
  
> <span data-ttu-id="9c900-126">読み上げcontents テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9c900-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c900-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="9c900-127">Return value</span></span>

<span data-ttu-id="9c900-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c900-128">S_OK</span></span> 
  
> <span data-ttu-id="9c900-129">コンテンツテーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="9c900-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="9c900-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9c900-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9c900-131">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9c900-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9c900-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9c900-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9c900-133">コンテナーには内容が含まれていないため、目次表を提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="9c900-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c900-134">解説</span><span class="sxs-lookup"><span data-stu-id="9c900-134">Remarks</span></span>

<span data-ttu-id="9c900-135">**IMAPIContainer:: getcontentstable**メソッドは、コンテナーの contents テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="9c900-136">contents テーブルには、コンテナー内のオブジェクトに関する概要情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c900-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="9c900-137">目次テーブルに長い列セットがあります。</span><span class="sxs-lookup"><span data-stu-id="9c900-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="9c900-138">目次表の必須およびオプションの列の完全な一覧については、「 [contents tables](contents-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c900-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="9c900-139">一部のコンテナーには内容が含まれていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="9c900-140">これらのコンテナーは、 **getcontentstable**の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9c900-141">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="9c900-141">Notes to implementers</span></span>

<span data-ttu-id="9c900-142">コンテナーの contents テーブルをサポートしている場合は、次の操作も実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="9c900-143">コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドへの呼び出しをサポートして、 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="9c900-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="9c900-144">コンテナーの呼び出しに対する応答として**PR_CONTAINER_CONTENTS**を返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="9c900-145">[imapiprop:: GetProps](imapiprop-getprops.md)および[imapiprop:: getproplist](imapiprop-getproplist.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="9c900-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="9c900-146">リモートトランスポートプロバイダーのこのメソッドの実装では、 **getcontentstable**メソッドに渡された_pptable_パラメーターの[IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスへのポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="9c900-147">トランスポートプロバイダーに既存のコンテンツテーブルがある場合は、そのテーブルへのポインターを返すだけで十分です。</span><span class="sxs-lookup"><span data-stu-id="9c900-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="9c900-148">含まれていない場合、このメソッドは新しい[IMAPITable: IUnknown](imapitableiunknown.md)オブジェクトを作成し、メッセージヘッダーを (使用可能な場合は) テーブルに設定して、新しいテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="9c900-149">[itabledata:: hrgetview](itabledata-hrgetview.md)メソッドは、戻り値を生成し、テーブルポインターを_pptable_パラメーターに格納するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="9c900-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="9c900-150">contents テーブルは、少なくとも次のプロパティ列をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c900-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="9c900-151">**PR_ENTRYID**([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-152">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-153">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-154">**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-155">**PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-156">**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-157">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-158">**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-159">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-160">**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-161">**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-162">**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-163">**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-164">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-165">**PR_HASATTACH**([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-166">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-167">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="9c900-168">**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9c900-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="9c900-169">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9c900-169">Notes to callers</span></span>

<span data-ttu-id="9c900-170">文字列およびバイナリコンテンツの表の列を切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="9c900-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="9c900-171">通常、プロバイダーは255文字を返します。</span><span class="sxs-lookup"><span data-stu-id="9c900-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="9c900-172">テーブルに切り捨てられた列が含まれているかどうかを事前に知ることはできないため、列の長さが255または510バイトの場合は、列が切り捨てられていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="9c900-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="9c900-173">必要に応じて、エントリ id を使用して、切り捨てられた列の完全な値をオブジェクトから直接取得して、 **imapiprop:: GetProps**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c900-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="9c900-174">プロバイダーの実装に応じて、制限および並べ替え操作は、すべての文字列またはその文字列の切り捨てられたバージョンに適用できます。</span><span class="sxs-lookup"><span data-stu-id="9c900-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c900-175">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9c900-175">MFCMAPI reference</span></span>

<span data-ttu-id="9c900-176">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c900-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c900-177">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9c900-177">**File**</span></span>|<span data-ttu-id="9c900-178">**関数**</span><span class="sxs-lookup"><span data-stu-id="9c900-178">**Function**</span></span>|<span data-ttu-id="9c900-179">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9c900-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c900-180">ContentsTableDialog</span><span class="sxs-lookup"><span data-stu-id="9c900-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="9c900-181">CContentsTableDlg:: CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="9c900-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="9c900-182">**CContentsTableDlg**クラスは、 **getcontentstable**を使用して、contents テーブル内のエントリを取得します。</span><span class="sxs-lookup"><span data-stu-id="9c900-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c900-183">関連項目</span><span class="sxs-lookup"><span data-stu-id="9c900-183">See also</span></span>



[<span data-ttu-id="9c900-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="9c900-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="9c900-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9c900-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9c900-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9c900-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="9c900-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c900-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="9c900-188">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9c900-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="9c900-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9c900-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="9c900-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9c900-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

