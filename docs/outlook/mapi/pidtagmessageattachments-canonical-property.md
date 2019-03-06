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
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413974"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="144b6-103">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="144b6-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="144b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="144b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="144b6-105">メッセージの添付ファイルの表が保存されています。</span><span class="sxs-lookup"><span data-stu-id="144b6-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="144b6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="144b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="144b6-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="144b6-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="144b6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="144b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="144b6-109">0x0e13</span><span class="sxs-lookup"><span data-stu-id="144b6-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="144b6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="144b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="144b6-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="144b6-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="144b6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="144b6-112">Area:</span></span>  <br/> |<span data-ttu-id="144b6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="144b6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="144b6-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="144b6-114">Remarks</span></span>

<span data-ttu-id="144b6-115">このプロパティは、 [imapiprop:: CopyTo](imapiprop-copyto.md)操作で除外することも、 [imapiprop:: copyprops](imapiprop-copyprops.md)操作に含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="144b6-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="144b6-116">PT_OBJECT 型のプロパティとして、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドによって正常に取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="144b6-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="144b6-117">このコンテンツは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドによってアクセスされ、 **IID_IMAPITable**インターフェイスの識別子が要求されます。</span><span class="sxs-lookup"><span data-stu-id="144b6-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="144b6-118">サービスプロバイダーは、設定されている場合は[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドに報告する必要がありますが、設定されていない場合はレポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="144b6-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="144b6-119">表の内容を取得するには、クライアントアプリケーションは[IMessage:: getattachmenttable](imessage-getattachmenttable.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="144b6-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="144b6-120">�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="144b6-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="144b6-121">このプロパティは、 [ssubrestriction](ssubrestriction.md)構造で指定することによって、サブプロパティの制限に使用できます。</span><span class="sxs-lookup"><span data-stu-id="144b6-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="144b6-122">これにより、クライアントは、指定した条件に一致する添付ファイルを持つメッセージにコンテナーのビューを制限できます。</span><span class="sxs-lookup"><span data-stu-id="144b6-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="144b6-123">添付ファイルテーブルにある1つ以上の行、つまり1つの添付ファイルがサブオブジェクト制限を満たす場合は、メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="144b6-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="144b6-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="144b6-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="144b6-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="144b6-125">Protocol specifications</span></span>

<span data-ttu-id="144b6-126">[[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="144b6-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="144b6-127">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="144b6-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="144b6-128">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="144b6-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="144b6-129">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="144b6-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="144b6-130">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="144b6-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="144b6-131">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="144b6-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="144b6-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="144b6-132">Header files</span></span>

<span data-ttu-id="144b6-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="144b6-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="144b6-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="144b6-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="144b6-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="144b6-135">Mapitags.h</span></span>
  
> <span data-ttu-id="144b6-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="144b6-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="144b6-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="144b6-137">See also</span></span>



[<span data-ttu-id="144b6-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="144b6-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="144b6-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="144b6-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="144b6-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="144b6-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="144b6-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="144b6-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

