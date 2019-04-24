---
title: TNEF カスタム添付ファイル処理を使用したメッセージの送信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339698"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="df557-103">TNEF カスタム添付ファイル処理を使用したメッセージの送信</span><span class="sxs-lookup"><span data-stu-id="df557-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="df557-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df557-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df557-105">メッセージ送信時に添付ファイルの処理をカスタマイズするには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="df557-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="df557-106">**IStream**インターフェイスとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって、TNEF オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="df557-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="df557-107">[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、メッセージに対して定義されているすべてのプロパティの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="df557-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="df557-108">メッセージシステムでサポートされているすべてのプロパティを除外するには、 [imapiprop](imapipropiunknown.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="df557-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="df557-109">適切なタイミングで、メッセージングシステムが必要とする形式でメッセージングシステムにこれらのプロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="df557-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="df557-110">[ITnef:: addprops](itnef-addprops.md)メソッドを呼び出して、TNEF_PROP_MESSAGE_ONLY フラグを設定することによって、添付ファイルのすべてのプロパティではなく、メッセージにプロパティのみを追加します。</span><span class="sxs-lookup"><span data-stu-id="df557-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="df557-111">次の項目を使用して[ITnef:: addprops](itnef-addprops.md)を呼び出します。 TNEF_PROP_EXCLUDE フラグは、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を含むプロパティタグ配列です。プロパティ、および処理する添付ファイルを指定する添付ファイル識別子です。</span><span class="sxs-lookup"><span data-stu-id="df557-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="df557-112">[ITnef:: setprops](itnef-setprops.md)メソッドを使用して、添付ファイルにファイル名が含まれている場合にメッセージングシステムへの添付ファイルを識別する一意の文字列を持つ**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティタグを追加します。メッセージングシステムはサポートできません。</span><span class="sxs-lookup"><span data-stu-id="df557-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="df557-113">たとえば、同じ元のファイル名を持つ複数の添付ファイル、またはメッセージングシステムの有効なファイル名ではないファイル名。</span><span class="sxs-lookup"><span data-stu-id="df557-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="df557-114">この文字列は、タグ付きメッセージテキストに添付ファイルタグを書き込み、添付ファイルをそのデータに関連付けるときに、キー番号と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="df557-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="df557-115">詳細については、「 [TNEF のタグ付きメッセージテキスト](tnef-tagged-message-text.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df557-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="df557-116">添付ファイルごとに**addprops**と**setprops**呼び出しを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="df557-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="df557-117">要求されたすべてのプロパティが追加された後に、メッセージを TNEF ストリームにエンコードするには、 [ITnef:: Finish](itnef-finish.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df557-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="df557-118">タグ付きメッセージテキストを取得するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="df557-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="df557-119">このタグ付きテキストは、メッセージシステムの添付モデルを使用してエンコードされた**IStream**インターフェイスからのメソッドを使用して読み取られ、メッセージングシステムに書き出されます。</span><span class="sxs-lookup"><span data-stu-id="df557-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="df557-120">[IUnknown:: release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、 [ITnef](itnefiunknown.md)オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="df557-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="df557-121">メッセージングシステムの添付モデルを使用して、残りの添付ファイルをメッセージングシステムに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="df557-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="df557-122">トランスポートプロバイダーは、前述の手順を使用して添付ファイルを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df557-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="df557-123">これができない場合、トランスポートプロバイダーは、カスタマイズされた添付ファイル処理のために次の手順を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df557-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="df557-124">トランスポートプロバイダーによって、すべての添付ファイルの**PR_ATTACH_TRANSPORT_NAME**プロパティに、メッセージングシステムの有効な添付ファイル識別子である一意の値が含まれていることが確認されます。</span><span class="sxs-lookup"><span data-stu-id="df557-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="df557-125">トランスポートプロバイダーは、各添付ファイルに対して**ITnef:: addprops**に対して単一の呼び出しを使用し、TNEF_PROP_CONTAINED フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="df557-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

