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
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355721"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="1fe08-103">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fe08-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1fe08-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fe08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fe08-105">コンテンツテーブル内のメッセージの状態を定義するフラグの32ビットビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fe08-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1fe08-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fe08-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="1fe08-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="1fe08-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1fe08-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fe08-109">0x0e17</span><span class="sxs-lookup"><span data-stu-id="1fe08-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="1fe08-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1fe08-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fe08-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1fe08-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1fe08-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1fe08-112">Area:</span></span>  <br/> |<span data-ttu-id="1fe08-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="1fe08-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fe08-114">解説</span><span class="sxs-lookup"><span data-stu-id="1fe08-114">Remarks</span></span>

<span data-ttu-id="1fe08-115">メッセージは、コンテンツテーブルと1つ以上の検索結果テーブルに存在し、メッセージの各インスタンスの状態が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1fe08-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="1fe08-116">このプロパティは、メッセージのプロパティではなく、contents テーブルの列であるとみなされません。</span><span class="sxs-lookup"><span data-stu-id="1fe08-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="1fe08-117">クライアントアプリケーションでは、このプロパティに次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="1fe08-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="1fe08-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="1fe08-119">メッセージに返信しました。</span><span class="sxs-lookup"><span data-stu-id="1fe08-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="1fe08-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="1fe08-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="1fe08-121">このメッセージは、その後の削除のためにマークされています。</span><span class="sxs-lookup"><span data-stu-id="1fe08-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="1fe08-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="1fe08-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="1fe08-123">メッセージは下書きの改訂状態です。</span><span class="sxs-lookup"><span data-stu-id="1fe08-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="1fe08-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="1fe08-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="1fe08-125">メッセージは、受信者のフォルダー表示から抑制されます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="1fe08-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="1fe08-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="1fe08-127">メッセージは、受信者のフォルダー表示で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="1fe08-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="1fe08-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="1fe08-129">メッセージがリモートメッセージストアで削除対象としてマークされ、ローカルクライアントにダウンロードされていません。</span><span class="sxs-lookup"><span data-stu-id="1fe08-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="1fe08-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1fe08-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1fe08-131">メッセージは、リモートメッセージストアからローカルクライアントにダウンロードするようにマークされています。</span><span class="sxs-lookup"><span data-stu-id="1fe08-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="1fe08-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="1fe08-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="1fe08-133">メッセージには、クライアント定義の目的のタグが付けられています。</span><span class="sxs-lookup"><span data-stu-id="1fe08-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="1fe08-134">**MSGSTATUS_DELMARKED**、 **MSGSTATUS_HIDDEN**、 **MSGSTATUS_HIGHLIGHTED**、および**MSGSTATUS_TAGGED**の各フラグはクライアントによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="1fe08-135">トランスポートプロバイダーとストアプロバイダーは、操作を行わずにこれらのビットを渡します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="1fe08-136">クライアントは、これらの値をアプリケーションに適した方法で解釈できます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="1fe08-137">多くのクライアントがこのプロパティを使用する方法の1つは、削除対象としてマークされたメッセージを代表アイコンで表示することです。</span><span class="sxs-lookup"><span data-stu-id="1fe08-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="1fe08-138">リモートビューアークライアントは、リモートトランスポートプロバイダーによって提供されるヘッダーフォルダー内のメッセージに**MSGSTATUS_REMOTE_DELETE**または**MSGSTATUS_REMOTE_DOWNLOAD**を設定できます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="1fe08-139">クライアントアプリケーションは、このフォルダー内の各メッセージヘッダーを調べて、リモートメッセージストアでメッセージをダウンロードまたは削除する必要があるかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="1fe08-140">次に、 [imapifolder:: setmessagestatus](imapifolder-setmessagestatus.md)メソッドを使用して、適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="1fe08-141">**setmessagestatus**は、このプロパティの任意のフラグを設定する唯一の方法です。[imapiprop:: setprops](imapiprop-setprops.md)メソッドを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1fe08-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="1fe08-142">このプロパティを取得するために、クライアントは imapifolder [:: GetProps](imapiprop-getprops.md)ではなく、 [imapifolder:: getmessagestatus](imapifolder-getmessagestatus.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="1fe08-143">このプロパティのビット16から 31 (の場合は 0x80000000 ~ 0x80000000) は、個人間メッセージ (IPM) クライアントアプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1fe08-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="1fe08-144">他のすべてのビットは MAPI での使用のために予約されています。前の表で定義されていないものは、最初は0に設定され、その後は変更されません。</span><span class="sxs-lookup"><span data-stu-id="1fe08-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1fe08-145">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1fe08-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1fe08-146">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1fe08-146">Protocol specifications</span></span>

<span data-ttu-id="1fe08-147">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fe08-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fe08-148">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1fe08-149">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1fe08-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1fe08-150">サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1fe08-151">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1fe08-151">Header files</span></span>

<span data-ttu-id="1fe08-152">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fe08-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fe08-153">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1fe08-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fe08-154">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1fe08-154">Mapitags.h</span></span>
  
> <span data-ttu-id="1fe08-155">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1fe08-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fe08-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fe08-156">See also</span></span>



[<span data-ttu-id="1fe08-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1fe08-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="1fe08-158">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1fe08-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fe08-159">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fe08-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fe08-160">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1fe08-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fe08-161">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1fe08-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

