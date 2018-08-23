---
title: ゲートウェイの役割を書式設定されたテキストをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804040"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="8d853-103">書式付きテキストのサポート: ゲートウェイの責任</span><span class="sxs-lookup"><span data-stu-id="8d853-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="8d853-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d853-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="8d853-105">**ゲートウェイ、送信メッセージのリッチ テキスト形式を処理するために**</span><span class="sxs-lookup"><span data-stu-id="8d853-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="8d853-106">メッセージ ストアからメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティだけを取得します。</span><span class="sxs-lookup"><span data-stu-id="8d853-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="8d853-107">**PR_RTF_COMPRESSED**プロパティのみを取得する主な利点は、メッセージのテキストは、ゲートウェイ、メッセージ ・ ストアが別のマシンに存在する場合、コンピューター間で送信するのには必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8d853-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="8d853-108">Rtf 形式のライブラリ関数**HrTextFromCompressedRTFStream**を呼び出すことによっていずれかの書式付きの文字列からのメッセージのテキストを生成または、メッセージがローカルに格納されている**行う**。</span><span class="sxs-lookup"><span data-stu-id="8d853-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="8d853-109">呼び出しを**行う**には、RTF_SYNC_RTF_CHANGED フラグを設定してください。</span><span class="sxs-lookup"><span data-stu-id="8d853-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="8d853-110">詳細については、[行う](rtfsync.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d853-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="8d853-111">サポートされていない文字の削除など、メッセージのテキストを元に戻せない変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="8d853-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="8d853-112">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) とすべての rtf 形式の補助プロパティの両方は、いずれかのセットに存在しないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d853-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="8d853-113">変更が行われた場合、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグのセットを使用して**行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d853-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="8d853-114">**** 変更されたテキストから rtf 形式の補助プロパティを再計算されます。</span><span class="sxs-lookup"><span data-stu-id="8d853-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="8d853-115">Reversable の添付ファイルのプレース ホルダーを挿入して、非破壊的なコード ページ変換を実行するなど、メッセージのテキストに変更を加える場合です。</span><span class="sxs-lookup"><span data-stu-id="8d853-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="8d853-116">メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="8d853-116">Send the message.</span></span>
    
 <span data-ttu-id="8d853-117">**ゲートウェイの受信メッセージのリッチ テキスト形式を処理するために**</span><span class="sxs-lookup"><span data-stu-id="8d853-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="8d853-118">メッセージが送信される前に直接加えられたメッセージ テキスト変更をすべて元に戻します。</span><span class="sxs-lookup"><span data-stu-id="8d853-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="8d853-119">メッセージに、 **PR_RTF_COMPRESSED**と ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティの両方が含まれている場合に**行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d853-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="8d853-120">メッセージが含まれている場合に、 **PR_RTF_COMPRESSED**プロパティを使用してメッセージ ・ ストア内のメッセージを更新します。**PR_RTF_COMPRESSED**が存在しない場合にのみ、 **PR_BODY**プロパティを使用して更新します。</span><span class="sxs-lookup"><span data-stu-id="8d853-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="8d853-121">**PR_BODY**を破棄して、メッセージには、このプロパティと**PR_RTF_COMPRESSED**の両方が含まれている場合。</span><span class="sxs-lookup"><span data-stu-id="8d853-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="8d853-122">ゲートウェイは、メッセージ ・ ストアが別のマシン上にある場合、メッセージのテキストと書式設定されたテキストの両方の送信を避けるために**行う**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8d853-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="8d853-123">ゲートウェイがローカルの場合は、両方のプロパティを設定し、同期を実行するメッセージ ・ ストアをできるようにすることできます。</span><span class="sxs-lookup"><span data-stu-id="8d853-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

