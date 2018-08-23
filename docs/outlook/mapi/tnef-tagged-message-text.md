---
title: TNEF タグ付きメッセージ テキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1d514dc8b50183e5d07d71b421a441487e933580
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588861"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="fc9ea-103">TNEF タグ付きメッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="fc9ea-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="fc9ea-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc9ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc9ea-105">タグ付きのメッセージのテキストは、親メッセージの添付ファイルの位置を解決するのには TNEF が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="fc9ea-106">これは、は、添付ファイルの位置にあるメッセージのテキストのプレース ホルダーを追加することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="fc9ea-107">このプレース ホルダー、または添付ファイルのタグは、TNEF 添付ファイルとの位置を解決する方法を知っていることのような方法で添付ファイルを説明します。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="fc9ea-108">タグの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="fc9ea-109">**\<オブジェクトのタイトル\>** と**\<ファイル名\>** は、添付ファイル自体から取得される値を含む変数です。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="fc9ea-110">これらの値は利用できませんの場合、タイトルは TNEF の添付ファイルの種類に基づいて、デフォルトとして使用します。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="fc9ea-111">** \<KeyNum\>** 変数には、TNEF 添付ファイルに割り当てられている添付ファイルのキーのテキスト表現が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="fc9ea-112">基本キーの値が渡される[OpenTnefStreamEx](opentnefstreamex.md)の呼び出しにします。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="fc9ea-113">基本値は 0 にできませんする必要があり、 **OpenTnefStreamEx**を呼び出すたびに同じにしないで。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="fc9ea-114">システム時間に基づいて、実行時ライブラリが用意されています、どのようなランダム番号ジェネレーターから 0 であることを保証する限り、擬似乱数を使用することで十分です。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="fc9ea-115">**\<トランスポート名\>** [OpenTnefStreamEx](opentnefstreamex.md)の呼び出しまたは**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティの値に渡されるストリーム名が変数に含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fc9ea-116">**PR_ATTACH_TRANSPORT_NAME**プロパティと**\<トランスポート名\>** を実装するトランスポート プロバイダーの名前とは何もメッセージのテキストのタグ内の変数があります。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="fc9ea-117">これらのアイテムは、トランスポート プロバイダーが、メッセージング システムの添付ファイルの名前を表します。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="fc9ea-118">トランスポート プロバイダーは、 [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出すことによってタグ付けされたメッセージ テキストのメッセージが表示されたら、メッセージのテキストがタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="fc9ea-119">タグ付きテキスト ストリームから読み取る場合、TNEF は、適切なタグを使用して**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティに指定したメッセージ テキストの 1 つの文字を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="fc9ea-120">タグ付きのテキスト ストリームに書き込む場合、TNEF タグの受信データを確認、関連付けられている添付ファイルを検索、タグを 1 つの空白文字に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="fc9ea-121">タグ付けされたメッセージのテキストを使用すると、トランスポート プロバイダーを維持できる、メッセージング システムがメッセージのテキストに加えた変更のほとんどに関係なく、添付ファイルの位置に注意してください。</span><span class="sxs-lookup"><span data-stu-id="fc9ea-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

