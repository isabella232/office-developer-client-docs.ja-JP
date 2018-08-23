---
title: PidTagMessageStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 21336e158d21bba6c7204eb446df3efc80b70e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802999"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="6ff0b-103">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ff0b-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="6ff0b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ff0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ff0b-105">コンテンツ テーブル内のメッセージの状態を定義するフラグの 32 ビットのビットマップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ff0b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6ff0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ff0b-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="6ff0b-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="6ff0b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6ff0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ff0b-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="6ff0b-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="6ff0b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6ff0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ff0b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6ff0b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6ff0b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6ff0b-112">Area:</span></span>  <br/> |<span data-ttu-id="6ff0b-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="6ff0b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ff0b-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6ff0b-114">Remarks</span></span>

<span data-ttu-id="6ff0b-115">コンテンツ テーブルと 1 つまたは複数の検索結果のテーブルにメッセージが存在し、メッセージの各インスタンスが別の状態を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="6ff0b-116">このプロパティと見なすことが、メッセージ、内容のテーブル内の列のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="6ff0b-117">クライアント アプリケーションでは、このプロパティで次のフラグのいずれかを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="6ff0b-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="6ff0b-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="6ff0b-119">メッセージは既に返信されています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="6ff0b-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="6ff0b-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="6ff0b-121">メッセージは、それ以降の削除のマークされています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="6ff0b-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="6ff0b-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="6ff0b-123">メッセージは、ドラフトのリビジョンの状態です。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="6ff0b-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="6ff0b-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="6ff0b-125">メッセージは、宛先のフォルダーを表示から非表示にするのには。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="6ff0b-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="6ff0b-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="6ff0b-127">メッセージでは、宛先のフォルダーの表示で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="6ff0b-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="6ff0b-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="6ff0b-129">メッセージは、ローカル クライアントにダウンロードすることがなくリモート メッセージ ストアを削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="6ff0b-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="6ff0b-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="6ff0b-131">メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロード用にマークされています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="6ff0b-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="6ff0b-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="6ff0b-133">クライアント定義の目的は、メッセージをタグ付けされました。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="6ff0b-134">**MSGSTATUS_DELMARKED**、 **MSGSTATUS_HIDDEN**、 **MSGSTATUS_HIGHLIGHTED**、および**MSGSTATUS_TAGGED**のフラグは、クライアントによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="6ff0b-135">トランスポートとストアのプロバイダーは、操作をしなくても、これらのビットを渡します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="6ff0b-136">クライアントは、アプリケーションに適した任意の方法でこれらの値を解釈できます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="6ff0b-137">多数のクライアントがこのプロパティを使用する方法の 1 つでは、代表的なアイコンが削除対象としてマークされたメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="6ff0b-138">ビューアーがリモート クライアントを設定できます**MSGSTATUS_REMOTE_DELETE**または**MSGSTATUS_REMOTE_DOWNLOAD**メッセージをリモート トランスポート プロバイダーによって提供されたヘッダーのフォルダーにします。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="6ff0b-139">クライアント アプリケーションでは、各メッセージをダウンロードするか、リモート メッセージ ストアを削除するかどうかを判断するには、このフォルダー内のメッセージのヘッダーを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="6ff0b-140">[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)メソッドを使用して、適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="6ff0b-141">**SetMessageStatus**は、このプロパティのフラグのいずれかを設定する唯一の方法[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="6ff0b-142">このプロパティを取得するためには、クライアントは、 [IMAPIProp::GetProps](imapiprop-getprops.md)ではなく、 [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="6ff0b-143">31 (0x80000000 から 0x10000) をこのプロパティの 16 ビットは個人間メッセージ (IPM) のクライアント アプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="6ff0b-144">他のすべてのビットは、使用するため、MAPI ので予約されています上記の表で定義されていないものは、最初に 0 に設定する必要があり、その後変更されていません。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6ff0b-145">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6ff0b-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ff0b-146">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6ff0b-146">Protocol specifications</span></span>

<span data-ttu-id="6ff0b-147">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ff0b-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ff0b-148">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ff0b-149">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ff0b-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ff0b-150">サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ff0b-151">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6ff0b-151">Header files</span></span>

<span data-ttu-id="6ff0b-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ff0b-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ff0b-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ff0b-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ff0b-154">Mapitags.h</span></span>
  
> <span data-ttu-id="6ff0b-155">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6ff0b-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ff0b-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ff0b-156">See also</span></span>



[<span data-ttu-id="6ff0b-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6ff0b-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="6ff0b-158">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ff0b-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ff0b-159">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6ff0b-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ff0b-160">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ff0b-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ff0b-161">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6ff0b-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

