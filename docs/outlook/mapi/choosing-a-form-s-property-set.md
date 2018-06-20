---
title: フォームのプロパティ セットを選択します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 456ef036b26fd8b9840d33f0f699474c3a6ce127
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799796"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="d15e1-103">フォームのプロパティ セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-103">Choosing a form's property set</span></span>

<span data-ttu-id="d15e1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d15e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d15e1-105">フォーム サーバーを実装する場合は、個々 のメッセージ クラスに必要な情報のプロパティを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d15e1-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="d15e1-106">これらのプロパティは、MAPI のプロパティ、定義済みまたはカスタム プロパティを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="d15e1-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="d15e1-107">プロパティの使用についての詳細については、 [MAPI プロパティの概要](mapi-property-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d15e1-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="d15e1-108">フォーム構成ファイルには、クライアント アプリケーションが使用するため、フォームのサーバーを公開するプロパティの一覧が含まれているが、全体、フォームのサーバーで使用されるプロパティの一覧にこれがありません。</span><span class="sxs-lookup"><span data-stu-id="d15e1-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="d15e1-109">通常、クライアント アプリケーションは、フォルダー内のメッセージを並べ替える、または何らかの方法では、そのインターフェイスをカスタマイズするのにユーザーを有効にするのに公開されたプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="d15e1-110">MAPI には、ほとんどのアプリケーションで十分に定義済みのプロパティの大規模なセットがあります。</span><span class="sxs-lookup"><span data-stu-id="d15e1-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="d15e1-111">ただし、カスタム メッセージ クラスが MAPI が定義されていないプロパティをどのようにしなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d15e1-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="d15e1-112">カスタム プロパティを使用するには、フォーム サーバーがサポートするのに必要が特別な情報をすべてのプロパティの定義済みの MAPI のセットを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="d15e1-113">カスタム プロパティを定義するのには次の方法のいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d15e1-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="d15e1-114">プロパティの名前を選択し、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="d15e1-115">[IMAPIProp](imapipropiunknown.md)インターフェイスを使用するには、このメソッドを呼び出してメッセージを作成するときにフォームのサーバーに渡される[IMessage](imessageimapiprop.md)ポインターに由来します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="d15e1-116">プロパティ名は、ワイド文字の文字列である必要があります注意してください。</span><span class="sxs-lookup"><span data-stu-id="d15e1-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="d15e1-117">カスタム プロパティ タグを自分で定義します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="d15e1-118">カスタム プロパティ タグは、0x7BFF から 0x6800 の範囲でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d15e1-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="d15e1-119">メッセージ クラスは、この範囲のプロパティを特定します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="d15e1-120">カスタム プロパティを定義する方法の詳細については、[新しい MAPI プロパティを定義する](defining-new-mapi-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d15e1-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d15e1-121">多くの場合、メッセージ テキストを持つフォームのサーバーでは、そこに格納するのに ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d15e1-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="d15e1-122">フォーム サーバーは、 **PR_RTF_COMPRESSED**を使用する場合にも確認してください ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティにメッセージのテキストのテキストのみのバージョンが含まれている結果のメッセージがリッチ テキストをサポートしていないクライアントによって読み取られた場合にテキスト形 (式 RTF) メッセージのテキストです。</span><span class="sxs-lookup"><span data-stu-id="d15e1-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d15e1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d15e1-123">See also</span></span>

- [<span data-ttu-id="d15e1-124">MAPI フォームのサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="d15e1-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

