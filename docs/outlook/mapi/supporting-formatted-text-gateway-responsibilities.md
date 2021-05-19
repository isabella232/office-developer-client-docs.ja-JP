---
title: 書式設定されたテキスト ゲートウェイの責任のサポート
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
# <a name="supporting-formatted-text-gateway-responsibilities"></a><span data-ttu-id="2c566-103">書式設定されたテキストのサポート: ゲートウェイの責任</span><span class="sxs-lookup"><span data-stu-id="2c566-103">Supporting Formatted Text: Gateway Responsibilities</span></span>

  
  
<span data-ttu-id="2c566-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c566-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2c566-105">**送信メッセージ、ゲートウェイのリッチ テキスト形式を処理するには**</span><span class="sxs-lookup"><span data-stu-id="2c566-105">**To handle Rich Text Format for outgoing messages, gateways**</span></span>
  
1. <span data-ttu-id="2c566-106">メッセージ ストアから **メッセージのPR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのみを取得します。</span><span class="sxs-lookup"><span data-stu-id="2c566-106">Retrieve only a message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property from the message store.</span></span> <span data-ttu-id="2c566-107">**PR_RTF_COMPRESSED** プロパティのみを取得する主な利点は、ゲートウェイとメッセージ ストアが異なるコンピューター上に存在する場合に、メッセージ テキストをコンピューター間で送信する必要がなされないという利点です。</span><span class="sxs-lookup"><span data-stu-id="2c566-107">The main advantage in retrieving only the **PR_RTF_COMPRESSED** property is that the message text does not need to be sent between machines if the gateway and the message store exist on different machines.</span></span> 
    
2. <span data-ttu-id="2c566-108">RTF ライブラリ関数 **HrTextFromCompressedRTFStream** を呼び出すことによって、または、メッセージがローカルに保存されている場合は RTFSync を呼び出して、書式設定されたテキストからメッセージ テキスト **を生成します**。</span><span class="sxs-lookup"><span data-stu-id="2c566-108">Generate the message text from the formatted text either by calling the RTF library function **HrTextFromCompressedRTFStream** or, if the message is stored locally, **RTFSync**.</span></span> <span data-ttu-id="2c566-109">RTFSync RTF_SYNC_RTF_CHANGED呼び出しで、このフラグを **設定する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="2c566-109">The RTF_SYNC_RTF_CHANGED flag should be set in the call to **RTFSync**.</span></span> <span data-ttu-id="2c566-110">詳細については [、「RTFSync」を参照してください](rtfsync.md)。</span><span class="sxs-lookup"><span data-stu-id="2c566-110">For more information, see [RTFSync](rtfsync.md).</span></span>
    
3. <span data-ttu-id="2c566-111">サポートされていない文字の削除など、メッセージ テキストに不可逆的な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="2c566-111">Make any irreversible modifications to the message text, such as dropping unsupported characters.</span></span> 
    
4. <span data-ttu-id="2c566-112">すべての RTF **補助PR_RTF_IN_SYNCプロパティ**[(PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)と両方が設定または不在であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2c566-112">Ensure that both **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) and all of the RTF auxilliary properties are either set or absent.</span></span>
    
5. <span data-ttu-id="2c566-113">変更が行われた場合は **、RTFSync** を呼び出し、RTF_SYNC_RTF_CHANGEDフラグRTF_SYNC_BODY_CHANGED設定します。</span><span class="sxs-lookup"><span data-stu-id="2c566-113">If any modifications were made, call **RTFSync** with both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags set.</span></span> <span data-ttu-id="2c566-114">**RTFSync** は、変更されたテキストから RTF 補助プロパティを再計算します。</span><span class="sxs-lookup"><span data-stu-id="2c566-114">**RTFSync** will recalculate the RTF auxilliary properties from the modified text.</span></span> 
    
6. <span data-ttu-id="2c566-115">添付ファイルのプレースホルダーの挿入や非破壊コード ページ変換の実行など、メッセージ テキストに対して不可逆的な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="2c566-115">Make any reversable modifications to the message text, such as inserting attachment placeholders and performing nondestructive code page conversions.</span></span>
    
7. <span data-ttu-id="2c566-116">メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="2c566-116">Send the message.</span></span>
    
 <span data-ttu-id="2c566-117">**受信メッセージ、ゲートウェイのリッチ テキスト形式を処理するには**</span><span class="sxs-lookup"><span data-stu-id="2c566-117">**To handle Rich Text Format for incoming messages, gateways**</span></span>
  
1. <span data-ttu-id="2c566-118">メッセージが送信される前に直接行われたメッセージ テキストの変更を取り消します。</span><span class="sxs-lookup"><span data-stu-id="2c566-118">Reverse any message text modifications that were made directly before the message was sent.</span></span> 
    
2. <span data-ttu-id="2c566-119">メッセージ **に、メッセージ** のプロパティ [(PidTagBody)](pidtagbody-canonical-property.md)プロパティと **PR_RTF_COMPRESSEDプロパティPR_BODY\*\*\*\*が含** まれている場合は、RTFSync を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2c566-119">Call **RTFSync** if the message contains both the **PR_RTF_COMPRESSED** and **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) properties.</span></span> 
    
3. <span data-ttu-id="2c566-120">メッセージに含まれている場合は **、PR_RTF_COMPRESSED プロパティを使用して** メッセージ ストア内のメッセージを更新します。更新は **、PR_BODY** が存在しない場合 **PR_RTF_COMPRESSED** プロパティで更新します。</span><span class="sxs-lookup"><span data-stu-id="2c566-120">Update the message in the message store with the **PR_RTF_COMPRESSED** property if the message contains it; update with the **PR_BODY** property only if **PR_RTF_COMPRESSED** is absent.</span></span> 
    
4. <span data-ttu-id="2c566-121">メッセージ **にPR_BODY** プロパティとプロパティの両方が含まれている場合は、このプロパティ **を破棄** PR_RTF_COMPRESSED。</span><span class="sxs-lookup"><span data-stu-id="2c566-121">Discard **PR_BODY** if the message contains both this property and **PR_RTF_COMPRESSED**.</span></span>
    
<span data-ttu-id="2c566-122">ゲートウェイは **RTFSync を** 呼び出して、メッセージ ストアが別のコンピューター上にある場合、メッセージ テキストと書式設定されたテキストの両方を送信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="2c566-122">Gateways call **RTFSync** to avoid transmitting both the message text and formatted text if the message store is on a different machine.</span></span> <span data-ttu-id="2c566-123">ゲートウェイがローカルの場合は、両方のプロパティを設定し、メッセージ ストアで同期を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2c566-123">If the gateway is local, it can set both properties and allow the message store to perform the synchronization.</span></span> 
  

