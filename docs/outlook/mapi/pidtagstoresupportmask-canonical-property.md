---
title: PidTagStoreSupportMask 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreSupportMask
api_type:
- COM
ms.assetid: ada5694a-b5b1-471f-be33-906fc052681a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340972"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="cf7fb-103">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf7fb-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="cf7fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf7fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf7fb-105">メッセージストアの特性を判断するためにクライアントアプリケーションが照会するフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf7fb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="cf7fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf7fb-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="cf7fb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cf7fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf7fb-109">0x340d</span><span class="sxs-lookup"><span data-stu-id="cf7fb-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="cf7fb-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="cf7fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf7fb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cf7fb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cf7fb-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="cf7fb-112">Area:</span></span>  <br/> |<span data-ttu-id="cf7fb-113">その他</span><span class="sxs-lookup"><span data-stu-id="cf7fb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf7fb-114">解説</span><span class="sxs-lookup"><span data-stu-id="cf7fb-114">Remarks</span></span>

<span data-ttu-id="cf7fb-115">このプロパティは、メッセージの送信を計画しているクライアントアプリケーションに対して、メッセージストアの機能を discloses ます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="cf7fb-116">このフラグは、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のいずれかを送信するかどうかなど、クライアントまたは別のストアによる決定をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="cf7fb-117">クライアントは**PR_STORE_SUPPORT_MASK**を設定してはなりません。このフラグを設定しようとすると、MAPI_E_COMPUTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="cf7fb-118">**PR_STORE_SUPPORT_MASK**ビットマスクには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="cf7fb-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="cf7fb-120">(131072、0x00020000)メッセージストアは、ANSI (8 ビット) 文字を含むプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="cf7fb-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="cf7fb-122">(32、0x00000020)メッセージストアは、メッセージへの添付ファイル (ole または ole 以外) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="cf7fb-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="cf7fb-124">(1024、0x00000400)メッセージストアは、テーブルの分類されたビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="cf7fb-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="cf7fb-126">(16、0x00000010)メッセージストアは新しいメッセージの作成をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="cf7fb-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="cf7fb-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="cf7fb-128">(1, 0x00000001)メッセージストア内のオブジェクトのエントリ識別子は一意であり、ストアの有効期間中は再利用されません。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="cf7fb-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="cf7fb-130">(65536、0x00010000)メッセージストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されている HTML メッセージをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="cf7fb-131">開発環境で mapidefs.h を使用している場合。H ファイルに STORE_HTML_OK が含まれていない場合は、値0x00010000 を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="cf7fb-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="cf7fb-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="cf7fb-133">(2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアはメッセージに対してルールおよびスパムフィルター処理を個別に実行することを示します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="cf7fb-134">ストアは[imapisupport:: Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される[通知](notification.md)構造で**fnevNewMail**を設定してから、新しいメッセージの詳細をリスニングクライアントに渡します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="cf7fb-135">その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="cf7fb-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="cf7fb-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="cf7fb-137">(524288、0x00080000)このフラグは予約されているため、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="cf7fb-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="cf7fb-139">(8, 0x00000008)メッセージストアは、既存のメッセージの変更をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="cf7fb-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="cf7fb-141">(512、0x00000200)メッセージストアは、複数値プロパティをサポートしており、保存操作中に複数値プロパティの値の順序の安定性を保証し、テーブル内の複数値プロパティのインスタンス化をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="cf7fb-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="cf7fb-143">(256、0x00000100)メッセージストアが通知をサポートしている。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="cf7fb-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="cf7fb-145">(64、0x00000040)メッセージストアは OLE 添付ファイルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="cf7fb-146">OLE データには、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して利用できるような**IStorage**インターフェイスを介してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="cf7fb-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="cf7fb-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="cf7fb-148">(16384、0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) であり、プライベートではありません (複数のインスタンスが複数のユーザーではない可能性があります)。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="cf7fb-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="cf7fb-150">(8388608、0x00800000)MAPI プロトコルハンドラーはストアをクロールしません。ストアは、メッセージをインデックス処理するために、インデクサーに対する通知による変更をすべて受信することを担当します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="cf7fb-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="cf7fb-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="cf7fb-152">(2, 0x00000002)メッセージストアのすべてのインターフェイスには、読み取り専用のアクセスレベルがあります。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="cf7fb-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="cf7fb-154">(4096、0x00001000)メッセージストアは制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="cf7fb-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="cf7fb-156">(2048、0x00000800)メッセージストアは、リッチテキスト形式 (RTF) メッセージ (通常は圧縮済み) をサポートしており、ストア自体は**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="cf7fb-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="cf7fb-158">(268435456、0x10000000)既定のストアではない場合でも、ルールがこの PST ストアに保存されることを示します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="cf7fb-159">**STORE_RULES_OK**が**NON_EMS_XP_SAVE**と組み合わせて使用されている場合、ルールは既定以外の PST ラップストアに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="cf7fb-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="cf7fb-161">(4、0x00000004)メッセージストアは、検索結果フォルダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="cf7fb-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="cf7fb-163">(8192、0x00002000)メッセージストアは、テーブルの並べ替えビューをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="cf7fb-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="cf7fb-165">(128、0x00000080)メッセージストアは、送信用のメッセージのマーキングをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="cf7fb-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="cf7fb-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="cf7fb-167">(32768、0x00008000)メッセージストアは、RTF メッセージの保存を未圧縮形式でサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="cf7fb-168">圧縮されていない RTF ストリームは、stream ヘッダーの値**dwMagicUncompressedRTF**によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="cf7fb-169">**dwMagicUncompressedRTF**の値は、rtflib で定義されています。H ファイル</span><span class="sxs-lookup"><span data-stu-id="cf7fb-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="cf7fb-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="cf7fb-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="cf7fb-171">(262144, 0x00040000)メッセージストアが Unicode ストレージをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="cf7fb-172">クライアントは、フラグの有無を調べて、Unicode の情報を要求するかストアに保存するかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="cf7fb-173">メッセージストアが rtf に対応していない場合でも、メッセージの rtf バージョンを保存できます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="cf7fb-174">特定のストアに対して STORE_RTF_OK ビットが設定されていない場合、RTF バージョンを保持しているクライアントは、 **PR_BODY**と**PR_RTF_COMPRESSED**のバージョンとテキストコンテンツの同期を維持するために、 [rtfsync](rtfsync.md)関数を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="cf7fb-175">RTF は、実際に圧縮されているかどうかにかかわらず、常に**PR_RTF_COMPRESSED**に保存されます。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cf7fb-176">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cf7fb-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf7fb-177">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cf7fb-177">Protocol specifications</span></span>

<span data-ttu-id="cf7fb-178">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf7fb-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf7fb-179">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf7fb-180">[[OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf7fb-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf7fb-181">クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf7fb-182">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="cf7fb-182">Header files</span></span>

<span data-ttu-id="cf7fb-183">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf7fb-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf7fb-184">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf7fb-185">Mapitags</span><span class="sxs-lookup"><span data-stu-id="cf7fb-185">Mapitags.h</span></span>
  
> <span data-ttu-id="cf7fb-186">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf7fb-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf7fb-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf7fb-187">See also</span></span>



[<span data-ttu-id="cf7fb-188">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="cf7fb-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf7fb-189">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf7fb-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf7fb-190">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cf7fb-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf7fb-191">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="cf7fb-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

