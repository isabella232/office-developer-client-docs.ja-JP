---
title: TNEF ユーザー設定添付ファイル処理を使用したメッセージの送信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 0c7cdf754b2a4b38516b1ac06074fdba9d2227f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577745"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="9b4e3-103">TNEF ユーザー設定添付ファイル処理を使用したメッセージの送信</span><span class="sxs-lookup"><span data-stu-id="9b4e3-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="9b4e3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b4e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b4e3-105">メッセージを送信するときは、添付ファイルの処理をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="9b4e3-106">**IStream**インターフェイスとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって TNEF オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="9b4e3-107">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="9b4e3-108">[IMAPIProp](imapipropiunknown.md)メソッドを使用すると、メッセージング システムでサポートされているすべてのプロパティを除外できます。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="9b4e3-109">適切なタイミングでは、メッセージング システムに必要な形式でのメッセージング システムにこれらのプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="9b4e3-110">メッセージのプロパティだけを追加するのには[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出します: 添付ファイルのプロパティの [なし] は、-TNEF_PROP_MESSAGE_ONLY フラグを設定することによって。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="9b4e3-111">これらの項目に[ITnef::AddProps](itnef-addprops.md)を呼び出す: TNEF_PROP_EXCLUDE のフラグ、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を格納するプロパティ タグ配列プロパティ、および添付ファイルを処理する添付ファイルを指定する識別子です。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="9b4e3-112">添付ファイルにファイル名がある場合、メッセージング システムに添付ファイルを識別する一意の文字列を**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティ タグを追加するのには、 [ITnef::SetProps](itnef-setprops.md)メソッドを使用する、メッセージング システムをサポートできません。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="9b4e3-113">たとえば、複数の添付ファイル、同じ元のファイル名、またはメッセージング システムの有効なファイル名ではないファイル名にします。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="9b4e3-114">この文字列で使用するキーの番号タグ付けされたメッセージの添付ファイルのタグを記述するときに添付ファイルをデータに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="9b4e3-115">詳細については、 [TNEF-Tagged メッセージのテキスト](tnef-tagged-message-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="9b4e3-116">**AddProps**と**SetProps**の呼び出しは、添付ファイルごとに繰り返します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="9b4e3-117">要求されたすべてのプロパティを追加した後は、TNEF ストリームにメッセージをエンコードするために[ITnef::Finish](itnef-finish.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="9b4e3-118">[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出すことによって、タグ付けされたメッセージのテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="9b4e3-119">このタグ付きテキストは、メッセージング システムの添付ファイルのモデルを使用してエンコードして、メッセージング システムに書き込まれます、 **IStream**インターフェイスからメソッドを使用して読み取られます。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="9b4e3-120">[ITnef](itnefiunknown.md)オブジェクトを解放する[が](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-120">Call the [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="9b4e3-121">メッセージング システムの添付ファイルのモデルを使用してメッセージング システムに残りの添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="9b4e3-122">トランスポート プロバイダーは、プロセスの添付ファイルを上記で説明した手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="9b4e3-123">不可能な場合は、トランスポート プロバイダーは、必要があるカスタマイズされた添付ファイルの処理の次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="9b4e3-124">トランスポート プロバイダーは、メッセージング システムの有効な添付ファイルの識別子は、一意の値がすべての添付ファイルの**PR_ATTACH_TRANSPORT_NAME**プロパティに含まれているようにします。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="9b4e3-125">トランスポート プロバイダーは、添付ファイルごとに、TNEF_PROP_CONTAINED フラグを渡すこと、 **ITnef::AddProps**を 1 回の呼び出しを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b4e3-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

