---
title: PidTagFolderAssociatedContents の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fe6395029e312a19bce6252e73b4616bb0aa0851
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802750"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="deac4-103">PidTagFolderAssociatedContents の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="deac4-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="deac4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="deac4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="deac4-105">コンテンツが関連付けられているテーブルに関する情報を提供する埋め込まれたコンテンツ テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="deac4-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="deac4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="deac4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="deac4-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="deac4-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="deac4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="deac4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="deac4-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="deac4-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="deac4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="deac4-110">Data type:</span></span>  <br/> |<span data-ttu-id="deac4-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="deac4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="deac4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="deac4-112">Area:</span></span>  <br/> |<span data-ttu-id="deac4-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="deac4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deac4-114">備考</span><span class="sxs-lookup"><span data-stu-id="deac4-114">Remarks</span></span>

<span data-ttu-id="deac4-115">コンテンツが関連付けられているテーブルでは、標準的な内容の表に表示されていないサブフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="deac4-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="deac4-116">フォルダーの関連する、または非表示、メッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="deac4-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="deac4-117">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="deac4-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="deac4-118">**PT_OBJECT**の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **IID_IMAPITable**のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="deac4-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="deac4-119">サービス プロバイダーする必要があります報告して[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを報告ことがあります (オプション) が設定されている場合、またはに設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="deac4-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="deac4-120">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="deac4-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="deac4-121">フォルダーの内容のテーブルの詳細については、[テーブルの内容](contents-tables.md)と[フォルダーの内容のテーブルを表示する](displaying-a-folder-contents-table.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="deac4-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="deac4-122">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))、このプロパティは、使用状況に似ています。</span><span class="sxs-lookup"><span data-stu-id="deac4-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="deac4-123">いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="deac4-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="deac4-124">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="deac4-124">**Property**</span></span>|<span data-ttu-id="deac4-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="deac4-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="deac4-126">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="deac4-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="deac4-127">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="deac4-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="deac4-128">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="deac4-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="deac4-129">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="deac4-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="deac4-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="deac4-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="deac4-131">関連付けられているコンテンツ」テーブル</span><span class="sxs-lookup"><span data-stu-id="deac4-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="deac4-132">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="deac4-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="deac4-133">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="deac4-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="deac4-134">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="deac4-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="deac4-135">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="deac4-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="deac4-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="deac4-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="deac4-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="deac4-137">Protocol specifications</span></span>

<span data-ttu-id="deac4-138">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deac4-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deac4-139">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="deac4-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="deac4-140">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deac4-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deac4-141">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="deac4-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="deac4-142">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="deac4-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="deac4-143">IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムに変換します。</span><span class="sxs-lookup"><span data-stu-id="deac4-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="deac4-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="deac4-144">Header files</span></span>

<span data-ttu-id="deac4-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="deac4-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="deac4-146">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="deac4-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="deac4-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="deac4-147">Mapitags.h</span></span>
  
> <span data-ttu-id="deac4-148">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="deac4-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="deac4-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="deac4-149">See also</span></span>



[<span data-ttu-id="deac4-150">PidTagAssociatedContentCount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="deac4-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="deac4-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="deac4-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="deac4-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="deac4-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="deac4-153">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="deac4-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="deac4-154">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="deac4-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

