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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316304"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="44807-103">PidTagFolderAssociatedContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44807-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="44807-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44807-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44807-105">関連する contents テーブルに関する情報を提供する、埋め込みコンテンツの table オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="44807-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44807-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44807-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44807-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="44807-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="44807-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44807-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44807-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="44807-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="44807-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44807-110">Data type:</span></span>  <br/> |<span data-ttu-id="44807-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="44807-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="44807-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44807-112">Area:</span></span>  <br/> |<span data-ttu-id="44807-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="44807-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44807-114">解説</span><span class="sxs-lookup"><span data-stu-id="44807-114">Remarks</span></span>

<span data-ttu-id="44807-115">関連付けられた contents テーブルは、標準の contents テーブルに表示されないサブフォルダーを表します。</span><span class="sxs-lookup"><span data-stu-id="44807-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="44807-116">フォルダーに関連付けられた、または非表示のメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="44807-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="44807-117">このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="44807-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="44807-118">**PT_OBJECT**型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。このコンテンツは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされ、 **IID_IMAPITable**インターフェイスの識別子が要求されます。</span><span class="sxs-lookup"><span data-stu-id="44807-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="44807-119">サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="44807-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="44807-120">表の内容を取得するには、クライアントアプリケーションは[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="44807-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="44807-121">フォルダコンテンツの表の詳細については、「[目次](contents-tables.md)表」および「[フォルダーコンテンツの表示](displaying-a-folder-contents-table.md)」の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44807-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="44807-122">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))、およびこのプロパティの使用方法は似ています。</span><span class="sxs-lookup"><span data-stu-id="44807-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="44807-123">複数の MAPI プロパティを使用して、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="44807-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="44807-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="44807-124">**Property**</span></span>|<span data-ttu-id="44807-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="44807-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44807-126">**PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44807-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44807-127">Contents テーブル</span><span class="sxs-lookup"><span data-stu-id="44807-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="44807-128">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44807-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44807-129">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="44807-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="44807-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="44807-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="44807-131">関連付けられたコンテンツテーブル</span><span class="sxs-lookup"><span data-stu-id="44807-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="44807-132">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44807-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44807-133">Attachment テーブル</span><span class="sxs-lookup"><span data-stu-id="44807-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="44807-134">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="44807-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="44807-135">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="44807-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="44807-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44807-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44807-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="44807-137">Protocol specifications</span></span>

<span data-ttu-id="44807-138">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44807-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44807-139">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="44807-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44807-140">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44807-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44807-141">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="44807-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="44807-142">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44807-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44807-143">IETF RFC2445、RFC2446、RFC2447、予定および会議のアイテムを変換します。</span><span class="sxs-lookup"><span data-stu-id="44807-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44807-144">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="44807-144">Header files</span></span>

<span data-ttu-id="44807-145">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44807-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="44807-146">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44807-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="44807-147">Mapitags</span><span class="sxs-lookup"><span data-stu-id="44807-147">Mapitags.h</span></span>
  
> <span data-ttu-id="44807-148">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="44807-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44807-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="44807-149">See also</span></span>



[<span data-ttu-id="44807-150">PidTagAssociatedContentCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44807-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="44807-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44807-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44807-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44807-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44807-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44807-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44807-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="44807-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

