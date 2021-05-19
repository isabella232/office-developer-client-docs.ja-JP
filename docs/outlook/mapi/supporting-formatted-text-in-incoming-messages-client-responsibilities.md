---
title: 受信メッセージの書式設定されたテキストのサポート クライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434502"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="e082c-103">受信メッセージの書式設定されたテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="e082c-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="e082c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e082c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e082c-105">メッセージがメッセージング システム間で転送される場合、MAPI スプーラーはリッチ テキストの書式設定がメッセージ テキストと同期されたままになります。</span><span class="sxs-lookup"><span data-stu-id="e082c-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="e082c-106">MAPI スプーラーは、トランスポート プロバイダーに渡すメッセージのラップされたバージョン内から [RTFSync](rtfsync.md) 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e082c-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="e082c-107">トランスポート プロバイダーは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出してメッセージに加えた変更を保存し、新しい受信者にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="e082c-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="e082c-108">受信者の RTF 対応クライアント アプリケーションがメッセージを開いてテキストを表示する場合は、テキストを書式設定と同期し、使用可能なプロパティに応じて **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="e082c-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="e082c-109">**メッセージを開く場合は、RTF 対応のクライアント**</span><span class="sxs-lookup"><span data-stu-id="e082c-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="e082c-110">メッセージ **ストアが RTF** 対応ではない場合は、RTFSync を呼び出して、メッセージ テキストを書式設定と同期します。</span><span class="sxs-lookup"><span data-stu-id="e082c-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="e082c-111">**PR_RTF_IN_SYNC RTF_SYNC_BODY_CHANGED** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが見つからないか、FALSE に設定されている場合は、ulFlags パラメーターにこのフラグを渡す必要があります。 </span><span class="sxs-lookup"><span data-stu-id="e082c-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="e082c-112">RTF 対応のメッセージ ストアを操作するクライアントは、メッセージ ストアが処理を行うので **、RTFSync** 呼び出しを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e082c-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="e082c-113">メッセージ [テキストが更新されている場合は、IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e082c-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="e082c-114">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出して、次のプロパティ **PR_RTF_COMPRESSED** します。</span><span class="sxs-lookup"><span data-stu-id="e082c-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="e082c-115">この **PR_RTF_COMPRESSED** 使用できない場合は、代わりに PR_BODY プロパティを開き **、メッセージ** コンテンツを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e082c-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="e082c-116">[WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出して、圧縮された RTF データの圧縮されていないバージョンを作成します (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="e082c-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="e082c-117">圧縮されていない RTF データまたはプレーン テキスト データをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="e082c-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="e082c-118">**RTFSync** は、メッセージが更新されたかどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="e082c-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="e082c-119">この値が TRUE を返す場合は、ある時点で **SaveChanges** を呼び出して更新プログラムを永続的に設定します。</span><span class="sxs-lookup"><span data-stu-id="e082c-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="e082c-120">RTFSync が返された直後に呼び **出しを行う** 必要はなされません。</span><span class="sxs-lookup"><span data-stu-id="e082c-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e082c-121">多くのコンポーネントで、書式設定されたテキストを受信する前に処理する場合が多いので、破損の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e082c-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="e082c-122">この破損は、メッセージ ストア プロバイダー、サードパーティ アプリケーション、ゲートウェイ、または送信エラーから発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e082c-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

