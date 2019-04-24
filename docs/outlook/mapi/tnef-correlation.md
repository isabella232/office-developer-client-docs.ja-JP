---
title: TNEF の関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327399"
---
# <a name="tnef-correlation"></a><span data-ttu-id="fc892-103">TNEF の関連付け</span><span class="sxs-lookup"><span data-stu-id="fc892-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="fc892-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc892-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc892-105">一部のメッセージングシステムでは、受信メッセージに添付されたトランスポート中立カプセル化形式 (TNEF) ストリームに対して相互関係チェックを実行して、そのメッセージに、tnef ストリームが実際に属していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc892-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="fc892-106">これは、受信メッセージのヘッダーの一部のフィールドの値と、TNEF ストリームの一部のプロパティに格納されているその値のコピーを一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc892-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="fc892-107">通常、メッセージ ID 番号など、各メッセージに固有の値は、このために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc892-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="fc892-108">tnef ストリームを作成したトランスポートまたはゲートウェイは、メッセージヘッダーから適切な値を選択し、適切なプロパティにコピーを格納してから、送信メッセージのプロパティを tnef ストリームにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="fc892-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="fc892-109">メッセージを受信するゲートウェイまたはトランスポートは、そのプロパティを TNEF ストリームから抽出し、その値が受信メッセージ上の対応するヘッダーフィールドの値と一致することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="fc892-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="fc892-110">値が一致しない場合、ゲートウェイまたはトランスポートは TNEF ストリームを破棄し、ネイティブメッセージエンベロープのみを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc892-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="fc892-111">このようなチェックは、非 MAPI ベースのメールクライアントが、古いメッセージから転送または関連性のないメッセージに対して TNEF ストリームを含むファイルを添付することがあるために賢明です。チェックされていない場合、このようなエラーによって、メッセージテキストが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc892-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="fc892-112">選択されたヘッダーフィールド値は、メッセージに対して一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc892-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="fc892-113">メッセージングシステムによって異なるヘッダーフィールドが使用されるため、すべてのメッセージングシステムに対して固定ヘッダーフィールドはありませんが、通常、この目的に適したメッセージにはメッセージングシステムが一意の識別子を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="fc892-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="fc892-114">たとえば、通常、SMTP システムは MessageID ヘッダーを使用しますが、IM_THIS_IPM 属性を使用するのは通常、400システムです。</span><span class="sxs-lookup"><span data-stu-id="fc892-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

