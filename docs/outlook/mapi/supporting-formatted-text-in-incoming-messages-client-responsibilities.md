---
title: 受信メッセージでの書式付きテキストのサポートクライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327413"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="0b29b-103">受信メッセージでの書式付きテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="0b29b-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="0b29b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b29b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b29b-105">メッセージはメッセージングシステム間で転送されるため、MAPI スプーラーは、リッチテキスト形式がメッセージテキストと同期したままになるようにします。</span><span class="sxs-lookup"><span data-stu-id="0b29b-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="0b29b-106">MAPI スプーラーは、ラップされたバージョンのメッセージ内から、トランスポートプロバイダーに渡される[rtfsync](rtfsync.md) function を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="0b29b-107">トランスポートプロバイダーは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、メッセージに加えられた変更を保存し、新しい受信者にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="0b29b-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="0b29b-108">受信者の RTF 対応クライアントアプリケーションがメッセージを開いてテキストを表示する場合は、テキストを書式設定と同期して、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のどちらかを開く必要があります。使用できるプロパティに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="0b29b-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="0b29b-109">**メッセージ、RTF 対応クライアントを開くには**</span><span class="sxs-lookup"><span data-stu-id="0b29b-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="0b29b-110">メッセージストアが RTF に対応していない場合は、 **rtfsync**を呼び出してメッセージテキストと書式設定を同期します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="0b29b-111">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが存在しない場合、または FALSE に設定されている場合は、 _ulflags_パラメーターで RTF_SYNC_BODY_CHANGED フラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b29b-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="0b29b-112">RTF 対応のメッセージストアを使用しているクライアントは、メッセージストアがそれを処理するため、 **rtfsync**呼び出しを行わないでください。</span><span class="sxs-lookup"><span data-stu-id="0b29b-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="0b29b-113">メッセージテキストが更新された場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="0b29b-114">**PR_RTF_COMPRESSED**プロパティを開くには、 [imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="0b29b-115">**PR_RTF_COMPRESSED**が使用できない場合は、代わりに**PR_BODY**プロパティを開いて、メッセージの内容を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b29b-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="0b29b-116">圧縮された RTF データの圧縮されていないバージョンを作成するには、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="0b29b-117">非圧縮 RTF データまたはプレーンテキストデータをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="0b29b-118">**rtfsync**メッセージが更新されたかどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="0b29b-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="0b29b-119">この値が TRUE を返す場合は、任意の時点で**SaveChanges**を呼び出して更新を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="0b29b-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="0b29b-120">**rtfsync**が返された直後に呼び出しを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0b29b-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0b29b-121">受信する前に、多くのコンポーネントが書式設定されたテキストを処理するため、破損の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b29b-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="0b29b-122">この破損は、メッセージストアプロバイダー、サードパーティアプリケーション、ゲートウェイ、または転送エラーによって発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0b29b-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

