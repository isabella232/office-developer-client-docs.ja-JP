---
title: PidTagContainerHierarchy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332859"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="0f86b-103">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f86b-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="0f86b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f86b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f86b-105">子コンテナーに関する情報を提供する埋め込み階層テーブル オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="0f86b-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f86b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0f86b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f86b-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="0f86b-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="0f86b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0f86b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f86b-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="0f86b-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="0f86b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0f86b-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f86b-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0f86b-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0f86b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0f86b-112">Area:</span></span>  <br/> |<span data-ttu-id="0f86b-113">Container</span><span class="sxs-lookup"><span data-stu-id="0f86b-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f86b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="0f86b-114">Remarks</span></span>

<span data-ttu-id="0f86b-115">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="0f86b-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="0f86b-116">型の **プロパティとして**、PT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITableする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f86b-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="0f86b-117">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。</span><span class="sxs-lookup"><span data-stu-id="0f86b-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="0f86b-118">表の内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetHierarchyTable メソッドを呼び出す必要](imapicontainer-gethierarchytable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="0f86b-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="0f86b-119">詳細については、「階層テーブル [」を参照してください](hierarchy-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="0f86b-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="0f86b-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) **、PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) 、このプロパティは使用法で似ています。</span><span class="sxs-lookup"><span data-stu-id="0f86b-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="0f86b-121">複数の MAPI プロパティを使用すると、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0f86b-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="0f86b-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="0f86b-122">**Property**</span></span>|<span data-ttu-id="0f86b-123">**表**</span><span class="sxs-lookup"><span data-stu-id="0f86b-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f86b-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f86b-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f86b-125">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="0f86b-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="0f86b-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="0f86b-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="0f86b-127">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="0f86b-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="0f86b-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f86b-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f86b-129">関連付けられたコンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="0f86b-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="0f86b-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f86b-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f86b-131">添付ファイルテーブル</span><span class="sxs-lookup"><span data-stu-id="0f86b-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="0f86b-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0f86b-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0f86b-133">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="0f86b-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0f86b-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0f86b-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f86b-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0f86b-135">Protocol specifications</span></span>

<span data-ttu-id="0f86b-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f86b-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f86b-137">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="0f86b-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f86b-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f86b-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f86b-139">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="0f86b-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="0f86b-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f86b-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f86b-141">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="0f86b-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f86b-142">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0f86b-142">Header files</span></span>

<span data-ttu-id="0f86b-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f86b-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f86b-144">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0f86b-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f86b-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f86b-145">Mapitags.h</span></span>
  
> <span data-ttu-id="0f86b-146">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="0f86b-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f86b-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f86b-147">See also</span></span>



[<span data-ttu-id="0f86b-148">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0f86b-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f86b-149">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f86b-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f86b-150">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0f86b-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f86b-151">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="0f86b-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

