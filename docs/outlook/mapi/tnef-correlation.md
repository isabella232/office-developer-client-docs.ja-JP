---
title: TNEF 相関関係
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804114"
---
# <a name="tnef-correlation"></a><span data-ttu-id="cb285-103">TNEF 相関関係</span><span class="sxs-lookup"><span data-stu-id="cb285-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="cb285-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb285-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb285-105">いくつかのメッセージング システムでは、TNEF ストリームはそのメッセージを実際に属していることを確認するのには受信メッセージに添付する任意のトランスポート ニュートラル カプセル化形式 (TNEF) ストリームの相互関係のチェックを実行します。</span><span class="sxs-lookup"><span data-stu-id="cb285-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="cb285-106">TNEF ストリーム内のいくつかのプロパティに格納されている値のコピーを受信メッセージのヘッダーにいくつかのフィールドの値と一致するが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb285-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="cb285-107">おそらく、メッセージごとに、メッセージの ID 番号などの一意の値は通常、これを使用します。</span><span class="sxs-lookup"><span data-stu-id="cb285-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="cb285-108">トランスポートまたは TNEF ストリームを作成するゲートウェイは、メッセージ ヘッダーから適切な値を選択して、TNEF ストリームに送信するメッセージのプロパティをエンコードする前に適切なプロパティにコピーを配置することです。</span><span class="sxs-lookup"><span data-stu-id="cb285-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="cb285-109">ゲートウェイまたはトランスポートするメッセージが表示される TNEF ストリームからプロパティを抽出し、その値が対応する受信メッセージのヘッダー フィールドの値と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cb285-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="cb285-110">値が一致しない場合、ゲートウェイまたはトランスポートを破棄 TNEF ストリームとプロセスのネイティブ メッセージ エンベロープのみ。</span><span class="sxs-lookup"><span data-stu-id="cb285-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="cb285-111">非 MAPI ベースのメール クライアント古いメッセージからを転送またはであっても、関係のないメッセージです。 TNEF ストリームを含むファイルを添付することがありますので、このようなチェックは万全を期してチェックが付いていない場合このようなエラー メッセージのテキストが失われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cb285-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="cb285-112">選択ヘッダー フィールドの値は、メッセージに一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cb285-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="cb285-113">別のメッセージング システムは、さまざまなヘッダー フィールドを使用するため、メッセージング システムのすべての固定ヘッダーのフィールドはありませんが、通常メッセージング システムはこの目的に適しているメッセージに固有 id を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="cb285-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="cb285-114">などの SMTP システムでは通常、メッセージ Id ヘッダーを使用して、X.400 システムは、通常、IM_THIS_IPM 属性を使用中にします。</span><span class="sxs-lookup"><span data-stu-id="cb285-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

