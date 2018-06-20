---
title: PidTagMessageRecipients の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802992"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="34579-103">PidTagMessageRecipients の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="34579-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="34579-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="34579-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="34579-105">制限に一致する受信者オブジェクトを含むすべてのメッセージを検索する内容のテーブルに適用される制限の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="34579-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="34579-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="34579-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="34579-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="34579-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="34579-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="34579-108">Identifier:</span></span>  <br/> |<span data-ttu-id="34579-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="34579-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="34579-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="34579-110">Data type:</span></span>  <br/> |<span data-ttu-id="34579-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="34579-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="34579-112">領域:</span><span class="sxs-lookup"><span data-stu-id="34579-112">Area:</span></span>  <br/> |<span data-ttu-id="34579-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="34579-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34579-114">備考</span><span class="sxs-lookup"><span data-stu-id="34579-114">Remarks</span></span>

<span data-ttu-id="34579-115">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="34579-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="34579-116">**PT_OBJECT**の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで。</span><span class="sxs-lookup"><span data-stu-id="34579-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="34579-117">方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **IID_IMAPITable**のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="34579-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="34579-118">サービス プロバイダーする必要があります報告して[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを報告ことがあります (オプション) が設定されている場合、またはに設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="34579-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="34579-119">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="34579-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="34579-120">[SSubRestriction](ssubrestriction.md)構造体で指定して、サブオブジェクトの制限についてこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="34579-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="34579-121">これにより、会議の受信者を含むメッセージが条件を指定するためのコンテナーの表示を制限するクライアントです。</span><span class="sxs-lookup"><span data-stu-id="34579-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="34579-122">1 人の受信者、受信者テーブルの少なくとも 1 つの行は、サブオブジェクトの制限を満たしている場合に表示するメッセージが適用されます。</span><span class="sxs-lookup"><span data-stu-id="34579-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="34579-123">**メモ**サブオブジェクトの制限の結果を使用して、テーブル内のすべてのメッセージに対して、 [IMAPISession::OpenEntry](imapisession-openentry.md)に相当の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="34579-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="34579-124">クライアント アプリケーションは、検索するメッセージの数によっては、パフォーマンスに影響ことができます。</span><span class="sxs-lookup"><span data-stu-id="34579-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="34579-125">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティは、このプロパティは、使用状況に似ています。</span><span class="sxs-lookup"><span data-stu-id="34579-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="34579-126">いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="34579-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="34579-127">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="34579-127">**Property**</span></span>|<span data-ttu-id="34579-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="34579-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34579-129">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34579-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34579-130">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="34579-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="34579-131">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34579-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34579-132">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="34579-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="34579-133">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34579-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34579-134">関連付けられているコンテンツ」テーブル</span><span class="sxs-lookup"><span data-stu-id="34579-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="34579-135">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="34579-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="34579-136">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="34579-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="34579-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="34579-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="34579-138">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="34579-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="34579-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="34579-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="34579-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="34579-140">Protocol specifications</span></span>

<span data-ttu-id="34579-141">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34579-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34579-142">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="34579-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="34579-143">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34579-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34579-144">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="34579-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="34579-145">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34579-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34579-146">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="34579-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="34579-147">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34579-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34579-148">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="34579-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="34579-149">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="34579-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="34579-150">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="34579-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="34579-151">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="34579-151">Header files</span></span>

<span data-ttu-id="34579-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34579-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="34579-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="34579-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="34579-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34579-154">Mapitags.h</span></span>
  
> <span data-ttu-id="34579-155">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="34579-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34579-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="34579-156">See also</span></span>



[<span data-ttu-id="34579-157">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="34579-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34579-158">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="34579-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34579-159">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="34579-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34579-160">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="34579-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

