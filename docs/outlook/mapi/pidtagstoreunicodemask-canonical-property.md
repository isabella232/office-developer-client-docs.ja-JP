---
title: PidTagStoreUnicodeMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreUnicodeMask
api_type:
- COM
ms.assetid: a6082162-2a74-4850-a0df-4bdbc67b41d8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339320"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="bef72-103">PidTagStoreUnicodeMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bef72-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="bef72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bef72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bef72-105">メッセージストアの特性を判断するためにクライアントアプリケーションが照会する必要があるフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="bef72-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bef72-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bef72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bef72-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="bef72-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="bef72-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bef72-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bef72-109">0x340f</span><span class="sxs-lookup"><span data-stu-id="bef72-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="bef72-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bef72-110">Data type:</span></span>  <br/> |<span data-ttu-id="bef72-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bef72-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bef72-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="bef72-112">Area:</span></span>  <br/> |<span data-ttu-id="bef72-113">MAPI メッセージストア</span><span class="sxs-lookup"><span data-stu-id="bef72-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bef72-114">解説</span><span class="sxs-lookup"><span data-stu-id="bef72-114">Remarks</span></span>

<span data-ttu-id="bef72-115">このプロパティによって、メッセージストアの機能が、メッセージを送信することを計画しているクライアントアプリケーションに discloses ます。</span><span class="sxs-lookup"><span data-stu-id="bef72-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="bef72-116">このフラグを使用すると、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のいずれかを送信するかどうかなど、クライアントまたは別のストアによる判断が容易になります。</span><span class="sxs-lookup"><span data-stu-id="bef72-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="bef72-117">クライアントはこのプロパティを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="bef72-117">A client should never set this property.</span></span> <span data-ttu-id="bef72-118">**MAPI_E_COMPUTED**が返されます。</span><span class="sxs-lookup"><span data-stu-id="bef72-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="bef72-119">このプロパティには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="bef72-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="bef72-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="bef72-121">(131072、0x00020000)メッセージストアは、アメリカン National 標準協会 (ANSI) (8 ビット) 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="bef72-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="bef72-123">(32、0x00000020)メッセージストアは、オブジェクトのリンクと埋め込み (ole) または ole 以外の添付ファイルをメッセージに対してサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="bef72-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="bef72-125">(1024、0x00000400)メッセージストアは、テーブルの分類されたビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="bef72-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="bef72-127">(16、0x00000010)メッセージストアは新しいメッセージの作成をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="bef72-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="bef72-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="bef72-129">(1, 0x00000001)メッセージストア内のオブジェクトのエントリ識別子は一意であり、ストアの有効期間中は再利用されません。</span><span class="sxs-lookup"><span data-stu-id="bef72-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="bef72-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="bef72-131">(65536、0x00010000)メッセージストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されている HTML メッセージをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="bef72-132">**STORE_HTML_OK**は、mapidefs.h のバージョンでは定義されていないことに注意してください。H Microsoft Exchange 2000 Server 以前に含まれています。</span><span class="sxs-lookup"><span data-stu-id="bef72-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="bef72-133">開発環境で mapidefs.h を使用している場合。H ファイルに**STORE_HTML_OK**が含まれていない場合は、値「0x00010000」を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="bef72-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="bef72-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="bef72-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="bef72-135">(2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアがメッセージに対してルールおよびスパムフィルター処理を個別に実行することを示します。</span><span class="sxs-lookup"><span data-stu-id="bef72-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="bef72-136">ストアは[imapisupport:: Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される[通知](notification.md)構造で**fnevNewMail**を設定してから、新しいメッセージの詳細をリスニングクライアントに渡します。</span><span class="sxs-lookup"><span data-stu-id="bef72-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="bef72-137">その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="bef72-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="bef72-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="bef72-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="bef72-139">(524288、0x00080000)このフラグは予約されているため、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="bef72-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="bef72-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="bef72-141">(8, 0x00000008)メッセージストアは、既存のメッセージの変更をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="bef72-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="bef72-143">(512、0x00000200)メッセージストアは、複数値プロパティをサポートしており、保存操作中に複数値プロパティの値の順序の安定性を保証し、テーブル内の複数値プロパティのインスタンス化をサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="bef72-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="bef72-145">(256、0x00000100)メッセージストアが通知をサポートしている。</span><span class="sxs-lookup"><span data-stu-id="bef72-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="bef72-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="bef72-147">(64、0x00000040)メッセージストアは OLE 添付ファイルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="bef72-148">OLE データは、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して利用できるような**IStorage**インターフェイスを介してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="bef72-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="bef72-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="bef72-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="bef72-150">(16384、0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) であり、プライベートではありません (複数のインスタンスが複数のユーザーではない可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="bef72-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="bef72-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="bef72-152">(8388608、0x00800000)MAPI プロトコルハンドラーはストアをクロールしません。ストアは、メッセージをインデックス処理するために、インデクサーに対する通知による変更をすべて転送する責任があります。</span><span class="sxs-lookup"><span data-stu-id="bef72-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="bef72-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="bef72-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="bef72-154">(2, 0x00000002)メッセージストアのすべてのインターフェイスには、読み取り専用のアクセスレベルがあります。</span><span class="sxs-lookup"><span data-stu-id="bef72-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="bef72-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="bef72-156">(4096、0x00001000)メッセージストアは制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="bef72-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="bef72-158">(2048、0x00000800)メッセージストアは、リッチテキスト形式 (RTF) メッセージ (通常は圧縮済み) をサポートしており、ストア自体は**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="bef72-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="bef72-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="bef72-160">(4、0x00000004)メッセージストアは、検索結果フォルダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="bef72-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="bef72-162">(8192、0x00002000)メッセージストアは、テーブルの並べ替えビューをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="bef72-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="bef72-164">(128、0x00000080)メッセージストアは、送信用のメッセージのマーキングをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="bef72-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="bef72-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="bef72-166">(32768、0x00008000)メッセージストアは、圧縮されていない形式での revisable フォームテキスト (RTF) メッセージの格納をサポートします。</span><span class="sxs-lookup"><span data-stu-id="bef72-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="bef72-167">圧縮されていない RTF ストリームは、stream ヘッダーの値**dwMagicUncompressedRTF**によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="bef72-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="bef72-168">**dwMagicUncompressedRTF**の値は、rtflib で定義されています。H ファイル</span><span class="sxs-lookup"><span data-stu-id="bef72-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="bef72-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="bef72-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="bef72-170">(262144, 0x00040000)メッセージストアは、Unicode 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bef72-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="bef72-171">メッセージストアが rtf に対応していない場合でも、メッセージの rtf バージョンを保存できます。</span><span class="sxs-lookup"><span data-stu-id="bef72-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="bef72-172">特定のストアに対して STORE_RTF_OK ビットが設定されていない場合、RTF バージョンを保持しているクライアントは、 **PR_BODY**と**PR_RTF_COMPRESSED**のバージョンとテキストコンテンツの同期を維持するために、 [rtfsync](rtfsync.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="bef72-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="bef72-173">RTF は、実際に圧縮されているかどうかにかかわらず、常に**PR_RTF_COMPRESSED**に保存されます。</span><span class="sxs-lookup"><span data-stu-id="bef72-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bef72-174">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bef72-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bef72-175">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bef72-175">Header files</span></span>

<span data-ttu-id="bef72-176">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bef72-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="bef72-177">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bef72-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="bef72-178">Mapitags</span><span class="sxs-lookup"><span data-stu-id="bef72-178">Mapitags.h</span></span>
  
> <span data-ttu-id="bef72-179">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bef72-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bef72-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="bef72-180">See also</span></span>



[<span data-ttu-id="bef72-181">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bef72-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bef72-182">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bef72-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bef72-183">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bef72-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bef72-184">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bef72-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

