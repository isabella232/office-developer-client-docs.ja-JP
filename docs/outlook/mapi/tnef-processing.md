---
title: TNEF 処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339600"
---
# <a name="tnef-processing"></a><span data-ttu-id="ac370-103">TNEF 処理</span><span class="sxs-lookup"><span data-stu-id="ac370-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="ac370-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac370-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac370-105">次の一連のアクションは、トランスポートが TNEF メソッドを使用して送信および受信メッセージを処理する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ac370-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="ac370-106">**TNEF ストリームを含むメッセージを送信するには**</span><span class="sxs-lookup"><span data-stu-id="ac370-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="ac370-107">メッセージングシステムでサポートされているメッセージのプロパティを処理します。</span><span class="sxs-lookup"><span data-stu-id="ac370-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="ac370-108">メッセージに特定の方法でマークを付けて、受信側トランスポートプロバイダーがメッセージに TNEF 処理を必要とするかどうかを判断できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ac370-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="ac370-109">たとえば、tnef トランスポートプロバイダーが SMTP メッセージングシステムに送信すると、メッセージに tnef データが含まれていることを示すために、"X-CONTAINS-TNEF" などのカスタムヘッダーフィールドが追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="ac370-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="ac370-110">tnef オブジェクトを取得し、それを使用して、メッセージングシステムでサポートされていないメッセージプロパティを tnef ストリームにカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="ac370-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="ac370-111">メッセージングシステムの添付モデルを使用して、TNEF ストリームをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="ac370-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="ac370-112">たとえば、基になる添付ファイルモデルが uuencode の添付ファイルを対象としていて、メッセージテキストに追加されている場合、トランスポートプロバイダーは、別の添付ファイルに TNEF ストリームを uuencode する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac370-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="ac370-113">トランスポートプロバイダーは、メッセージを受信するときに、エンコードされた TNEF ストリームを含む添付ファイルを認識するためのメソッドも実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac370-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="ac370-114">この添付ファイルにマークを付ける標準的な方法は、添付ファイルのファイル名を「winmail.dat」にすることです。DAT "。</span><span class="sxs-lookup"><span data-stu-id="ac370-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="ac370-115">トランスポートプロバイダーがこれを行う場合、この規則に従う他の TNEF 対応のトランスポートプロバイダーは、これと相互運用することができます。</span><span class="sxs-lookup"><span data-stu-id="ac370-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="ac370-116">[ITnef: IUnknown](itnefiunknown.md)インターフェイスメソッドを使用して、メッセージの添付ファイルの位置を示すタグをメッセージテキストに挿入します。</span><span class="sxs-lookup"><span data-stu-id="ac370-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="ac370-117">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)メソッドを使用してタグ付きメッセージテキストにアクセスし、メッセージングシステムに送信します。</span><span class="sxs-lookup"><span data-stu-id="ac370-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="ac370-118">**カプセル化されたプロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="ac370-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="ac370-119">メッセージングシステムによってサポートされるプロパティを新しいメッセージに書き込みます。これには、カプセル化されたプロパティを含むタグ付きメッセージテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac370-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="ac370-120">適切な添付ファイルから TNEF ストリームをデコードします。</span><span class="sxs-lookup"><span data-stu-id="ac370-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="ac370-121">他の添付ファイルをデコードし、メッセージの新しい MAPI 添付ファイルに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="ac370-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="ac370-122">[OpenTnefStreamEx](opentnefstreamex.md)関数を使用してデコードするために TNEF ストリームを開きます。</span><span class="sxs-lookup"><span data-stu-id="ac370-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="ac370-123">TNEF ストリームをデコードし、カプセル化されたプロパティを新しいメッセージに書き込むには、 [ITnef:: ExtractProps](itnef-extractprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac370-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="ac370-124">エンコードされていないプロパティと重複しているエンコード済みのプロパティは、エンコードされたプロパティがデコードされるときに、エンコードされていないプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="ac370-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="ac370-125">[ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを使用して、メッセージテキストを解析し、メッセージテキストのタグから添付ファイルの位置を復元します。</span><span class="sxs-lookup"><span data-stu-id="ac370-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

