---
title: PidTagFolderAssociatedContents 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391063"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="b8941-103">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8941-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="b8941-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8941-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8941-105">コンテンツが関連付けられているテーブルに関する情報を提供する埋め込まれたコンテンツ テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8941-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8941-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b8941-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b8941-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b8941-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="b8941-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b8941-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b8941-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="b8941-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="b8941-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b8941-110">Data type:</span></span>  <br/> |<span data-ttu-id="b8941-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="b8941-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="b8941-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b8941-112">Area:</span></span>  <br/> |<span data-ttu-id="b8941-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="b8941-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8941-114">備考</span><span class="sxs-lookup"><span data-stu-id="b8941-114">Remarks</span></span>

<span data-ttu-id="b8941-115">コンテンツが関連付けられているテーブルでは、標準的な内容の表に表示されていないサブフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="b8941-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="b8941-116">フォルダーの関連する、または非表示、メッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8941-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="b8941-117">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="b8941-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="b8941-118">**PT_OBJECT**の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **IID_IMAPITable**のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8941-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="b8941-119">サービス プロバイダーする必要があります報告して[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを報告ことがあります (オプション) が設定されている場合、またはに設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="b8941-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="b8941-120">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8941-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="b8941-121">フォルダーの内容のテーブルの詳細については、[テーブルの内容](contents-tables.md)と[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8941-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="b8941-122">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))、このプロパティは、使用状況に似ています。</span><span class="sxs-lookup"><span data-stu-id="b8941-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="b8941-123">いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b8941-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="b8941-124">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="b8941-124">**Property**</span></span>|<span data-ttu-id="b8941-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="b8941-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8941-126">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8941-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8941-127">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="b8941-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="b8941-128">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8941-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8941-129">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="b8941-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="b8941-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="b8941-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="b8941-131">関連付けられているコンテンツ」テーブル</span><span class="sxs-lookup"><span data-stu-id="b8941-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="b8941-132">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8941-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8941-133">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="b8941-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="b8941-134">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8941-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b8941-135">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="b8941-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b8941-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b8941-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b8941-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b8941-137">Protocol specifications</span></span>

<span data-ttu-id="b8941-138">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8941-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8941-139">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8941-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b8941-140">[[MS OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8941-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8941-141">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="b8941-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b8941-142">[[MS OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b8941-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b8941-143">IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムに変換します。</span><span class="sxs-lookup"><span data-stu-id="b8941-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b8941-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b8941-144">Header files</span></span>

<span data-ttu-id="b8941-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8941-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="b8941-146">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b8941-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="b8941-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b8941-147">Mapitags.h</span></span>
  
> <span data-ttu-id="b8941-148">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b8941-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b8941-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="b8941-149">See also</span></span>



[<span data-ttu-id="b8941-150">PidTagAssociatedContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8941-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="b8941-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8941-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b8941-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8941-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b8941-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b8941-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b8941-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b8941-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

