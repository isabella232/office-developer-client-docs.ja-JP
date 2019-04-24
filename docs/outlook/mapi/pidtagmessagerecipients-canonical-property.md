---
title: PidTagMessageRecipients 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355686"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="ca963-103">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca963-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="ca963-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca963-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca963-105">制限を満たす受信者サブオブジェクトを含むすべてのメッセージを検索するために、コンテンツテーブルに適用できる制限の表が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca963-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca963-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ca963-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca963-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="ca963-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="ca963-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ca963-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ca963-109">0x0e12</span><span class="sxs-lookup"><span data-stu-id="ca963-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="ca963-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ca963-110">Data type:</span></span>  <br/> |<span data-ttu-id="ca963-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ca963-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ca963-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ca963-112">Area:</span></span>  <br/> |<span data-ttu-id="ca963-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="ca963-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca963-114">解説</span><span class="sxs-lookup"><span data-stu-id="ca963-114">Remarks</span></span>

<span data-ttu-id="ca963-115">このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="ca963-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="ca963-116">**PT_OBJECT**型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca963-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="ca963-117">このコンテンツは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされ、 **IID_IMAPITable**インターフェイスの識別子が要求されます。</span><span class="sxs-lookup"><span data-stu-id="ca963-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="ca963-118">サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ca963-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="ca963-119">表の内容を取得するには、クライアントアプリケーションは[IMessage:: get table](imessage-getrecipienttable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca963-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="ca963-120">このプロパティは、 [ssubrestriction](ssubrestriction.md)構造で指定することによって、サブプロパティの制限に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca963-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="ca963-121">これにより、クライアントは、指定した条件に一致する受信者のメッセージへのコンテナーの表示を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="ca963-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="ca963-122">受信者のテーブルに少なくとも1つの行がある場合、つまり1人の受信者の制限を満たすメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca963-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="ca963-123">**メモ**サブクリップの制限結果は、テーブル内のすべてのメッセージに対する[imapisession:: openentry](imapisession-openentry.md)呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="ca963-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="ca963-124">クライアントアプリケーションと検索するメッセージ数に応じて、パフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ca963-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="ca963-125">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティとこのプロパティの使用方法は似ています。</span><span class="sxs-lookup"><span data-stu-id="ca963-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="ca963-126">複数の MAPI プロパティを使用して、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ca963-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="ca963-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="ca963-127">**Property**</span></span>|<span data-ttu-id="ca963-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="ca963-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca963-129">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca963-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ca963-130">Contents テーブル</span><span class="sxs-lookup"><span data-stu-id="ca963-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="ca963-131">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca963-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ca963-132">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="ca963-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="ca963-133">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca963-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ca963-134">関連付けられたコンテンツテーブル</span><span class="sxs-lookup"><span data-stu-id="ca963-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="ca963-135">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ca963-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ca963-136">Attachment テーブル</span><span class="sxs-lookup"><span data-stu-id="ca963-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="ca963-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="ca963-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="ca963-138">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="ca963-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ca963-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ca963-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca963-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ca963-140">Protocol specifications</span></span>

<span data-ttu-id="ca963-141">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca963-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca963-142">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca963-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca963-143">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca963-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca963-144">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="ca963-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ca963-145">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca963-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca963-146">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="ca963-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="ca963-147">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca963-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca963-148">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ca963-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="ca963-149">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca963-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca963-150">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="ca963-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca963-151">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ca963-151">Header files</span></span>

<span data-ttu-id="ca963-152">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca963-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca963-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca963-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="ca963-154">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ca963-154">Mapitags.h</span></span>
  
> <span data-ttu-id="ca963-155">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca963-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca963-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca963-156">See also</span></span>



[<span data-ttu-id="ca963-157">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ca963-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca963-158">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca963-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca963-159">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca963-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca963-160">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ca963-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

