---
title: TNEF-Taggedメッセージ テキスト
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
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="3a214-103">TNEF-Taggedメッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="3a214-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="3a214-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a214-105">タグ付きメッセージ テキストは、親メッセージ内の添付ファイルの位置を解決するために TNEF によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="3a214-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="3a214-106">これは、添付ファイルの位置にメッセージ テキストに場所の所有者を追加することで行われます。</span><span class="sxs-lookup"><span data-stu-id="3a214-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="3a214-107">この場所の所有者 (添付ファイル タグ) は、TNEF が添付ファイルとその位置を解決する方法を知っている方法で添付ファイルを記述します。</span><span class="sxs-lookup"><span data-stu-id="3a214-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="3a214-108">タグの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3a214-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="3a214-109">**\< オブジェクトの \> タイトル\*\*\*\*\< とファイル \> 名** は、添付ファイル自体から取得される値を含む変数です。</span><span class="sxs-lookup"><span data-stu-id="3a214-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="3a214-110">これらの値を使用できない場合、タイトルの既定値は添付ファイルの種類に基づいて TNEF です。</span><span class="sxs-lookup"><span data-stu-id="3a214-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="3a214-111">**\< KeyNum \> 変数** には、TNEF によって添付ファイルに割り当てられた添付ファイル キーのテキスト表現が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3a214-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="3a214-112">キーの基本値は [、OpenTnefStreamEx 呼び出しに渡](opentnefstreamex.md) されます。</span><span class="sxs-lookup"><span data-stu-id="3a214-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="3a214-113">基本値を 0 にし **、OpenTnefStreamEx** の呼び出しごとに同じ値にしない必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a214-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="3a214-114">実行時ライブラリが提供する任意の乱数ジェネレーターからのシステム時間に基づいて擬似乱数を使用すれば十分です。これらの乱数がゼロではないと保証されている限りです。</span><span class="sxs-lookup"><span data-stu-id="3a214-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="3a214-115">トランスポート **\< 名変数 \> には**[、OpenTnefStreamEx](opentnefstreamex.md)呼び出しに渡されるストリーム名、または **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3a214-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a214-116">メッセージ **PR_ATTACH_TRANSPORT_NAME** タグの PR_ATTACH_TRANSPORT_NAME プロパティと Transport **\< Name \>** 変数は、実装するトランスポート プロバイダーの名前とは関係しません。</span><span class="sxs-lookup"><span data-stu-id="3a214-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="3a214-117">これらのアイテムは、トランスポート プロバイダーとメッセージング システムの添付ファイルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="3a214-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="3a214-118">メッセージ テキストは、トランスポート プロバイダーが [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) メソッドを呼び出してタグ付けされたメッセージ テキストを求めるときにタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="3a214-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="3a214-119">タグ付きテキスト ストリームから読み取る場合 **、TNEF は、PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで指定されたインデックスにあるメッセージ テキスト内の 1 文字を適切なタグに置き換える。</span><span class="sxs-lookup"><span data-stu-id="3a214-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="3a214-120">タグ付きテキスト ストリームに書き込む場合、TNEF はタグの受信データをチェックし、関連付けられた添付ファイルを検索し、タグを 1 つのスペース文字に置き換える。</span><span class="sxs-lookup"><span data-stu-id="3a214-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="3a214-121">タグ付きメッセージ テキストを使用すると、メッセージング システムによってメッセージ テキストに加えたほとんどの変更に関係なく、トランスポート プロバイダーは添付ファイルの位置を保持できます。</span><span class="sxs-lookup"><span data-stu-id="3a214-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

