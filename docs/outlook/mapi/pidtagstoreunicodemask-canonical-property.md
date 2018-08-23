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
ms.openlocfilehash: 010b17de08ee5836a26c56f300b36822df2e981e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803600"
---
# <a name="pidtagstoreunicodemask-canonical-property"></a><span data-ttu-id="5c8b1-103">PidTagStoreUnicodeMask 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c8b1-103">PidTagStoreUnicodeMask Canonical Property</span></span>

  
  
<span data-ttu-id="5c8b1-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c8b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c8b1-105">クライアント アプリケーションはメッセージ ストアの特性を決定するクエリを実行するためのフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-105">Contains a bitmask of flags that client applications should query to determine the characteristics of a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c8b1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5c8b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c8b1-107">PR_STORE_UNICODE_MASK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-107">PR_STORE_UNICODE_MASK</span></span>  <br/> |
|<span data-ttu-id="5c8b1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5c8b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c8b1-109">0x340F</span><span class="sxs-lookup"><span data-stu-id="5c8b1-109">0x340F</span></span>  <br/> |
|<span data-ttu-id="5c8b1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5c8b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c8b1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5c8b1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5c8b1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5c8b1-112">Area:</span></span>  <br/> |<span data-ttu-id="5c8b1-113">MAPI メッセージ ストア</span><span class="sxs-lookup"><span data-stu-id="5c8b1-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c8b1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5c8b1-114">Remarks</span></span>

<span data-ttu-id="5c8b1-115">このプロパティは、メッセージを送信するクライアント アプリケーションにメッセージ ・ ストアの機能を公開します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-115">This property discloses the capabilities of a message store to client applications planning to send it a message.</span></span> <span data-ttu-id="5c8b1-116">フラグは、クライアントまたは別のストア ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY** **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) をのみを送信するかどうかなど、意思決定を促進できます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-116">The flags can facilitate decisions by a client or another store, such as whether to send **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) or only **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="5c8b1-117">クライアントでは、このプロパティを設定する必要があることはありません。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-117">A client should never set this property.</span></span> <span data-ttu-id="5c8b1-118">しようとするには、 **MAPI_E_COMPUTED**をが返されます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-118">An attempt returns **MAPI_E_COMPUTED**.</span></span> 
  
<span data-ttu-id="5c8b1-119">次のフラグの 1 つ以上は、このプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-119">One or more of the following flags can be set for this property:</span></span> 
  
<span data-ttu-id="5c8b1-120">STORE_ANSI_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-120">STORE_ANSI_OK</span></span>
  
> <span data-ttu-id="5c8b1-121">(131072、0x00020000)メッセージ ・ ストアは、米国規格協会 (ANSI) (8 ビット) 文字を含むプロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-121">(131072, 0x00020000) The message store supports properties that contain American National Standards Institute (ANSI) (8-bit) characters.</span></span>
    
<span data-ttu-id="5c8b1-122">STORE_ATTACH_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-122">STORE_ATTACH_OK</span></span> 
  
> <span data-ttu-id="5c8b1-123">(32、0x00000020)メッセージ ・ ストアには、オブジェクトのリンクし埋め込み (OLE) または非 OLE 添付ファイルをメッセージがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-123">(32, 0x00000020) The message store supports Object Linking and Embedding (OLE) or non-OLE attachments to messages.</span></span> 
    
<span data-ttu-id="5c8b1-124">STORE_CATEGORIZE_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-124">STORE_CATEGORIZE_OK</span></span> 
  
> <span data-ttu-id="5c8b1-125">(1024、0x00000400)メッセージ ・ ストアでは、テーブルの分類されたビューをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-125">(1024, 0x00000400) The message store supports categorized views of tables.</span></span> 
    
<span data-ttu-id="5c8b1-126">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-126">STORE_CREATE_OK</span></span> 
  
> <span data-ttu-id="5c8b1-127">(16、0x00000010)メッセージ ・ ストアには、新しいメッセージの作成がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-127">(16, 0x00000010) The message store supports creation of new messages.</span></span> 
    
<span data-ttu-id="5c8b1-128">STORE_ENTRYID_UNIQUE</span><span class="sxs-lookup"><span data-stu-id="5c8b1-128">STORE_ENTRYID_UNIQUE</span></span> 
  
> <span data-ttu-id="5c8b1-129">(1、0x00000001)エントリ、メッセージ ・ ストア内のオブジェクトの一意な識別子、つまり、ストアの有効期間中に使用されることです。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-129">(1, 0x00000001) Entry identifiers for the objects in the message store are unique, that is, never reused during the life of the store.</span></span> 
    
<span data-ttu-id="5c8b1-130">STORE_HTML_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-130">STORE_HTML_OK</span></span> 
  
> <span data-ttu-id="5c8b1-131">(65536、0x00010000)メッセージ ・ ストアは、 **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) のプロパティに格納されている HTML メッセージをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-131">(65536, 0x00010000) The message store supports HTML messages, stored in the **PR_BODY_HTML** ([PidTagBodyHtml](pidtagbodyhtml-canonical-property.md)) property.</span></span> <span data-ttu-id="5c8b1-132">**STORE_HTML_OK**が MAPIDEFS のバージョンで定義されていないことに注意してください。含まれている Microsoft Exchange 2000 server 以前」をします。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-132">Note that **STORE_HTML_OK** is not defined in versions of MAPIDEFS.H that are included with Microsoft Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="5c8b1-133">場合は、開発環境は、MAPIDEFS を使用します。H ファイルではないには、 **STORE_HTML_OK**、"0x00010000"の値を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-133">If your development environment uses a MAPIDEFS.H file that does not include **STORE_HTML_OK**, use the value "0x00010000" instead.</span></span> 
    
<span data-ttu-id="5c8b1-134">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="5c8b1-134">STORE_ITEMPROC</span></span>
  
> <span data-ttu-id="5c8b1-135">(2,097, 152、0x00200000)ラップされた PST ストア内をストアでは、新しいメッセージが到着すると、ストアは、ルールおよび迷惑メール フィルターとは別に、メッセージの処理を示します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-135">(2097152, 0x00200000) In a wrapped PST store, indicates that when a new message arrives at the store, the store does rules and spam filter processing on the message separately.</span></span> <span data-ttu-id="5c8b1-136">ストアの呼び出し[IMAPISupport::Notify](imapisupport-notify.md)、[通知](notification.md)の構造体をパラメーターとして渡され、リッスンしているクライアントに新しいメッセージの詳細を渡すには、設定**fnevNewMail** 。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-136">The store calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and then passes the details of the new message to the listening client.</span></span> <span data-ttu-id="5c8b1-137">その後、リッスンしているクライアントでは、通知を受信すると、メッセージのルールは処理されません。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-137">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span> 
    
<span data-ttu-id="5c8b1-138">STORE_LOCALSTORE</span><span class="sxs-lookup"><span data-stu-id="5c8b1-138">STORE_LOCALSTORE</span></span>
  
> <span data-ttu-id="5c8b1-139">(524288、0x00080000)このフラグは予約されており、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-139">(524288, 0x00080000) This flag is reserved and should not be used.</span></span>
    
<span data-ttu-id="5c8b1-140">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-140">STORE_MODIFY_OK</span></span> 
  
> <span data-ttu-id="5c8b1-141">(8, 0x00000008)メッセージ ・ ストアには、既存のメッセージの変更がサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-141">(8, 0x00000008) The message store supports modification of its existing messages.</span></span> 
    
<span data-ttu-id="5c8b1-142">STORE_MV_PROPS_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-142">STORE_MV_PROPS_OK</span></span> 
  
> <span data-ttu-id="5c8b1-143">(512、0x00000200)メッセージ ・ ストアが複数値を持つプロパティをサポートして、セーブセット全体で複数値を持つプロパティの値の順序の安定性を保証する操作、およびテーブル内の複数値を持つプロパティのインスタンス化をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-143">(512, 0x00000200) The message store supports multivalued properties, guarantees the stability of value order in a multivalued property throughout a save operation, and supports instantiation of multivalued properties in tables.</span></span> 
    
<span data-ttu-id="5c8b1-144">STORE_NOTIFY_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-144">STORE_NOTIFY_OK</span></span> 
  
> <span data-ttu-id="5c8b1-145">(256、0x00000100)メッセージ ・ ストアは、通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-145">(256, 0x00000100) The message store supports notifications.</span></span> 
    
<span data-ttu-id="5c8b1-146">STORE_OLE_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-146">STORE_OLE_OK</span></span> 
  
> <span data-ttu-id="5c8b1-147">(64、0x00000040)メッセージ ・ ストアでは、OLE 添付ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-147">(64, 0x00000040) The message store supports OLE attachments.</span></span> <span data-ttu-id="5c8b1-148">OLE データは次のように、 **IStorage**インターフェイス経由でアクセスできる**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) は、その使用が可能です。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-148">The OLE data is accessible through an **IStorage** interface, such as that available through the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> 
    
<span data-ttu-id="5c8b1-149">STORE_PUBLIC_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="5c8b1-149">STORE_PUBLIC_FOLDERS</span></span> 
  
> <span data-ttu-id="5c8b1-150">(16384、0x00004000)このストア内のフォルダーは、パブリック (マルチ ユーザー)、非プライベート (可能性のある複数のインスタンスですが、マルチ ユーザーではなく)。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-150">(16384, 0x00004000) The folders in this store are public (multi-user), not private (possibly multi-instance but not multi-user).</span></span> 
    
<span data-ttu-id="5c8b1-151">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-151">STORE_PUSHER_OK</span></span>
  
> <span data-ttu-id="5c8b1-152">(8,388, 608、0x00800000)MAPI プロトコル ハンドラーはストアをクロールしないと、ストアは、メッセージのインデックスを作成するのにはインデクサーに通知を使用して、変更をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-152">(8388608, 0x00800000) The MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>
    
<span data-ttu-id="5c8b1-153">STORE_READONLY</span><span class="sxs-lookup"><span data-stu-id="5c8b1-153">STORE_READONLY</span></span> 
  
> <span data-ttu-id="5c8b1-154">(2, 0x00000002)メッセージ ストアのすべてのインタ フェースでは、読み取り専用のアクセス レベルがあります。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-154">(2, 0x00000002) All interfaces for the message store have a read-only access level.</span></span> 
    
<span data-ttu-id="5c8b1-155">STORE_RESTRICTION_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-155">STORE_RESTRICTION_OK</span></span> 
  
> <span data-ttu-id="5c8b1-156">(4096、0x00001000)メッセージ ・ ストアには、制限がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-156">(4096, 0x00001000) The message store supports restrictions.</span></span> 
    
<span data-ttu-id="5c8b1-157">STORE_RTF_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-157">STORE_RTF_OK</span></span> 
  
> <span data-ttu-id="5c8b1-158">(2048、0x00000800)メッセージ ・ ストアは、リッチ テキスト形式 (RTF) メッセージは、通常は圧縮をサポートしていて、ストア自体が**PR_BODY**と**PR_RTF_COMPRESSED**の同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-158">(2048, 0x00000800) The message store supports Rich Text Format (RTF) messages, usually compressed, and the store itself keeps **PR_BODY** and **PR_RTF_COMPRESSED** synchronized.</span></span> 
    
<span data-ttu-id="5c8b1-159">STORE_SEARCH_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-159">STORE_SEARCH_OK</span></span> 
  
> <span data-ttu-id="5c8b1-160">(4、0x00000004)メッセージ ・ ストアには、検索結果フォルダーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-160">(4, 0x00000004) The message store supports search-results folders.</span></span> 
    
<span data-ttu-id="5c8b1-161">STORE_SORT_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-161">STORE_SORT_OK</span></span> 
  
> <span data-ttu-id="5c8b1-162">(8192、0x00002000)メッセージ ・ ストアでは、テーブルのビューが並べ替えをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-162">(8192, 0x00002000) The message store supports sorting views of tables.</span></span> 
    
<span data-ttu-id="5c8b1-163">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-163">STORE_SUBMIT_OK</span></span> 
  
> <span data-ttu-id="5c8b1-164">(128, 0x00000080)メッセージ ・ ストアは、メッセージ送信用のマークをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-164">(128, 0x00000080) The message store supports marking a message for submission.</span></span> 
    
<span data-ttu-id="5c8b1-165">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="5c8b1-165">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="5c8b1-166">(32768、0x00008000)メッセージ ・ ストアでは、未圧縮の形式でフォームの改訂可能なテキスト (RTF) メッセージの記憶域をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-166">(32768, 0x00008000) The message store supports storage of revisable form text (RTF) messages in uncompressed form.</span></span> <span data-ttu-id="5c8b1-167">非圧縮の rtf 形式のストリームは、ストリームのヘッダーの値**dwMagicUncompressedRTF**で識別されます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-167">An uncompressed RTF stream is identified by the value **dwMagicUncompressedRTF** in the stream header.</span></span> <span data-ttu-id="5c8b1-168">**DwMagicUncompressedRTF**値は、RTFLIB で定義されています。H ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-168">The **dwMagicUncompressedRTF** value is defined in the RTFLIB.H file.</span></span> 
    
<span data-ttu-id="5c8b1-169">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="5c8b1-169">STORE_UNICODE_OK</span></span>
  
> <span data-ttu-id="5c8b1-170">(262144、0x00040000)メッセージ ・ ストアには、Unicode 文字を含むプロパティがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-170">(262144, 0x00040000) The message store supports properties containing Unicode characters.</span></span>
    
<span data-ttu-id="5c8b1-171">メッセージ ・ ストアが RTF に対応していない場合でも、rtf メッセージを保存常にできます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-171">An RTF version of a message can always be stored, even if the message store is non-RTF-aware.</span></span> <span data-ttu-id="5c8b1-172">STORE_RTF_OK ビットが特定のストアに設定されていない場合は、rtf 形式のバージョンを管理するクライアント自体関数を呼び出す必要[へ](rtfsync.md)テキストの内容を同期して**PR_BODY**と**PR_RTF_COMPRESSED**のバージョンを保持します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-172">If the STORE_RTF_OK bit is not set for a particular store, a client maintaining RTF versions must itself call the [RTFSync](rtfsync.md) function to keep the **PR_BODY** and **PR_RTF_COMPRESSED** versions synchronized for text content.</span></span> <span data-ttu-id="5c8b1-173">Rtf 形式は、それが実際に圧縮するかどうかどうかに常に**PR_RTF_COMPRESSED**に格納されます。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-173">RTF is always stored in **PR_RTF_COMPRESSED**, whether it is actually compressed or not.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5c8b1-174">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5c8b1-174">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5c8b1-175">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5c8b1-175">Header files</span></span>

<span data-ttu-id="5c8b1-176">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c8b1-176">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c8b1-177">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-177">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c8b1-178">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c8b1-178">Mapitags.h</span></span>
  
> <span data-ttu-id="5c8b1-179">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c8b1-179">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c8b1-180">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c8b1-180">See also</span></span>



[<span data-ttu-id="5c8b1-181">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c8b1-181">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c8b1-182">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c8b1-182">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c8b1-183">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c8b1-183">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c8b1-184">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c8b1-184">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

