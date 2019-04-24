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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283129"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="41b6b-103">PidTagContainerContents 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="41b6b-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="41b6b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41b6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41b6b-105">コンテナーに関する情報を提供する、埋め込みコンテンツの table オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="41b6b-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="41b6b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="41b6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41b6b-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="41b6b-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="41b6b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="41b6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41b6b-109">0x360f</span><span class="sxs-lookup"><span data-stu-id="41b6b-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="41b6b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="41b6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="41b6b-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="41b6b-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="41b6b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="41b6b-112">Area:</span></span>  <br/> |<span data-ttu-id="41b6b-113">Container</span><span class="sxs-lookup"><span data-stu-id="41b6b-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b6b-114">解説</span><span class="sxs-lookup"><span data-stu-id="41b6b-114">Remarks</span></span>

<span data-ttu-id="41b6b-115">このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="41b6b-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="41b6b-116">PT_OBJECT 型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。このコンテンツは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされ、IID_IMAPITable インターフェイスの識別子が要求されます。</span><span class="sxs-lookup"><span data-stu-id="41b6b-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="41b6b-117">サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="41b6b-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="41b6b-118">表の内容を取得するには、クライアントアプリケーションは[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="41b6b-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="41b6b-119">詳細については、「 [Contents Tables](contents-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="41b6b-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="41b6b-120">このプロパティ、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))、および**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) は、使用方法に似ています。</span><span class="sxs-lookup"><span data-stu-id="41b6b-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="41b6b-121">複数の MAPI プロパティを使用して、テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="41b6b-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="41b6b-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="41b6b-122">**Property**</span></span>|<span data-ttu-id="41b6b-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="41b6b-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41b6b-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="41b6b-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="41b6b-125">Contents テーブル</span><span class="sxs-lookup"><span data-stu-id="41b6b-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="41b6b-126">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b6b-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b6b-127">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="41b6b-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="41b6b-128">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b6b-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b6b-129">関連付けられたコンテンツテーブル</span><span class="sxs-lookup"><span data-stu-id="41b6b-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="41b6b-130">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b6b-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b6b-131">Attachment テーブル</span><span class="sxs-lookup"><span data-stu-id="41b6b-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="41b6b-132">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="41b6b-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="41b6b-133">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="41b6b-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="41b6b-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="41b6b-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41b6b-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="41b6b-135">Protocol specifications</span></span>

<span data-ttu-id="41b6b-136">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41b6b-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41b6b-137">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="41b6b-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="41b6b-138">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41b6b-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41b6b-139">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="41b6b-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41b6b-140">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="41b6b-140">Header files</span></span>

<span data-ttu-id="41b6b-141">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41b6b-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="41b6b-142">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="41b6b-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="41b6b-143">Mapitags</span><span class="sxs-lookup"><span data-stu-id="41b6b-143">Mapitags.h</span></span>
  
> <span data-ttu-id="41b6b-144">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="41b6b-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41b6b-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="41b6b-145">See also</span></span>



[<span data-ttu-id="41b6b-146">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="41b6b-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41b6b-147">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="41b6b-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41b6b-148">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="41b6b-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41b6b-149">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="41b6b-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

