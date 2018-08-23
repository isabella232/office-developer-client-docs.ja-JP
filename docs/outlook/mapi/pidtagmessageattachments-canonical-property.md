---
title: PidTagMessageAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b375ef279fc50aecca75b60d8379438c56f13420
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569338"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="6cd6c-103">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6cd6c-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="6cd6c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cd6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cd6c-105">制限に一致する添付ファイルの下位オブジェクトが含まれているすべてのメッセージを検索する内容のテーブルに適用される制限の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain attachment subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cd6c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cd6c-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="6cd6c-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="6cd6c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cd6c-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="6cd6c-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="6cd6c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6cd6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cd6c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="6cd6c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="6cd6c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6cd6c-112">Area:</span></span>  <br/> |<span data-ttu-id="6cd6c-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="6cd6c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cd6c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6cd6c-114">Remarks</span></span>

<span data-ttu-id="6cd6c-115">このプロパティは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)操作で除外または[IMAPIProp::CopyProps](imapiprop-copyprops.md)操作に含まれることができます。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="6cd6c-116">PT_OBJECT の型のプロパティとして、正常に取得できません、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドで。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="6cd6c-117">方式では[IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **IID_IMAPITable**のインタ フェース識別子を要求するその内容にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="6cd6c-118">サービス プロバイダーする必要があります報告して[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを報告ことがあります (オプション) が設定されている場合、またはに設定されていない場合はありません。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="6cd6c-119">テーブルの内容を取得するには、クライアント アプリケーションは、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="6cd6c-120">�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="6cd6c-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="6cd6c-121">[SSubRestriction](ssubrestriction.md)構造体で指定して、サブオブジェクトの制限についてこのプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="6cd6c-122">これにより、クライアントが会議の添付ファイル付きのメッセージを検索条件に一致するためのコンテナーの表示を制限します。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="6cd6c-123">1 つの添付ファイル、添付ファイル テーブル内の少なくとも 1 つの行は、サブオブジェクトの制限を満たしている場合に表示するメッセージが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6cd6c-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6cd6c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cd6c-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6cd6c-125">Protocol specifications</span></span>

<span data-ttu-id="6cd6c-126">[[MS OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-126">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-127">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="6cd6c-128">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-128">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-129">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="6cd6c-130">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd6c-130">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd6c-131">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cd6c-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6cd6c-132">Header files</span></span>

<span data-ttu-id="6cd6c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cd6c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cd6c-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cd6c-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cd6c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="6cd6c-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cd6c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cd6c-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="6cd6c-137">See also</span></span>



[<span data-ttu-id="6cd6c-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6cd6c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cd6c-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6cd6c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cd6c-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6cd6c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cd6c-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6cd6c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

