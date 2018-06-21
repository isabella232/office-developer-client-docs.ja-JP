---
title: 着信メッセージ クライアントの責任でテキストを書式設定をサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19804046"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a><span data-ttu-id="fd522-103">受信メッセージ内のテキストを書式設定のサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="fd522-103">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="fd522-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd522-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd522-105">メッセージング システム間でメッセージが転送されると、MAPI スプーラーはリッチ テキストの書式設定がメッセージのテキストとの同期であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd522-105">As messages are transferred between messaging systems, the MAPI spooler makes sure that the rich text formatting remains synchronized with the message text.</span></span> <span data-ttu-id="fd522-106">MAPI スプーラーは、トランスポート プロバイダーに渡すメッセージの折り返しが設定されたバージョン内から[行う](rtfsync.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-106">The MAPI spooler calls the [RTFSync](rtfsync.md) function from within a wrapped version of the message that it passes to the transport provider.</span></span> <span data-ttu-id="fd522-107">トランスポート プロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことによってメッセージに加えられた変更内容を保存し、新しい受信者にルーティングします。</span><span class="sxs-lookup"><span data-stu-id="fd522-107">The transport provider saves the changes made to the message by calling the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and then routes it to the new recipient.</span></span> 
  
<span data-ttu-id="fd522-108">書式付きテキストを同期し、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のいずれかを開き、受信者の RTF に対応するクライアント アプリケーションでは、テキストを表示するメッセージが開いたら、必要があります。、プロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd522-108">When the recipient's RTF-aware client application opens the message to display the text, it must synchronize the text with the formatting and open either **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) or **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), depending on which property is available.</span></span>
  
 <span data-ttu-id="fd522-109">**メッセージ、rtf 形式に対応していないクライアントを開く**</span><span class="sxs-lookup"><span data-stu-id="fd522-109">**To open a message, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="fd522-110">メッセージ ・ ストアが RTF に対応していない場合、書式が設定されたメッセージのテキストの同期を**行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-110">Call **RTFSync** to synchronize the message text with the formatting if the message store is not RTF-aware.</span></span> <span data-ttu-id="fd522-111">RTF_SYNC_BODY_CHANGED フラグは、 **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティがないか、FALSE に設定されている場合、 _ulFlags_パラメーターに渡さする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd522-111">The RTF_SYNC_BODY_CHANGED flag should be passed in the  _ulFlags_ parameter if the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or set to FALSE.</span></span> <span data-ttu-id="fd522-112">RTF に対応してメッセージ ・ ストアを使用するクライアントでは、そのメッセージ ・ ストアを管理するため**へ**の呼び出しをする必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="fd522-112">Clients working with RTF-aware message stores need not make the **RTFSync** call because the message store takes care of it.</span></span> 
    
2. <span data-ttu-id="fd522-113">メッセージのテキストが更新されている場合は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-113">Call [IMAPIProp::SaveChanges](imapiprop-savechanges.md) if the message text has been updated.</span></span> 
    
3. <span data-ttu-id="fd522-114">**PR_RTF_COMPRESSED**プロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-114">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="fd522-115">**PR_RTF_COMPRESSED**が利用できない場合は、メッセージの内容を表示する代わりに**PR_BODY**プロパティを開いてください。</span><span class="sxs-lookup"><span data-stu-id="fd522-115">If **PR_RTF_COMPRESSED** is not available, you should open the **PR_BODY** property instead to display the message content.</span></span> 
    
4. <span data-ttu-id="fd522-116">使用可能な場合は、圧縮された rtf 形式のデータの圧縮されていないバージョンを作成する[WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-116">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function to create an uncompressed version of the compressed RTF data, if available.</span></span> 
    
5. <span data-ttu-id="fd522-117">非圧縮の rtf 形式のデータまたはテキスト形式のデータをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="fd522-117">Display the uncompressed RTF data or the plain text data to the user.</span></span>
    
 <span data-ttu-id="fd522-118">**** メッセージが更新されたかどうかを示すブール値を返します。</span><span class="sxs-lookup"><span data-stu-id="fd522-118">**RTFSync** returns a Boolean value that indicates whether or not the message has been updated.</span></span> <span data-ttu-id="fd522-119">この値が TRUE を返した場合は、永続的な更新を行うには、ある時点で**SaveChanges**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fd522-119">If this value returns TRUE, call **SaveChanges** at some point to make the update permanent.</span></span> <span data-ttu-id="fd522-120">**** 返します後すぐに呼び出しがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="fd522-120">The call does not have to be made immediately after **RTFSync** returns.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fd522-121">非常に多くのコンポーネントは、受信する前に書式設定されたテキストを処理するため、破損の可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd522-121">Because so many components handle the formatted text before you receive it, there is the possibility of corruption.</span></span> <span data-ttu-id="fd522-122">この破損は、メッセージ ストア プロバイダー、サードパーティ製アプリケーションが、ゲートウェイ、または転送エラーからものがあります。</span><span class="sxs-lookup"><span data-stu-id="fd522-122">This corruption could come from the message store provider, a third party application, a gateway, or a transmission error.</span></span> 
  

