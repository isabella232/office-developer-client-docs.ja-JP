---
title: PidTagContainerContents の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802593"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="c94c4-103">PidTagContainerContents の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c94c4-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="c94c4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c94c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c94c4-105">コンテナーに関する情報を提供する埋め込まれたコンテンツ テーブル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c94c4-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c94c4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c94c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c94c4-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="c94c4-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="c94c4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c94c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c94c4-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="c94c4-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="c94c4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c94c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c94c4-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="c94c4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="c94c4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c94c4-112">Area:</span></span>  <br/> |<span data-ttu-id="c94c4-113">Container</span><span class="sxs-lookup"><span data-stu-id="c94c4-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c94c4-114">備考</span><span class="sxs-lookup"><span data-stu-id="c94c4-114">Remarks</span></span>

<span data-ttu-id="c94c4-115">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="c94c4-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="c94c4-116">PT_OBJECT の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) IID_IMAPITable のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94c4-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="c94c4-117">サービス プロバイダーする必要がありますに報告して、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドが設定されているが報告したことができます (オプション)、または設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="c94c4-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="c94c4-118">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94c4-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="c94c4-119">詳細については、[内容のテーブル](contents-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c94c4-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="c94c4-120">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) と**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) は、このプロパティは、使用状況に似ています。</span><span class="sxs-lookup"><span data-stu-id="c94c4-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="c94c4-121">いくつかの MAPI プロパティは、テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="c94c4-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="c94c4-122">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="c94c4-122">**Property**</span></span>|<span data-ttu-id="c94c4-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="c94c4-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c94c4-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="c94c4-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="c94c4-125">コンテンツ テーブル</span><span class="sxs-lookup"><span data-stu-id="c94c4-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="c94c4-126">**PR_CONTAINER_HIERARCHY**([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c94c4-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c94c4-127">階層テーブル</span><span class="sxs-lookup"><span data-stu-id="c94c4-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="c94c4-128">**PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c94c4-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c94c4-129">関連付けられているコンテンツ」テーブル</span><span class="sxs-lookup"><span data-stu-id="c94c4-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="c94c4-130">**PR_MESSAGE_ATTACHMENTS**([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c94c4-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c94c4-131">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="c94c4-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="c94c4-132">**PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c94c4-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="c94c4-133">受信者テーブル</span><span class="sxs-lookup"><span data-stu-id="c94c4-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c94c4-134">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c94c4-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c94c4-135">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c94c4-135">Protocol specifications</span></span>

<span data-ttu-id="c94c4-136">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c94c4-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c94c4-137">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c94c4-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c94c4-138">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c94c4-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c94c4-139">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c94c4-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c94c4-140">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c94c4-140">Header files</span></span>

<span data-ttu-id="c94c4-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c94c4-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="c94c4-142">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c94c4-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="c94c4-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c94c4-143">Mapitags.h</span></span>
  
> <span data-ttu-id="c94c4-144">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c94c4-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c94c4-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="c94c4-145">See also</span></span>



[<span data-ttu-id="c94c4-146">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c94c4-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c94c4-147">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c94c4-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c94c4-148">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c94c4-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c94c4-149">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c94c4-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

