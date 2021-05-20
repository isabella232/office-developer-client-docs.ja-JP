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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431107"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="9a766-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="9a766-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="9a766-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a766-105">コンテナーのコンテンツ テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9a766-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9a766-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9a766-106">Parameters</span></span>

 <span data-ttu-id="9a766-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a766-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9a766-108">[in]コンテンツ テーブルの返し方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9a766-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="9a766-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9a766-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9a766-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="9a766-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="9a766-111">コンテナーの関連付けられたコンテンツ テーブルは、標準のコンテンツ テーブルの代わりに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="9a766-112">このフラグはフォルダーでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a766-112">This flag is used only with folders.</span></span> <span data-ttu-id="9a766-113">関連付けられたコンテンツ テーブルに含まれるメッセージは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドの呼び出しで設定MAPI_ASSOCIATEDフラグを設定して作成されました。</span><span class="sxs-lookup"><span data-stu-id="9a766-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="9a766-114">クライアントは通常、関連付けられたコンテンツ テーブルを使用して、フォーム、ビュー、その他の非表示メッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="9a766-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="9a766-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="9a766-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="9a766-116">frightsFreeBusySimple および frightsFreeBusyDetailed 権限へのアクセス **を** 有効PR_MEMBER_RIGHTS。</span><span class="sxs-lookup"><span data-stu-id="9a766-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="9a766-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9a766-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9a766-118">**GetContentsTable は** 、呼び出し元がテーブルを使用できる前に、正常に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9a766-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="9a766-119">テーブルが使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="9a766-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a766-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9a766-121">文字列データを含む列を Unicode 形式で返す要求。</span><span class="sxs-lookup"><span data-stu-id="9a766-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="9a766-122">このフラグMAPI_UNICODE設定しない場合は、ANSI 形式で文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="9a766-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="9a766-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="9a766-124">現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="9a766-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="9a766-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9a766-125">_lppTable_</span></span>
  
> <span data-ttu-id="9a766-126">[out]目次テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="9a766-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9a766-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="9a766-127">Return value</span></span>

<span data-ttu-id="9a766-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a766-128">S_OK</span></span> 
  
> <span data-ttu-id="9a766-129">コンテンツ テーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="9a766-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="9a766-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9a766-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9a766-131">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9a766-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9a766-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9a766-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9a766-133">コンテナーにはコンテンツが含め、コンテンツ テーブルを提供できません。</span><span class="sxs-lookup"><span data-stu-id="9a766-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a766-134">注釈</span><span class="sxs-lookup"><span data-stu-id="9a766-134">Remarks</span></span>

<span data-ttu-id="9a766-135">**IMAPIContainer::GetContentsTable** メソッドは、コンテナーのコンテンツ テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9a766-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="9a766-136">コンテンツ テーブルには、コンテナー内のオブジェクトに関する概要情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a766-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="9a766-137">コンテンツ テーブルには長い列セットがあります。</span><span class="sxs-lookup"><span data-stu-id="9a766-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="9a766-138">コンテンツ テーブルの必須列とオプション列の完全な一覧については、「コンテンツ テーブル」 [を参照してください](contents-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="9a766-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="9a766-139">一部のコンテナーにコンテンツがない場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="9a766-140">これらのコンテナーは、MAPI_E_NO_SUPPORT実装の **GetContentsTable からデータを返します**。</span><span class="sxs-lookup"><span data-stu-id="9a766-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9a766-141">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="9a766-141">Notes to implementers</span></span>

<span data-ttu-id="9a766-142">コンテナーのコンテンツ テーブルをサポートする場合は、次の操作も行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="9a766-143">コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドへの呼び出しをサポートして、PR_CONTAINER_CONTENTS **(** [PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a766-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="9a766-144">コンテナー **PR_CONTAINER_CONTENTS** 呼び出しに応答して、コンテナーの呼び出しを返します。</span><span class="sxs-lookup"><span data-stu-id="9a766-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="9a766-145">[IMAPIProp::GetProps](imapiprop-getprops.md) メソッドと [IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッド。</span><span class="sxs-lookup"><span data-stu-id="9a766-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="9a766-146">このメソッドのリモート トランスポート プロバイダーの実装では **、GetContentsTable** メソッドに渡される _ppTable_ パラメーターの [IMAPITable : IUnknown](imapitableiunknown.md)インターフェイスへのポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="9a766-147">トランスポート プロバイダーに既存のコンテンツ テーブルがある場合は、そのテーブルへのポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="9a766-148">指定しない場合、このメソッドは新しい [IMAPITable : IUnknown](imapitableiunknown.md) オブジェクトを作成し、メッセージ ヘッダーをテーブルに設定し (使用可能な場合)、新しいテーブルへのポインターを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="9a766-149">[ITableData::HrGetView](itabledata-hrgetview.md)メソッドは、戻り値を生成し、ppTable パラメーターにテーブル ポインターを格納 _する場合に便利_ です。</span><span class="sxs-lookup"><span data-stu-id="9a766-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="9a766-150">コンテンツ テーブルは、少なくとも次のプロパティ列をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a766-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="9a766-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="9a766-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a766-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="9a766-169">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9a766-169">Notes to callers</span></span>

<span data-ttu-id="9a766-170">文字列およびバイナリコンテンツテーブルの列は切り捨て可能です。</span><span class="sxs-lookup"><span data-stu-id="9a766-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="9a766-171">通常、プロバイダーは 255 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="9a766-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="9a766-172">テーブルに切り捨てられた列が含まれるかどうかは事前に分からないので、列の長さが 255 バイトまたは 510 バイトの場合は、列が切り捨てられると仮定します。</span><span class="sxs-lookup"><span data-stu-id="9a766-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="9a766-173">必要に応じて、切り捨てられた列の完全な値をオブジェクトから直接取得するには、そのエントリ識別子を使用して開き **、IMAPIProp::GetProps** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9a766-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="9a766-174">プロバイダーの実装に応じて、制限と並べ替え操作は、すべての文字列またはその文字列の切り捨てられたバージョンに適用できます。</span><span class="sxs-lookup"><span data-stu-id="9a766-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9a766-175">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9a766-175">MFCMAPI reference</span></span>

<span data-ttu-id="9a766-176">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a766-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9a766-177">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9a766-177">**File**</span></span>|<span data-ttu-id="9a766-178">**関数**</span><span class="sxs-lookup"><span data-stu-id="9a766-178">**Function**</span></span>|<span data-ttu-id="9a766-179">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9a766-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9a766-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="9a766-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="9a766-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="9a766-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="9a766-182">**CContentsTableDlg** クラスは **、GetContentsTable** を使用してコンテンツ テーブル内のエントリを取得します。</span><span class="sxs-lookup"><span data-stu-id="9a766-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a766-183">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a766-183">See also</span></span>



[<span data-ttu-id="9a766-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="9a766-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="9a766-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9a766-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9a766-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="9a766-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="9a766-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a766-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="9a766-188">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a766-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="9a766-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9a766-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="9a766-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9a766-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

