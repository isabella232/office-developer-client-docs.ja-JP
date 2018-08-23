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
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800459"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="2ce87-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="2ce87-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="2ce87-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ce87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ce87-105">コンテナーの内容のテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="2ce87-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="2ce87-106">Parameters</span></span>

 <span data-ttu-id="2ce87-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ce87-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2ce87-108">[in]コンテンツ テーブルを返す方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2ce87-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="2ce87-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2ce87-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="2ce87-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="2ce87-111">コンテナーの内容が関連付けられているテーブルは、標準的な内容のテーブルの代わりに返されます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="2ce87-112">このフラグは、フォルダーでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-112">This flag is used only with folders.</span></span> <span data-ttu-id="2ce87-113">コンテンツが関連付けられているテーブルに含まれるメッセージは、MAPI_ASSOCIATED フラグが設定されている[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)メソッドの呼び出しで作成されました。</span><span class="sxs-lookup"><span data-stu-id="2ce87-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="2ce87-114">クライアントは、フォーム、ビュー、およびその他の非表示のメッセージを取得するために通常関連付けられている内容のテーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="2ce87-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="2ce87-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="2ce87-116">**PR_MEMBER_RIGHTS**で frightsFreeBusySimple と frightsFreeBusyDetailed の権限にアクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="2ce87-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="2ce87-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2ce87-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2ce87-118">**GetContentsTable**が正常に完了可能性があります前にテーブルが使用可能な呼び出し元にします。</span><span class="sxs-lookup"><span data-stu-id="2ce87-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="2ce87-119">テーブルが使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="2ce87-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ce87-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ce87-121">Unicode 形式で文字列データを含む列が返されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="2ce87-122">MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="2ce87-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="2ce87-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="2ce87-124">ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。</span><span class="sxs-lookup"><span data-stu-id="2ce87-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="2ce87-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="2ce87-125">_lppTable_</span></span>
  
> <span data-ttu-id="2ce87-126">[out]コンテンツ テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ce87-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ce87-127">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2ce87-127">Return value</span></span>

<span data-ttu-id="2ce87-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ce87-128">S_OK</span></span> 
  
> <span data-ttu-id="2ce87-129">内容のテーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="2ce87-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="2ce87-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2ce87-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2ce87-131">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2ce87-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="2ce87-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2ce87-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2ce87-133">コンテナーでは、内容がないので、内容のテーブルを提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="2ce87-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ce87-134">注釈</span><span class="sxs-lookup"><span data-stu-id="2ce87-134">Remarks</span></span>

<span data-ttu-id="2ce87-135">**IMAPIContainer::GetContentsTable**メソッドは、コンテナーの内容のテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="2ce87-136">コンテンツ テーブルには、コンテナー内のオブジェクトについての概要情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ce87-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="2ce87-137">テーブルの内容は、長い列のセットを持っています。</span><span class="sxs-lookup"><span data-stu-id="2ce87-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="2ce87-138">必須および省略可能なテーブルの列の内容の一覧は、[テーブルの内容](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ce87-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="2ce87-139">内容がないといくつかのコンテナーのことができます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="2ce87-140">これらのコンテナーでは、 **GetContentsTable**の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2ce87-141">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="2ce87-141">Notes to implementers</span></span>

<span data-ttu-id="2ce87-142">コンテナーのコンテンツ テーブルをサポートする場合も、次の行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ce87-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="2ce87-143">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)のメソッドの呼び出しをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2ce87-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="2ce87-144">コンテナーの呼び出しへの応答として**PR_CONTAINER_CONTENTS**を返す</span><span class="sxs-lookup"><span data-stu-id="2ce87-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="2ce87-145">[IMAPIProp::GetProps](imapiprop-getprops.md)および[IMAPIProp::GetPropList](imapiprop-getproplist.md)の方法です。</span><span class="sxs-lookup"><span data-stu-id="2ce87-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="2ce87-146">このメソッドをリモート トランスポート プロバイダーの実装へのポインターを返す必要があります、 [IMAPITable: IUnknown](imapitableiunknown.md) 、 **GetContentsTable**メソッドに渡される_ppTable_パラメーター内のインタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="2ce87-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="2ce87-147">場合は、トランスポート プロバイダーは、既存のコンテンツ テーブルへのポインターを返すには十分です。</span><span class="sxs-lookup"><span data-stu-id="2ce87-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="2ce87-148">場合は、このメソッドが新規に作成する必要があります[IMAPITable: IUnknown](imapitableiunknown.md)オブジェクト、テーブルには、メッセージ ヘッダー (使用可能な場合)、および新しいテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="2ce87-149">[ITableData::HrGetView](itabledata-hrgetview.md)メソッドは、戻り値を生成して、 _ppTable_パラメーターでテーブルのポインターを格納するに便利です。</span><span class="sxs-lookup"><span data-stu-id="2ce87-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="2ce87-150">内容のテーブルは、少なくとも次のプロパティの列をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ce87-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="2ce87-151">**PR_ENTRYID**([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-152">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-153">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-154">**PR_DISPLAY_TO**([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-155">**あるの PR_SUBJECT**([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-156">**PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-157">**PR_MESSAGE_FLAGS**([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-158">**PR_MESSAGE_SIZE**([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-159">**PR_PRIORITY**([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-160">**PR_IMPORTANCE**([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-161">**PR_SENSITIVITY**([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-162">**PR_MESSAGE_DELIVERY_TIME**([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-163">**PR_MSG_STATUS**([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-164">**PR_MESSAGE_DOWNLOAD_TIME**([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-165">**PR_HASATTACH**([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-166">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-167">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="2ce87-168">**PR_NORMALIZED_SUBJECT**([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2ce87-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="2ce87-169">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2ce87-169">Notes to callers</span></span>

<span data-ttu-id="2ce87-170">文字列とバイナリの内容のテーブルの列を切り捨てることができます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="2ce87-171">通常、プロバイダーは、255 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="2ce87-172">テーブルには、切り捨てられた列が含まれて かどうか、あらかじめ知ることはできません、ため、列の長さが 255 であるか、510 バイトである場合、列が切り捨てられることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="2ce87-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="2ce87-173">常にから取得できます、切り捨てられた列の最大の価値に応じて、直接オブジェクトを開くには、そのエントリの識別子を使用して、 **IMAPIProp::GetProps**メソッドを呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="2ce87-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="2ce87-174">プロバイダーの実装の制限や並べ替え操作によっては、文字列のすべてまたはその文字列の切り捨てられたバージョンを適用できます。</span><span class="sxs-lookup"><span data-stu-id="2ce87-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ce87-175">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="2ce87-175">MFCMAPI reference</span></span>

<span data-ttu-id="2ce87-176">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="2ce87-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ce87-177">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="2ce87-177">**File**</span></span>|<span data-ttu-id="2ce87-178">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="2ce87-178">**Function**</span></span>|<span data-ttu-id="2ce87-179">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="2ce87-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ce87-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="2ce87-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="2ce87-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="2ce87-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="2ce87-182">**CContentsTableDlg**クラスでは、 **GetContentsTable**を使用して、コンテンツ テーブル内のエントリを取得します。</span><span class="sxs-lookup"><span data-stu-id="2ce87-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ce87-183">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ce87-183">See also</span></span>



[<span data-ttu-id="2ce87-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="2ce87-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="2ce87-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2ce87-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="2ce87-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="2ce87-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="2ce87-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ce87-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="2ce87-188">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ce87-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="2ce87-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2ce87-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="2ce87-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="2ce87-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

