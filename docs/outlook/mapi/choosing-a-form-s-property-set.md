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
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="055b2-103">フォームのプロパティ セットの選択</span><span class="sxs-lookup"><span data-stu-id="055b2-103">Choosing a form's property set</span></span>

<span data-ttu-id="055b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="055b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="055b2-105">フォームサーバーを実装するときは、メッセージクラスに必要な情報の各要素にプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="055b2-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="055b2-106">これらのプロパティは、定義済みの MAPI プロパティにすることも、定義するカスタムプロパティにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="055b2-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="055b2-107">プロパティの使用の詳細については、「 [MAPI プロパティの概要](mapi-property-overview.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="055b2-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="055b2-108">フォーム構成ファイルには、フォームサーバーがクライアントアプリケーションで公開するプロパティのリストが含まれていますが、これはフォームサーバーで使用されるプロパティのリスト全体である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="055b2-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="055b2-109">通常、クライアントアプリケーションは公開されているプロパティを使用して、ユーザーがフォルダー内のメッセージを並べ替えたり、何らかの方法でインターフェイスをカスタマイズしたりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="055b2-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="055b2-110">MAPI には、ほとんどのアプリケーションに十分な、定義済みのプロパティセットが多数あります。</span><span class="sxs-lookup"><span data-stu-id="055b2-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="055b2-111">ただし、カスタムメッセージクラスに MAPI で定義されていないプロパティが必要になる場合もあります。</span><span class="sxs-lookup"><span data-stu-id="055b2-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="055b2-112">カスタムプロパティを使用して、フォームサーバーがサポートする必要のある特別な情報について、MAPI で事前定義されたプロパティのセットを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="055b2-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="055b2-113">カスタムプロパティを定義するには、次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="055b2-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="055b2-114">プロパティの名前を選択し、 [imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを使用して、プロパティタグを取得します。</span><span class="sxs-lookup"><span data-stu-id="055b2-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="055b2-115">このメソッドを呼び出す[imapiprop](imapipropiunknown.md)インターフェイスは、メッセージが作成されたときにフォームサーバーに渡される[IMessage](imessageimapiprop.md)ポインターから取得します。</span><span class="sxs-lookup"><span data-stu-id="055b2-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="055b2-116">プロパティ名はワイド文字文字列である必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="055b2-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="055b2-117">カスタムプロパティタグを自分で定義します。</span><span class="sxs-lookup"><span data-stu-id="055b2-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="055b2-118">カスタムプロパティタグは、範囲0x6800 から0x7bff にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="055b2-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="055b2-119">この範囲のプロパティは、メッセージクラスに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="055b2-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="055b2-120">カスタムプロパティの定義の詳細については、「[新しい MAPI プロパティの定義](defining-new-mapi-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="055b2-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="055b2-121">メッセージテキストを持つフォームサーバーは、通常、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを使用して格納します。</span><span class="sxs-lookup"><span data-stu-id="055b2-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="055b2-122">フォームサーバーで**PR_RTF_COMPRESSED**を使用する場合は、リッチテキストをサポートしていないクライアントによってメッセージが読み取られた場合に備えて、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティにメッセージテキストのテキストのみのバージョンが含まれていることを確認する必要があります。Format (RTF) メッセージテキスト。</span><span class="sxs-lookup"><span data-stu-id="055b2-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="055b2-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="055b2-123">See also</span></span>

- [<span data-ttu-id="055b2-124">MAPI フォームサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="055b2-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

