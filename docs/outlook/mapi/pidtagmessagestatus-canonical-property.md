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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355721"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="44992-103">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44992-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="44992-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44992-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44992-105">コンテンツ テーブル内のメッセージの状態を定義するフラグの 32 ビット ビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="44992-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44992-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="44992-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44992-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="44992-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="44992-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="44992-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44992-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="44992-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="44992-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="44992-110">Data type:</span></span>  <br/> |<span data-ttu-id="44992-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="44992-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="44992-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="44992-112">Area:</span></span>  <br/> |<span data-ttu-id="44992-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="44992-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44992-114">注釈</span><span class="sxs-lookup"><span data-stu-id="44992-114">Remarks</span></span>

<span data-ttu-id="44992-115">メッセージは、コンテンツ テーブルと 1 つ以上の検索結果テーブルに存在し、メッセージの各インスタンスの状態が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="44992-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="44992-116">このプロパティは、メッセージのプロパティではなく、コンテンツ テーブル内の列と見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="44992-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="44992-117">クライアント アプリケーションは、このプロパティで次の 1 つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="44992-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="44992-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="44992-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="44992-119">メッセージが返信されました。</span><span class="sxs-lookup"><span data-stu-id="44992-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="44992-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="44992-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="44992-121">メッセージは、後続の削除のマークが付けされています。</span><span class="sxs-lookup"><span data-stu-id="44992-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="44992-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="44992-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="44992-123">メッセージが下書きリビジョンの状態です。</span><span class="sxs-lookup"><span data-stu-id="44992-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="44992-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="44992-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="44992-125">メッセージは受信者のフォルダー表示から抑制されます。</span><span class="sxs-lookup"><span data-stu-id="44992-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="44992-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="44992-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="44992-127">メッセージは受信者のフォルダー表示で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="44992-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="44992-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="44992-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="44992-129">メッセージは、ローカル クライアントにダウンロードせずにリモート メッセージ ストアで削除のマークが付けされています。</span><span class="sxs-lookup"><span data-stu-id="44992-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="44992-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="44992-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="44992-131">メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロードするマークが付けされています。</span><span class="sxs-lookup"><span data-stu-id="44992-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="44992-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="44992-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="44992-133">メッセージは、クライアント定義の目的でタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="44992-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="44992-134">クライアントMSGSTATUS_DELMARKED、MSGSTATUS_HIDDEN、MSGSTATUS_HIGHLIGHTED、MSGSTATUS_TAGGED **フラグが** 定義されます。 </span><span class="sxs-lookup"><span data-stu-id="44992-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="44992-135">トランスポートプロバイダーとストア プロバイダーは、アクションなしでこれらのビットを渡します。</span><span class="sxs-lookup"><span data-stu-id="44992-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="44992-136">クライアントは、アプリケーションに適した方法でこれらの値を解釈できます。</span><span class="sxs-lookup"><span data-stu-id="44992-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="44992-137">多くのクライアントでこのプロパティを使用する方法の 1 つは、削除のマークが付いたメッセージを代表的なアイコンで表示する方法です。</span><span class="sxs-lookup"><span data-stu-id="44992-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="44992-138">リモート ビューアー クライアントは **、リモート\*\*\*\*MSGSTATUS_REMOTE_DELETEプロバイダー** MSGSTATUS_REMOTE_DOWNLOADヘッダー フォルダー内のメッセージに対して、そのメッセージを設定または設定できます。</span><span class="sxs-lookup"><span data-stu-id="44992-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="44992-139">クライアント アプリケーションは、このフォルダー内の各メッセージ ヘッダーを調べて、リモート メッセージ ストアでメッセージをダウンロードするか削除するか判断できます。</span><span class="sxs-lookup"><span data-stu-id="44992-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="44992-140">次に [、IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) メソッドを使用して、適切なフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="44992-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="44992-141">**SetMessageStatus** は、このプロパティのフラグを設定する唯一の方法です。 [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="44992-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="44992-142">このプロパティを取得するには、クライアントは [IMAPIProp::GetProps ではなく IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) [を呼び出します](imapiprop-getprops.md)。</span><span class="sxs-lookup"><span data-stu-id="44992-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="44992-143">このプロパティのビット 16 ~ 31 (0x10000 ~ 0x80000000) は、対人間メッセージ (IPM) クライアント アプリケーションで使用できます。</span><span class="sxs-lookup"><span data-stu-id="44992-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="44992-144">その他のすべてのビットは、MAPI で使用するために予約されています。前の表で定義されていない場合は、最初は 0 に設定し、その後変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44992-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="44992-145">関連リソース</span><span class="sxs-lookup"><span data-stu-id="44992-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44992-146">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="44992-146">Protocol specifications</span></span>

<span data-ttu-id="44992-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44992-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44992-148">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="44992-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44992-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44992-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44992-150">サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。</span><span class="sxs-lookup"><span data-stu-id="44992-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44992-151">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="44992-151">Header files</span></span>

<span data-ttu-id="44992-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44992-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="44992-153">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="44992-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="44992-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44992-154">Mapitags.h</span></span>
  
> <span data-ttu-id="44992-155">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="44992-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44992-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="44992-156">See also</span></span>



[<span data-ttu-id="44992-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="44992-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="44992-158">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="44992-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44992-159">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="44992-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44992-160">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="44992-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44992-161">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="44992-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

