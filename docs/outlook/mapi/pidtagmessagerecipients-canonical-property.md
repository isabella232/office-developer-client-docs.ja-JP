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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355686"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="b9914-103">PidTagMessageRecipients 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9914-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="b9914-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9914-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9914-105">制限を満たす受信者サブオブジェクトを含むすべてのメッセージを検索するためにコンテンツ テーブルに適用できる制限のテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9914-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9914-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b9914-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9914-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="b9914-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="b9914-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b9914-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9914-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="b9914-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="b9914-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b9914-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9914-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b9914-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b9914-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b9914-112">Area:</span></span>  <br/> |<span data-ttu-id="b9914-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="b9914-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9914-114">注釈</span><span class="sxs-lookup"><span data-stu-id="b9914-114">Remarks</span></span>

<span data-ttu-id="b9914-115">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="b9914-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b9914-116">型の **プロパティPT_OBJECT** [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドでは正常に取得できません。</span><span class="sxs-lookup"><span data-stu-id="b9914-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="b9914-117">その内容にアクセスするには [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用して、インターフェイス識別子 **IID_IMAPITableする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="b9914-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="b9914-118">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合は、必要に応じて報告する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b9914-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b9914-119">表の内容を取得するには、クライアント アプリケーションが [IMessage::GetRecipientTable メソッドを呼び出す必要](imessage-getrecipienttable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="b9914-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="b9914-120">このプロパティは [、SSubRestriction](ssubrestriction.md) 構造で指定することで、サブオブジェクト制限に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9914-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="b9914-121">これにより、クライアントはコンテナーのビューを、指定された条件を満たす受信者とのメッセージに制限できます。</span><span class="sxs-lookup"><span data-stu-id="b9914-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="b9914-122">メッセージは、受信者テーブル内の少なくとも 1 行(つまり、1 人の受信者がサブオブジェクト制限を満たす場合)を表示する資格を与える。</span><span class="sxs-lookup"><span data-stu-id="b9914-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="b9914-123">**メモ** サブオブジェクト制限の結果の使用は、テーブル内のすべてのメッセージに対する [IMAPISession::OpenEntry](imapisession-openentry.md) 呼び出しと同じです。</span><span class="sxs-lookup"><span data-stu-id="b9914-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="b9914-124">クライアント アプリケーションと検索するメッセージの数に応じて、パフォーマンスに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b9914-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="b9914-125">プロパティ **PR_MESSAGE_ATTACHMENTS** プロパティ [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)プロパティと、このプロパティは使用法で似ています。</span><span class="sxs-lookup"><span data-stu-id="b9914-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="b9914-126">複数の MAPI プロパティを使用すると、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b9914-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="b9914-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="b9914-127">**Property**</span></span>|<span data-ttu-id="b9914-128">**表**</span><span class="sxs-lookup"><span data-stu-id="b9914-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9914-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9914-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b9914-130">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="b9914-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="b9914-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9914-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b9914-132">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="b9914-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="b9914-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9914-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b9914-134">関連付けられたコンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="b9914-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="b9914-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b9914-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b9914-136">添付ファイルテーブル</span><span class="sxs-lookup"><span data-stu-id="b9914-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="b9914-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="b9914-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="b9914-138">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="b9914-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b9914-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b9914-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9914-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b9914-140">Protocol specifications</span></span>

<span data-ttu-id="b9914-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9914-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9914-142">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="b9914-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9914-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9914-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9914-144">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="b9914-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b9914-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9914-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9914-146">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="b9914-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b9914-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9914-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9914-148">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="b9914-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="b9914-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9914-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9914-150">メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。</span><span class="sxs-lookup"><span data-stu-id="b9914-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9914-151">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b9914-151">Header files</span></span>

<span data-ttu-id="b9914-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9914-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9914-153">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9914-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9914-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b9914-154">Mapitags.h</span></span>
  
> <span data-ttu-id="b9914-155">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="b9914-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9914-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9914-156">See also</span></span>



[<span data-ttu-id="b9914-157">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b9914-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9914-158">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9914-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9914-159">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b9914-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9914-160">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="b9914-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

