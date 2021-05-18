---
title: PidTagContainerContents 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283129"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="80b69-103">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80b69-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="80b69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80b69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80b69-105">コンテナーに関する情報を提供する埋め込みコンテンツ テーブル オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="80b69-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80b69-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="80b69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="80b69-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="80b69-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="80b69-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="80b69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="80b69-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="80b69-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="80b69-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="80b69-110">Data type:</span></span>  <br/> |<span data-ttu-id="80b69-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="80b69-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="80b69-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="80b69-112">Area:</span></span>  <br/> |<span data-ttu-id="80b69-113">Container</span><span class="sxs-lookup"><span data-stu-id="80b69-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80b69-114">注釈</span><span class="sxs-lookup"><span data-stu-id="80b69-114">Remarks</span></span>

<span data-ttu-id="80b69-115">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="80b69-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="80b69-116">型のプロパティPT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。その内容は [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドによってアクセスされ、インターフェイス識別子IID_IMAPITableする必要があります。</span><span class="sxs-lookup"><span data-stu-id="80b69-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="80b69-117">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合はオプションで報告できます。</span><span class="sxs-lookup"><span data-stu-id="80b69-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="80b69-118">テーブルの内容を取得するには、クライアント アプリケーションが [IMAPIContainer::GetContentsTable メソッドを呼び出す必要](imapicontainer-getcontentstable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="80b69-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="80b69-119">詳細については、「コンテンツ テーブル [」を参照してください](contents-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="80b69-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="80b69-120">このプロパティは **、PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) 、および **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) の使用法と似ています。</span><span class="sxs-lookup"><span data-stu-id="80b69-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="80b69-121">複数の MAPI プロパティを使用すると、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="80b69-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="80b69-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="80b69-122">**Property**</span></span>|<span data-ttu-id="80b69-123">**表**</span><span class="sxs-lookup"><span data-stu-id="80b69-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80b69-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="80b69-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="80b69-125">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="80b69-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="80b69-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80b69-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80b69-127">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="80b69-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="80b69-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80b69-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80b69-129">関連付けられたコンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="80b69-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="80b69-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80b69-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80b69-131">添付ファイルテーブル</span><span class="sxs-lookup"><span data-stu-id="80b69-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="80b69-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80b69-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80b69-133">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="80b69-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="80b69-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="80b69-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="80b69-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="80b69-135">Protocol specifications</span></span>

<span data-ttu-id="80b69-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80b69-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80b69-137">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="80b69-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="80b69-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80b69-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="80b69-139">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="80b69-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="80b69-140">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="80b69-140">Header files</span></span>

<span data-ttu-id="80b69-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="80b69-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="80b69-142">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="80b69-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="80b69-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="80b69-143">Mapitags.h</span></span>
  
> <span data-ttu-id="80b69-144">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="80b69-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80b69-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="80b69-145">See also</span></span>



[<span data-ttu-id="80b69-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="80b69-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="80b69-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="80b69-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="80b69-148">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="80b69-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="80b69-149">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="80b69-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

