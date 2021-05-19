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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342568"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="76508-103">PidTagMessageAttachments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76508-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="76508-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76508-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76508-105">メッセージの添付ファイルのテーブルを含む。</span><span class="sxs-lookup"><span data-stu-id="76508-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76508-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="76508-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="76508-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="76508-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="76508-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="76508-108">Identifier:</span></span>  <br/> |<span data-ttu-id="76508-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="76508-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="76508-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="76508-110">Data type:</span></span>  <br/> |<span data-ttu-id="76508-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="76508-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="76508-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="76508-112">Area:</span></span>  <br/> |<span data-ttu-id="76508-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="76508-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76508-114">注釈</span><span class="sxs-lookup"><span data-stu-id="76508-114">Remarks</span></span>

<span data-ttu-id="76508-115">このプロパティは [、IMAPIProp::CopyTo](imapiprop-copyto.md) 操作で除外するか [、IMAPIProp::CopyProps 操作に含](imapiprop-copyprops.md) めできます。</span><span class="sxs-lookup"><span data-stu-id="76508-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="76508-116">型のプロパティPT_OBJECT [IMAPIProp::GetProps メソッドでは正常に取得](imapiprop-getprops.md) できません。</span><span class="sxs-lookup"><span data-stu-id="76508-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="76508-117">その内容にアクセスするには [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを使用して、インターフェイス識別子 **IID_IMAPITableする必要** があります。</span><span class="sxs-lookup"><span data-stu-id="76508-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="76508-118">サービス プロバイダーは [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが設定されている場合は、それを報告する必要がありますが、設定されていない場合は、必要に応じて報告する場合があります。</span><span class="sxs-lookup"><span data-stu-id="76508-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="76508-119">表の内容を取得するには、クライアント アプリケーションが [IMessage::GetAttachmentTable メソッドを呼び出す必要](imessage-getattachmenttable.md) があります。</span><span class="sxs-lookup"><span data-stu-id="76508-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="76508-120">�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="76508-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="76508-121">このプロパティは [、SSubRestriction](ssubrestriction.md) 構造で指定することで、サブオブジェクト制限に使用できます。</span><span class="sxs-lookup"><span data-stu-id="76508-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="76508-122">これにより、クライアントはコンテナーのビューを、指定された条件を満たす添付ファイルを含むメッセージに制限できます。</span><span class="sxs-lookup"><span data-stu-id="76508-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="76508-123">メッセージは、添付ファイル テーブル内の少なくとも 1 つの行 (つまり、1 つの添付ファイル) がサブオブジェクト制限を満たす場合に表示できます。</span><span class="sxs-lookup"><span data-stu-id="76508-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="76508-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="76508-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="76508-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="76508-125">Protocol specifications</span></span>

<span data-ttu-id="76508-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76508-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76508-127">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="76508-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="76508-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76508-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76508-129">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="76508-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="76508-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="76508-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="76508-131">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="76508-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="76508-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="76508-132">Header files</span></span>

<span data-ttu-id="76508-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76508-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="76508-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="76508-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="76508-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="76508-135">Mapitags.h</span></span>
  
> <span data-ttu-id="76508-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="76508-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="76508-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="76508-137">See also</span></span>



[<span data-ttu-id="76508-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="76508-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="76508-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="76508-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="76508-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="76508-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="76508-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="76508-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

