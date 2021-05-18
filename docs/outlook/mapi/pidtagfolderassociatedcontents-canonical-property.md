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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316304"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="3cc38-103">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cc38-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="3cc38-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cc38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cc38-105">関連付けられたコンテンツ テーブルに関する情報を提供する埋め込みコンテンツ テーブル オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="3cc38-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3cc38-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3cc38-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cc38-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3cc38-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="3cc38-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3cc38-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cc38-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="3cc38-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="3cc38-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3cc38-110">Data type:</span></span>  <br/> |<span data-ttu-id="3cc38-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="3cc38-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="3cc38-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3cc38-112">Area:</span></span>  <br/> |<span data-ttu-id="3cc38-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="3cc38-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cc38-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3cc38-114">Remarks</span></span>

<span data-ttu-id="3cc38-115">関連付けられたコンテンツ テーブルは、標準コンテンツ テーブルに表示されないサブフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="3cc38-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="3cc38-116">フォルダーに関連付けられているメッセージまたは非表示のメッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3cc38-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="3cc38-117">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="3cc38-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="3cc38-118">型の **プロパティとして**、PT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITable **要求されます** 。</span><span class="sxs-lookup"><span data-stu-id="3cc38-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="3cc38-119">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合は、必要に応じて報告する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3cc38-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="3cc38-120">テーブルの内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetContentsTable メソッドを呼び出す必要](imapicontainer-getcontentstable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="3cc38-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="3cc38-121">フォルダーコンテンツ テーブルの詳細については、「コンテンツ テーブル」および「 [フォルダー](contents-tables.md) [コンテンツ テーブルの表示」を参照してください](displaying-a-folder-contents-table.md)。</span><span class="sxs-lookup"><span data-stu-id="3cc38-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="3cc38-122">この **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) 、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) であり、このプロパティは使用法で似ています。</span><span class="sxs-lookup"><span data-stu-id="3cc38-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="3cc38-123">複数の MAPI プロパティを使用すると、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3cc38-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="3cc38-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="3cc38-124">**Property**</span></span>|<span data-ttu-id="3cc38-125">**表**</span><span class="sxs-lookup"><span data-stu-id="3cc38-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cc38-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc38-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc38-127">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="3cc38-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="3cc38-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc38-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc38-129">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="3cc38-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="3cc38-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="3cc38-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="3cc38-131">関連付けられたコンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="3cc38-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="3cc38-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc38-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc38-133">添付ファイルテーブル</span><span class="sxs-lookup"><span data-stu-id="3cc38-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="3cc38-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc38-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc38-135">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="3cc38-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3cc38-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3cc38-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cc38-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3cc38-137">Protocol specifications</span></span>

<span data-ttu-id="3cc38-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cc38-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cc38-139">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="3cc38-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cc38-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cc38-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cc38-141">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="3cc38-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3cc38-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cc38-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cc38-143">IETF RFC2445、RFC2446、RFC2447、および予定と会議アイテムの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="3cc38-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cc38-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3cc38-144">Header files</span></span>

<span data-ttu-id="3cc38-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cc38-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cc38-146">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3cc38-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cc38-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3cc38-147">Mapitags.h</span></span>
  
> <span data-ttu-id="3cc38-148">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3cc38-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cc38-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="3cc38-149">See also</span></span>



[<span data-ttu-id="3cc38-150">PidTagAssociatedContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cc38-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="3cc38-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3cc38-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cc38-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3cc38-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cc38-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3cc38-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cc38-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3cc38-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

