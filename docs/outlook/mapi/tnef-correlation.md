---
title: TNEF の相関関係
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: '最終更新日: 2013 年 3 月 12 日'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410372"
---
# <a name="tnef-correlation"></a><span data-ttu-id="20f8b-103">TNEF の相関関係</span><span class="sxs-lookup"><span data-stu-id="20f8b-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="20f8b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20f8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20f8b-105">一部のメッセージング システムでは、受信メッセージに接続されている Transport-Neutral カプセル化形式 (TNEF) ストリームに対して相関チェックを実行し、TNEF ストリームが実際にはそのメッセージに属しているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="20f8b-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="20f8b-106">これには、受信メッセージのヘッダーにあるフィールドの値と、TNEF ストリームの一部のプロパティに格納されているその値のコピーを照合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f8b-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="20f8b-107">通常、メッセージ ID 番号など、メッセージごとに一意の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="20f8b-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="20f8b-108">TNEF ストリームを作成したトランスポートまたはゲートウェイは、メッセージ ヘッダーから適切な値を選択し、コピーを適切なプロパティに配置してから、送信メッセージのプロパティを TNEF ストリームにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="20f8b-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="20f8b-109">メッセージを受信するゲートウェイまたはトランスポートは、TNEF ストリームからそのプロパティを抽出し、その値が受信メッセージの対応するヘッダー フィールドの値と一致するを確認できます。</span><span class="sxs-lookup"><span data-stu-id="20f8b-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="20f8b-110">値が一致しない場合、ゲートウェイまたはトランスポートは TNEF ストリームを破棄し、ネイティブ メッセージ エンベロープのみを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f8b-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="20f8b-111">MAPI ベース以外のメール クライアントは、古いメッセージの TNEF ストリームを含むファイルを転送または関連のないメッセージに添付する可能性があるため、このようなチェックは慎重です。チェックされていない場合、このようなエラーによってメッセージ テキストが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="20f8b-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="20f8b-112">選択するヘッダー フィールドの値は、メッセージに対して一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="20f8b-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="20f8b-113">異なるメッセージング システムが異なるヘッダー フィールドを使用しますが、通常、メッセージング システムは、この目的に適したメッセージに一意の識別子を割り当てるので、すべてのメッセージング システムの固定ヘッダー フィールドはありません。</span><span class="sxs-lookup"><span data-stu-id="20f8b-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="20f8b-114">たとえば、SMTP システムは通常、MessageID ヘッダーを使用しますが、X.400 システムは通常、IM_THIS_IPM属性を使用します。</span><span class="sxs-lookup"><span data-stu-id="20f8b-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

