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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e15c259003ed2cb425eb181f4383f3054967b993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437939"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="7f2ca-103">PidTagStoreUnicodeMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f2ca-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="7f2ca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f2ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f2ca-105">クライアント アプリケーションがメッセージ ストアの特性を判断するためにクエリを実行する必要があるフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f2ca-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7f2ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f2ca-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="7f2ca-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7f2ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f2ca-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="7f2ca-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="7f2ca-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7f2ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f2ca-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f2ca-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f2ca-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7f2ca-112">Area:</span></span>  <br/> |<span data-ttu-id="7f2ca-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="7f2ca-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f2ca-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7f2ca-114">Remarks</span></span>

<span data-ttu-id="7f2ca-115">このプロパティは、メッセージ ストアの機能を、メッセージの送信を計画しているクライアント アプリケーションに公開します。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="7f2ca-116">このフラグは、PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) を送信するか **、PR_RTF_COMPRESSED** **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のみを送信するかなど、クライアントまたは別のストアによる決定を容易にできます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="7f2ca-117">クライアントは、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-117">A client should never set this property.</span></span> <span data-ttu-id="7f2ca-118">試行によって、MAPI_E_COMPUTED が **返されます**。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="7f2ca-119">このプロパティには、次のフラグを 1 つ以上設定できます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="7f2ca-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="7f2ca-121">(131072、0x00020000)メッセージ ストアは、米国国立標準研究所 (ANSI) (8 ビット) 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="7f2ca-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="7f2ca-123">(32,0x00000020)メッセージ ストアは、メッセージへのオブジェクト リンクと埋め込み (OLE) または OLE 以外の添付ファイルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="7f2ca-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="7f2ca-125">(1024,0x00000400)メッセージ ストアは、テーブルの分類ビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="7f2ca-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="7f2ca-127">(16、0x00000010)メッセージ ストアでは、新しいメッセージの作成がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="7f2ca-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="7f2ca-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="7f2ca-129">(1、0x00000001)メッセージ ストア内のオブジェクトのエントリ識別子は一意です。つまり、ストアの期間中は再利用されません。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="7f2ca-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="7f2ca-131">(65536、0x00010000)メッセージ ストアは HTML メッセージをサポートします。このメッセージは、PR_BODY_HTML **(** [PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="7f2ca-132">MAPIDEFS **STORE_HTML_OK** のバージョンでは定義されていない点に注意してください。Microsoft Exchange 2000 Server 以前に含まれる H。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="7f2ca-133">ご使用の開発環境で MAPIDEFS を使用している場合。このファイルを含STORE_HTML_OK H **ファイルは、** 代わりに "0x00010000" を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="7f2ca-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="7f2ca-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="7f2ca-135">(2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアはメッセージに対してルールとスパム フィルター処理を個別に実行します。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="7f2ca-136">ストアは [IMAPISupport::Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される [NOTIFICATION](notification.md)構造で **fnevNewMail** を設定し、新しいメッセージの詳細をリッスン クライアントに渡します。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="7f2ca-137">その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="7f2ca-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="7f2ca-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="7f2ca-139">(524288、0x00080000)このフラグは予約済みであり、使用できません。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="7f2ca-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="7f2ca-141">(8、0x00000008)メッセージ ストアは、既存のメッセージの変更をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="7f2ca-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="7f2ca-143">(512,0x00000200)メッセージ ストアは、複数値プロパティをサポートし、保存操作を通じて複数値プロパティの値の順序の安定性を保証し、テーブルでの複数値プロパティのインスタンス化をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="7f2ca-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="7f2ca-145">(256,0x00000100)メッセージ ストアは通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="7f2ca-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="7f2ca-147">(64、0x00000040)メッセージ ストアは OLE 添付ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="7f2ca-148">OLE データは **、IStorage** インターフェイスを介してアクセスできます (PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="7f2ca-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="7f2ca-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="7f2ca-150">(16384,0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) で、プライベート (マルチインスタンスの場合は複数インスタンスではなく、マルチユーザー) ではありません。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="7f2ca-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="7f2ca-152">(8388608,0x00800000)MAPI プロトコル ハンドラーはストアをクロールしません。また、メッセージのインデックスを作成するためにインデクサーに通知を通じて変更をプッシュする責任があります。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="7f2ca-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="7f2ca-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="7f2ca-154">(2、0x00000002)メッセージ ストアのすべてのインターフェイスには、読み取り専用アクセス レベルがあります。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="7f2ca-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="7f2ca-156">(4096,0x00001000)メッセージ ストアは制限をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="7f2ca-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="7f2ca-158">(2048,0x00000800)メッセージ ストアは、通常は圧縮されたリッチ テキスト形式 (RTF) メッセージをサポートし、ストア自体が同期 **PR_BODYとPR_RTF_COMPRESSED\*\*\*\*保持します**。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="7f2ca-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="7f2ca-160">(4、0x00000004)メッセージ ストアは、検索結果フォルダーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="7f2ca-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="7f2ca-162">(8192,0x00002000)メッセージ ストアは、テーブルの並べ替えビューをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="7f2ca-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="7f2ca-164">(128,0x00000080)メッセージ ストアは、送信用のメッセージのマーキングをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="7f2ca-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="7f2ca-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="7f2ca-166">(32768,0x00008000)メッセージ ストアでは、変更可能なフォーム テキスト (RTF) メッセージを圧縮されていない形式で保存できます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="7f2ca-167">圧縮されていない RTF ストリームは、ストリーム ヘッダーの **値 dwMagicUncompressedRTF** によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="7f2ca-168">**dwMagicUncompressedRTF** 値は RTFLIB で定義されます。H ファイル。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="7f2ca-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="7f2ca-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="7f2ca-170">(262144、0x00040000)メッセージ ストアは、Unicode 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="7f2ca-171">メッセージ ストアが RTF 対応でない場合でも、RTF バージョンのメッセージを常に保存できます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="7f2ca-172">STORE_RTF_OK ビットが特定のストアに対して設定されていない場合、RTF バージョンを管理するクライアントは、それ自体が [RTFSync](rtfsync.md) 関数を呼び出して **、PR_BODY** バージョンと **PR_RTF_COMPRESSED** バージョンをテキスト コンテンツ用に同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="7f2ca-173">RTF は、実際に **PR_RTF_COMPRESSED** かどうかに関PR_RTF_COMPRESSED常に格納されます。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7f2ca-174">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7f2ca-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f2ca-175">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7f2ca-175">Header files</span></span>

<span data-ttu-id="7f2ca-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f2ca-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f2ca-177">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f2ca-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f2ca-178">Mapitags.h</span></span>
  
> <span data-ttu-id="7f2ca-179">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="7f2ca-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f2ca-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f2ca-180">See also</span></span>



[<span data-ttu-id="7f2ca-181">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7f2ca-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f2ca-182">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f2ca-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f2ca-183">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7f2ca-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f2ca-184">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7f2ca-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

