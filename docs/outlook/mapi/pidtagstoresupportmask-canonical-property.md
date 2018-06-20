---
title: PidTagStoreSupportMask の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8d9f6311b19ddb489885004a9e507f780d9f1ea9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803597"
---
# <a name="pidtagstoresupportmask-canonical-property"></a><span data-ttu-id="ed608-103">PidTagStoreSupportMask の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="ed608-103">PidTagStoreSupportMask Canonical Property</span></span>

  
  
<span data-ttu-id="ed608-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed608-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed608-105">フラグのビットマスクにはメッセージ ・ ストアの特性を判断するのにはそのクライアント アプリケーションのクエリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed608-105">Contains a bitmask of flags that client applications query to determine the characteristics of a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ed608-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="ed608-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed608-107">PR_STORE_SUPPORT_MASK</span><span class="sxs-lookup"><span data-stu-id="ed608-107">PR_STORE_SUPPORT_MASK</span></span>  <br/> |
|<span data-ttu-id="ed608-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ed608-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed608-109">0x340D</span><span class="sxs-lookup"><span data-stu-id="ed608-109">0x340D</span></span>  <br/> |
|<span data-ttu-id="ed608-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="ed608-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed608-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ed608-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ed608-112">領域:</span><span class="sxs-lookup"><span data-stu-id="ed608-112">Area:</span></span>  <br/> |<span data-ttu-id="ed608-113">その他</span><span class="sxs-lookup"><span data-stu-id="ed608-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed608-114">備考</span><span class="sxs-lookup"><span data-stu-id="ed608-114">Remarks</span></span>

<span data-ttu-id="ed608-115">このプロパティは、メッセージを送信する計画は、クライアント アプリケーションにメッセージ ・ ストアの機能を公開します。</span><span class="sxs-lookup"><span data-stu-id="ed608-115">This property discloses the capabilities of a message store to client applications that are planning to send it a message.</span></span> <span data-ttu-id="ed608-116">フラグは、クライアントまたは別のストア ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY** **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) をのみを送信するかどうかなど、意思決定をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="ed608-116">The flags can support decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="ed608-117">クライアントは**PR_STORE_SUPPORT_MASK**; を設定しない必要があります。このフラグを設定するには、MAPI_E_COMPUTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="ed608-117">A client should never set **PR_STORE_SUPPORT_MASK**; an attempt to set this flag returns MAPI_E_COMPUTED.</span></span> 
  
<span data-ttu-id="ed608-118">**PR_STORE_SUPPORT_MASK**ビットマスクについては、次のフラグの 1 つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ed608-118">One or more of the following flags can be set for the **PR_STORE_SUPPORT_MASK** bitmask:</span></span> 
  
<span data-ttu-id="ed608-119">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-119">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="ed608-120">(131072、0x00020000)メッセージ ・ ストアには、ANSI (8 ビット) 文字が含まれるプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ed608-120">(131072, 0x00020000) The message store supports properties that contain ANSI (8-bit) characters.</span></span>
    
<span data-ttu-id="ed608-121">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-121">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="ed608-122">(32、0x00000020)メッセージ ・ ストアは、メッセージ添付ファイル (または非 OLE OLE) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed608-122">(32, 0x00000020) The message store supports attachments (OLE or non-OLE) to messages.</span></span> 
    
<span data-ttu-id="ed608-123">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-123">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="ed608-124">(1024、0x00000400)メッセージ ・ ストアでは、テーブルの分類されたビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed608-124">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="ed608-125">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-125">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="ed608-126">(16、0x00000010)メッセージ ・ ストアには、新しいメッセージの作成がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ed608-126">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="ed608-127">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="ed608-127">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="ed608-128">(1、0x00000001)エントリ、メッセージ ・ ストア内のオブジェクトの一意な識別子、つまり、ストアの有効期間中に使用されることです。</span><span class="sxs-lookup"><span data-stu-id="ed608-128">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="ed608-129">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-129">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="ed608-130">(65536、0x00010000)メッセージ ・ ストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) のプロパティに格納されている HTML メッセージをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-130">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="ed608-131">場合は、開発環境は、MAPIDEFS を使用します。H ファイルでは、STORE_HTML_OK ではない値 0x00010000 を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="ed608-131">If your development environment uses a MAPIDEFS.H file that does not include STORE_HTML_OK, use the value 0x00010000 instead.</span></span> 
    
<span data-ttu-id="ed608-132">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="ed608-132">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="ed608-133">(2,097, 152、0x00200000)ラップされた PST ストアのストアでは、新しいメッセージが到着すると、ストアを実行する仕訳ルールと迷惑メール フィルターがメッセージを個別に処理を示します。</span><span class="sxs-lookup"><span data-stu-id="ed608-133">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store performs rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="ed608-134">ストアの呼び出し[IMAPISupport::Notify](imapisupport-notify.md)、[通知](notification.md)の構造体をパラメーターとして渡され、リッスンしているクライアントに新しいメッセージの詳細を渡すには、設定**fnevNewMail** 。</span><span class="sxs-lookup"><span data-stu-id="ed608-134">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="ed608-135">その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。</span><span class="sxs-lookup"><span data-stu-id="ed608-135">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="ed608-136">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="ed608-136">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="ed608-137">(524288、0x00080000)このフラグは予約されており、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed608-137">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="ed608-138">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-138">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="ed608-139">(8, 0x00000008)メッセージ ・ ストアには、既存のメッセージの変更がサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-139">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="ed608-140">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-140">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="ed608-141">(512、0x00000200)メッセージ ・ ストアが複数値を持つプロパティをサポートして、セーブセット全体で複数値を持つプロパティの値の順序の安定性を保証する操作、およびテーブル内の複数値を持つプロパティのインスタンス化をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-141">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="ed608-142">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-142">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="ed608-143">(256、0x00000100)メッセージ ・ ストアは、通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-143">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="ed608-144">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-144">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="ed608-145">(64、0x00000040)メッセージ ・ ストアでは、OLE 添付ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-145">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="ed608-146">OLE データにアクセスできますよう、 **IStorage**インターフェイスを使用、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを使用。</span><span class="sxs-lookup"><span data-stu-id="ed608-146">The OLE data can be accessed through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="ed608-147">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="ed608-147">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="ed608-148">(16384、0x00004000)このストア内のフォルダーは、パブリック (マルチ ユーザー)、非プライベート (可能性のある複数のインスタンスですが、マルチ ユーザーではなく)。</span><span class="sxs-lookup"><span data-stu-id="ed608-148">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="ed608-149">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-149">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="ed608-150">(8,388, 608、0x00800000)MAPI プロトコル ハンドラーはストアをクロールしないと、ストアがメッセージをインデックス付けされたインデクサーに通知を使用して、変更をプッシュを行います。</span><span class="sxs-lookup"><span data-stu-id="ed608-150">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible for pushing any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="ed608-151">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="ed608-151">STORE_READONLY</span></span> 
  
> <span data-ttu-id="ed608-152">(2, 0x00000002)メッセージ ストアのすべてのインタ フェースでは、読み取り専用のアクセス レベルがあります。</span><span class="sxs-lookup"><span data-stu-id="ed608-152">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="ed608-153">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-153">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="ed608-154">(4096、0x00001000)メッセージ ・ ストアには、制限がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ed608-154">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="ed608-155">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-155">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="ed608-156">(2048、0x00000800)メッセージ ・ ストアは、リッチ テキスト形式 (RTF) メッセージは、通常は圧縮をサポートしていて、ストア自体が**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="ed608-156">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="ed608-157">STORE_RULES_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-157">STORE_RULES_OK</span></span>
  
> <span data-ttu-id="ed608-158">(268435456、0x10000000)既定のストアではない場合でも、この PST ストアにルールを格納するかを示します。</span><span class="sxs-lookup"><span data-stu-id="ed608-158">(268435456, 0x10000000) Indicates that rules should be stored in this PST store even if it is not the default store.</span></span> <span data-ttu-id="ed608-159">**STORE_RULES_OK**を**NON_EMS_XP_SAVE**と組み合わせて使用する場合、ルールは、既定ではないラップ PST ストア上で実行すること。</span><span class="sxs-lookup"><span data-stu-id="ed608-159">When **STORE_RULES_OK** is used in conjunction with **NON_EMS_XP_SAVE**, rules are able to run on non-default PST wrapped stores.</span></span>
    
<span data-ttu-id="ed608-160">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-160">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="ed608-161">(4、0x00000004)メッセージ ・ ストアには、検索結果フォルダーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-161">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="ed608-162">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-162">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="ed608-163">(8192、0x00002000)メッセージ ・ ストアでは、テーブルのビューが並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed608-163">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="ed608-164">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-164">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="ed608-165">(128, 0x00000080)メッセージ ・ ストアは、メッセージ送信用のマークをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed608-165">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="ed608-166">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="ed608-166">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="ed608-167">(32768、0x00008000)メッセージ ・ ストアでは、圧縮されていないフォームに rtf 形式のメッセージの記憶域をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ed608-167">(32768, 0x00008000) The message store supports storage of RTF messages in uncompressed form.</span></span> <span data-ttu-id="ed608-168">非圧縮の rtf 形式のストリームは、ストリームのヘッダーの値**dwMagicUncompressedRTF**で識別されます。</span><span class="sxs-lookup"><span data-stu-id="ed608-168">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="ed608-169">**DwMagicUncompressedRTF**値は、RTFLIB で定義されています。H ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ed608-169">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="ed608-170">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="ed608-170">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="ed608-171">(262144、0x00040000)メッセージ ・ ストアが Unicode のストレージをサポートしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="ed608-171">(262144, 0x00040000) Indicates that the message store supports Unicode storage.</span></span> <span data-ttu-id="ed608-172">クライアントは Unicode 情報をストアに保存するかを要求するかを決定するフラグの有無を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ed608-172">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span> 
    
<span data-ttu-id="ed608-173">メッセージ ・ ストアが RTF に対応していない場合でも、rtf メッセージを保存常にできます。</span><span class="sxs-lookup"><span data-stu-id="ed608-173">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="ed608-174">STORE_RTF_OK ビットが特定のストアに設定されていない場合は、rtf 形式のバージョンを管理するクライアント自体関数を呼び出す必要[へ](rtfsync.md)テキストの内容を同期して**PR_BODY**と**PR_RTF_COMPRESSED**のバージョンを保持します。</span><span class="sxs-lookup"><span data-stu-id="ed608-174">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="ed608-175">Rtf 形式は、それが実際に圧縮するかどうかどうかに常に**PR_RTF_COMPRESSED**に格納されます。</span><span class="sxs-lookup"><span data-stu-id="ed608-175">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed608-176">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ed608-176">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed608-177">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ed608-177">Protocol specifications</span></span>

<span data-ttu-id="ed608-178">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed608-178">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed608-179">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed608-179">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed608-180">[[MS OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed608-180">[[MS-OXMSG]](http://msdn.microsoft.com/library/b046868c-9fbf-41ae-9ffb-8de2bd4eec82%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed608-181">クライアント上のフォルダーを共有に関連する情報の送信に使用されるメッセージの形式について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed608-181">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed608-182">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ed608-182">Header files</span></span>

<span data-ttu-id="ed608-183">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed608-183">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed608-184">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed608-184">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed608-185">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed608-185">Mapitags.h</span></span>
  
> <span data-ttu-id="ed608-186">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed608-186">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed608-187">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed608-187">See also</span></span>



[<span data-ttu-id="ed608-188">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed608-188">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed608-189">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed608-189">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed608-190">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="ed608-190">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed608-191">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="ed608-191">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

