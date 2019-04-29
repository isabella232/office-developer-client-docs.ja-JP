---
title: TNEF タグ付きメッセージテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419920"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="81112-103">TNEF タグ付きメッセージテキスト</span><span class="sxs-lookup"><span data-stu-id="81112-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="81112-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81112-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81112-105">タグ付きメッセージテキストは、親メッセージ内の添付ファイルの位置を解決するために TNEF によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="81112-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="81112-106">これは、添付ファイルの位置に、メッセージテキストにプレースホルダーを追加することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="81112-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="81112-107">このプレースホルダーまたは attachment タグには、添付ファイルとその位置の解決方法が TNEF にわかるような方法で添付ファイルが記述されています。</span><span class="sxs-lookup"><span data-stu-id="81112-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="81112-108">タグの書式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="81112-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="81112-109">オブジェクトのタイトル\*\* \<\> \*\*とファイル名は、添付ファイル自体から取得される値を含む変数です。 \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="81112-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="81112-110">これらの値を使用できない場合、タイトルは添付ファイルの種類に基づいて TNEF によって既定で指定されます。</span><span class="sxs-lookup"><span data-stu-id="81112-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="81112-111">**keynum\>変数には、TNEF によって添付ファイルに割り当てられた添付ファイルキーのテキスト表現が含まれてい\<** ます。</span><span class="sxs-lookup"><span data-stu-id="81112-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="81112-112">キーの基本値が[OpenTnefStreamEx](opentnefstreamex.md)呼び出しに渡されます。</span><span class="sxs-lookup"><span data-stu-id="81112-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="81112-113">**OpenTnefStreamEx**のすべての呼び出しでは、基本値を0にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="81112-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="81112-114">ゼロにしない限り、ランタイムライブラリが提供する乱数ジェネレーターから、システム時間に基づく擬似乱数を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="81112-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="81112-115">\*\* \<トランスポート名\> **の変数には、 [OpenTnefStreamEx](opentnefstreamex.md)呼び出しに渡されたストリーム名、または**PR_ATTACH_TRANSPORT_NAME\*\* ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81112-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="81112-116">メッセージテキストタグの**PR_ATTACH_TRANSPORT_NAME**プロパティと\*\* \<トランスポート名\> \*\*の変数には、実装しているトランスポートプロバイダーの名前とは無関係なものがあります。</span><span class="sxs-lookup"><span data-stu-id="81112-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="81112-117">これらのアイテムは、トランスポートプロバイダーおよびメッセージングシステムの添付ファイルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="81112-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="81112-118">メッセージテキストは、トランスポートプロバイダーが[ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出して、タグ付きメッセージテキストを要求したときにタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="81112-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="81112-119">タグ付きテキストストリームから読み取る場合、TNEF は、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで指定されたインデックスで、メッセージテキストに含まれていた単一の文字を適切なタグに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="81112-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="81112-120">タグ付きテキストストリームに書き込む場合、TNEF は受信データのタグをチェックし、関連付けられた添付ファイルを見つけて、タグを1つのスペース文字に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="81112-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="81112-121">タグ付きメッセージテキストを使用すると、メッセージングシステムによってメッセージテキストに加えられたほとんどの変更に関係なく、トランスポートプロバイダーが添付ファイルの位置を保持することができます。</span><span class="sxs-lookup"><span data-stu-id="81112-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

