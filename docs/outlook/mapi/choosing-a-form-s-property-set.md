---
title: フォームのプロパティ セットの選択
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407194"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="1b4f6-103">フォームのプロパティ セットの選択</span><span class="sxs-lookup"><span data-stu-id="1b4f6-103">Choosing a form's property set</span></span>

<span data-ttu-id="1b4f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b4f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b4f6-105">フォーム サーバーを実装する場合は、メッセージ クラスで必要な情報ごとにプロパティを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="1b4f6-106">これらのプロパティには、定義済みの MAPI プロパティを指定するか、定義するカスタム プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="1b4f6-107">プロパティの操作の詳細については、「MAPI プロパティの概要 [」を参照してください](mapi-property-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="1b4f6-108">フォーム構成ファイルには、クライアント アプリケーションが使用するためにフォーム サーバーが公開するプロパティの一覧が含まれるが、フォーム サーバーで使用されるプロパティのリスト全体である必要はない。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="1b4f6-109">クライアント アプリケーションは通常、公開されたプロパティを使用して、ユーザーがフォルダー内のメッセージを並べ替え、または何らかの方法でインターフェイスをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="1b4f6-110">MAPI には、ほとんどのアプリケーションで十分な定義済みのプロパティの大きなセットがあります。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="1b4f6-111">ただし、MAPI で定義されていないプロパティがカスタム メッセージ クラスに必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="1b4f6-112">カスタム プロパティを使用して、フォーム サーバーがサポートする必要がある特別な情報に対して MAPI 定義済みのプロパティセットを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="1b4f6-113">カスタム プロパティを定義するには、次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="1b4f6-114">プロパティの名前を選択し [、IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを使用してプロパティ タグを取得します。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="1b4f6-115">この [メソッドを呼び出す IMAPIProp](imapipropiunknown.md) インターフェイスは、メッセージの作成時にフォーム サーバーに渡される [IMessage](imessageimapiprop.md) ポインターから取得されます。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="1b4f6-116">プロパティ名はワイド文字の文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="1b4f6-117">カスタム プロパティ タグを自分で定義します。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="1b4f6-118">カスタム プロパティ タグは、カスタム プロパティ タグの0x6800 0x7BFF。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="1b4f6-119">この範囲のプロパティは、メッセージ クラス固有です。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="1b4f6-120">カスタム プロパティの定義の詳細については、「新しい [MAPI プロパティの定義」を参照してください](defining-new-mapi-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b4f6-121">メッセージ テキストを含むフォーム サーバーは、多くの場合、PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを使用して保存します。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="1b4f6-122">フォーム サーバーで **PR_RTF_COMPRESSED** を使用する場合は、リッチ テキスト形式 (RTF) メッセージ テキストをサポートしていないクライアントが結果のメッセージを読み取る場合に備え **、PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティにメッセージ テキストのテキスト専用バージョンが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b4f6-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b4f6-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b4f6-123">See also</span></span>

- [<span data-ttu-id="1b4f6-124">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="1b4f6-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

