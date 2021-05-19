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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 143e7f0d2cd89cd4e7956cdda05d1bd512db4027
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340972"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="58cc5-103">PidTagStoreSupportMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58cc5-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="58cc5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58cc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58cc5-105">クライアント アプリケーションがメッセージ ストアの特性を判断するためにクエリを実行するフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="58cc5-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58cc5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="58cc5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58cc5-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="58cc5-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="58cc5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="58cc5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58cc5-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="58cc5-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="58cc5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="58cc5-110">Data type:</span></span>  <br/> |<span data-ttu-id="58cc5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="58cc5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="58cc5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="58cc5-112">Area:</span></span>  <br/> |<span data-ttu-id="58cc5-113">その他</span><span class="sxs-lookup"><span data-stu-id="58cc5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58cc5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="58cc5-114">Remarks</span></span>

<span data-ttu-id="58cc5-115">このプロパティは、メッセージ ストアの機能を、メッセージの送信を計画しているクライアント アプリケーションに公開します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="58cc5-116">このフラグは、PR_BODY **(** [PidTagBody](pidtagbody-canonical-property.md)) を送信するか、PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のみを送信するかなど、クライアントまたは別のストアによる決定をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="58cc5-117">クライアントは、ユーザーを設定 **PR_STORE_SUPPORT_MASK。** このフラグを設定しようとすると、このフラグがMAPI_E_COMPUTED。</span><span class="sxs-lookup"><span data-stu-id="58cc5-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="58cc5-118">次のフラグの 1 つ以上を、ビットマスクにPR_STORE_SUPPORT_MASKできます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="58cc5-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="58cc5-120">(131072、0x00020000)メッセージ ストアは、ANSI (8 ビット) 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="58cc5-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="58cc5-122">(32,0x00000020)メッセージ ストアは、メッセージへの添付ファイル (OLE または OLE 以外) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="58cc5-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="58cc5-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="58cc5-124">(1024,0x00000400)メッセージ ストアは、テーブルの分類ビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="58cc5-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="58cc5-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="58cc5-126">(16、0x00000010)メッセージ ストアでは、新しいメッセージの作成がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="58cc5-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="58cc5-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="58cc5-128">(1、0x00000001)メッセージ ストア内のオブジェクトのエントリ識別子は一意です。つまり、ストアの期間中は再利用されません。</span><span class="sxs-lookup"><span data-stu-id="58cc5-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="58cc5-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="58cc5-130">(65536、0x00010000)メッセージ ストアは HTML メッセージをサポートします。このメッセージは、PR_BODY_HTML **(** [PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="58cc5-131">ご使用の開発環境で MAPIDEFS を使用している場合。ファイルを含めSTORE_HTML_OK H ファイルは、代わりに0x00010000使用します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="58cc5-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="58cc5-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="58cc5-133">(2097152、0x00200000)ラップされた PST ストアで、新しいメッセージがストアに到着すると、ストアはメッセージに対してルールとスパム フィルター処理を個別に実行します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="58cc5-134">ストアは [IMAPISupport::Notify](imapisupport-notify.md)を呼び出し、パラメーターとして渡される [NOTIFICATION](notification.md)構造で **fnevNewMail** を設定し、新しいメッセージの詳細をリッスン クライアントに渡します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="58cc5-135">その後、リッスンしているクライアントが通知を受信すれば、メッセージに対するルールの処理は行われなくなります。</span><span class="sxs-lookup"><span data-stu-id="58cc5-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="58cc5-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="58cc5-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="58cc5-137">(524288、0x00080000)このフラグは予約済みであり、使用できません。</span><span class="sxs-lookup"><span data-stu-id="58cc5-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="58cc5-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="58cc5-139">(8、0x00000008)メッセージ ストアは、既存のメッセージの変更をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="58cc5-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="58cc5-141">(512,0x00000200)メッセージ ストアは、複数値プロパティをサポートし、保存操作を通じて複数値プロパティの値の順序の安定性を保証し、テーブルでの複数値プロパティのインスタンス化をサポートします。</span><span class="sxs-lookup"><span data-stu-id="58cc5-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="58cc5-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="58cc5-143">(256,0x00000100)メッセージ ストアは通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="58cc5-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="58cc5-145">(64、0x00000040)メッセージ ストアは OLE 添付ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="58cc5-146">OLE データにアクセスするには **、IStorage** インターフェイス (PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用して使用できます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="58cc5-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="58cc5-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="58cc5-148">(16384,0x00004000)このストア内のフォルダーはパブリック (マルチユーザー) で、プライベート (マルチインスタンスの場合は複数インスタンスではなく、マルチユーザー) ではありません。</span><span class="sxs-lookup"><span data-stu-id="58cc5-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="58cc5-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="58cc5-150">(8388608,0x00800000)MAPI プロトコル ハンドラーはストアをクロールしません。ストアは、インデクサーへの通知を通じて変更をプッシュしてメッセージのインデックスを作成する責任があります。</span><span class="sxs-lookup"><span data-stu-id="58cc5-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="58cc5-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="58cc5-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="58cc5-152">(2、0x00000002)メッセージ ストアのすべてのインターフェイスには、読み取り専用アクセス レベルがあります。</span><span class="sxs-lookup"><span data-stu-id="58cc5-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="58cc5-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="58cc5-154">(4096,0x00001000)メッセージ ストアは制限をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="58cc5-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="58cc5-156">(2048,0x00000800)メッセージ ストアは、通常は圧縮されたリッチ テキスト形式 (RTF) メッセージをサポートし、ストア自体が同期 **PR_BODYとPR_RTF_COMPRESSED\*\*\*\*保持します**。</span><span class="sxs-lookup"><span data-stu-id="58cc5-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="58cc5-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="58cc5-158">(268435456、0x10000000)ルールが既定のストアではない場合でも、この PST ストアに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58cc5-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="58cc5-159">既定 **STORE_RULES_OK** と組み合わせて使用NON_EMS_XP_SAVE、既定以外の PST ラップ ストアでルールを実行できます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="58cc5-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="58cc5-161">(4、0x00000004)メッセージ ストアは、検索結果フォルダーをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="58cc5-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="58cc5-163">(8192,0x00002000)メッセージ ストアは、テーブルの並べ替えビューをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="58cc5-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="58cc5-165">(128,0x00000080)メッセージ ストアは、送信用のメッセージのマーキングをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="58cc5-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="58cc5-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="58cc5-167">(32768,0x00008000)メッセージ ストアは、圧縮されていない形式の RTF メッセージの保存をサポートします。</span><span class="sxs-lookup"><span data-stu-id="58cc5-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="58cc5-168">圧縮されていない RTF ストリームは、ストリーム ヘッダーの **値 dwMagicUncompressedRTF** によって識別されます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="58cc5-169">**dwMagicUncompressedRTF** 値は RTFLIB で定義されます。H ファイル。</span><span class="sxs-lookup"><span data-stu-id="58cc5-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="58cc5-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="58cc5-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="58cc5-171">(262144、0x00040000)メッセージ ストアが Unicode ストレージをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="58cc5-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="58cc5-172">クライアントは、フラグの有無を調べて、Unicode の情報を要求するかストアに保存するかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="58cc5-173">メッセージ ストアが RTF 対応でない場合でも、RTF バージョンのメッセージを常に保存できます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="58cc5-174">STORE_RTF_OK ビットが特定のストアに対して設定されていない場合、RTF バージョンを管理するクライアントは、それ自体が [RTFSync](rtfsync.md) 関数を呼び出して **、PR_BODY** バージョンと **PR_RTF_COMPRESSED** バージョンをテキスト コンテンツ用に同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58cc5-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="58cc5-175">RTF は、実際に **PR_RTF_COMPRESSED** かどうかに関PR_RTF_COMPRESSED常に格納されます。</span><span class="sxs-lookup"><span data-stu-id="58cc5-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58cc5-176">関連リソース</span><span class="sxs-lookup"><span data-stu-id="58cc5-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58cc5-177">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="58cc5-177">Protocol specifications</span></span>

<span data-ttu-id="58cc5-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58cc5-178">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58cc5-179">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58cc5-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58cc5-180">[[MS-OXMSG]](https://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58cc5-181">クライアント上の共有フォルダーに関連する情報を送信するために使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58cc5-182">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="58cc5-182">Header files</span></span>

<span data-ttu-id="58cc5-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58cc5-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="58cc5-184">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="58cc5-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="58cc5-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58cc5-185">Mapitags.h</span></span>
  
> <span data-ttu-id="58cc5-186">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="58cc5-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58cc5-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="58cc5-187">See also</span></span>



[<span data-ttu-id="58cc5-188">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="58cc5-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58cc5-189">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="58cc5-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58cc5-190">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58cc5-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58cc5-191">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="58cc5-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

