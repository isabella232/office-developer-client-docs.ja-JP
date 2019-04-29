---
title: 書式設定されたテキストゲートウェイの役割をサポートする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419430"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="01f1c-103">書式付きテキストのサポート: ゲートウェイの責任</span><span class="sxs-lookup"><span data-stu-id="01f1c-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="01f1c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="01f1c-105">**送信メッセージのリッチテキスト形式を処理するには、ゲートウェイ**</span><span class="sxs-lookup"><span data-stu-id="01f1c-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="01f1c-106">メッセージストアからメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのみを取得します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="01f1c-107">**PR_RTF_COMPRESSED**プロパティのみを取得する場合の主な利点は、ゲートウェイとメッセージストアが異なるコンピューター上に存在する場合に、メッセージテキストをコンピューター間で送信する必要がないことです。</span><span class="sxs-lookup"><span data-stu-id="01f1c-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="01f1c-108">RTF ライブラリ関数**hrtextfromcompressedrtfstream**を呼び出すか、メッセージがローカルに格納されている場合は**rtfsync**を呼び出して、書式設定されたテキストからメッセージテキストを生成します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="01f1c-109">RTF_SYNC_RTF_CHANGED フラグは、 **rtfsync**への呼び出しで設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01f1c-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="01f1c-110">詳細については、「 [rtfsync](rtfsync.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01f1c-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="01f1c-111">サポートされていない文字を削除するなど、メッセージテキストを変更せずに取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="01f1c-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="01f1c-112">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) と RTF auxilliary のすべてのプロパティが設定されているか、存在しないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="01f1c-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="01f1c-113">変更が行われた場合は、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグが設定された**rtfsync**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="01f1c-114">**rtfsync**は、変更されたテキストから RTF auxilliary プロパティを再計算します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="01f1c-115">添付ファイルのプレースホルダーの挿入や非破壊コードページ変換の実行など、メッセージテキストに対して reversable の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="01f1c-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="01f1c-116">メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-116">Send the message.</span></span>
    
 <span data-ttu-id="01f1c-117">**受信メッセージのリッチテキスト形式を処理するには、ゲートウェイ**</span><span class="sxs-lookup"><span data-stu-id="01f1c-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="01f1c-118">メッセージが送信される前に、テキストによる変更を取り消します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="01f1c-119">メッセージに**PR_RTF_COMPRESSED**プロパティと**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティの両方が含まれている場合は、 **rtfsync**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="01f1c-120">メッセージに含まれている場合は、 **PR_RTF_COMPRESSED**プロパティを使用して、メッセージストア内のメッセージを更新します。**PR_RTF_COMPRESSED**が存在しない場合にのみ、 **PR_BODY**プロパティを使用して update を行います。</span><span class="sxs-lookup"><span data-stu-id="01f1c-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="01f1c-121">メッセージにこのプロパティと**PR_RTF_COMPRESSED**の両方が含まれている場合は、 **PR_BODY**を破棄します。</span><span class="sxs-lookup"><span data-stu-id="01f1c-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="01f1c-122">ゲートウェイは**rtfsync**を呼び出して、メッセージのテキストと書式設定されたテキストの両方を送信しないようにします (メッセージストアが別のコンピューターにある場合)。</span><span class="sxs-lookup"><span data-stu-id="01f1c-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="01f1c-123">ゲートウェイがローカルの場合は、両方のプロパティを設定し、メッセージストアで同期を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="01f1c-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

