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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399571"
---
# <a name="tnef-processing"></a><span data-ttu-id="66367-103">TNEF 処理</span><span class="sxs-lookup"><span data-stu-id="66367-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="66367-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66367-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66367-105">次の一連のアクションでは、送信および受信メッセージを処理するトランスポートが TNEF のメソッドを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="66367-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="66367-106">**TNEF ストリームを含むメッセージを送信するのには**</span><span class="sxs-lookup"><span data-stu-id="66367-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="66367-107">メッセージング システムでサポートされているメッセージのプロパティを処理します。</span><span class="sxs-lookup"><span data-stu-id="66367-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="66367-108">メッセージを開封済みの実装で特定方法ため、受信側のトランスポート プロバイダーを判断できますメッセージが TNEF の処理を必要とします。</span><span class="sxs-lookup"><span data-stu-id="66367-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="66367-109">たとえば、SMTP メッセージング システムに送信する TNEF の転送プロバイダーは、"X-が含まれています-TNEF"メッセージで TNEF データが含まれていることを示すようにカスタム ヘッダー フィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="66367-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="66367-110">TNEF オブジェクトを取得して、TNEF ストリームに、メッセージング システムでサポートされていないメッセージのプロパティをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="66367-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="66367-111">メッセージング システムの添付ファイルのモデルを使用して、TNEF ストリームをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="66367-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="66367-112">などのアタッチメント モデルを基になる uuencode の添付ファイルには、それらをメッセージのテキストに追加し、トランスポート プロバイダーは、必要があります uuencode TNEF ストリーム別の添付ファイルにします。</span><span class="sxs-lookup"><span data-stu-id="66367-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="66367-113">トランスポート プロバイダーでは、どの添付ファイルにエンコード済みの TNEF ストリームが含まれている場合メッセージを受信したときを認識するためメソッドも実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="66367-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="66367-114">この添付ファイルをマークするための標準的な方法が"WINMAIL の添付ファイルの名前を指定するには。DAT"です。</span><span class="sxs-lookup"><span data-stu-id="66367-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="66367-115">トランスポート プロバイダーは、この規則に従っている他の TNEF を有効にしたトランスポート プロバイダーはこれと相互運用することになります。</span><span class="sxs-lookup"><span data-stu-id="66367-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="66367-116">使用[ITnef: IUnknown](itnefiunknown.md)インターフェイスのメソッドはメッセージのテキストでのメッセージの添付ファイルの位置を記述するタグを挿入します。</span><span class="sxs-lookup"><span data-stu-id="66367-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="66367-117">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)の方法でタグ付けされたメッセージのテキストにアクセスし、メッセージング システムに送信します。</span><span class="sxs-lookup"><span data-stu-id="66367-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="66367-118">**カプセル化されたプロパティを取得するには**</span><span class="sxs-lookup"><span data-stu-id="66367-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="66367-119">カプセル化されたプロパティが含まれるタグ付きのメッセージのテキストを含む、新しいメッセージにメッセージング システムによってサポートされるプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="66367-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="66367-120">適切な添付ファイルの TNEF ストリームをデコードします。</span><span class="sxs-lookup"><span data-stu-id="66367-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="66367-121">他のすべての添付ファイルをデコードし、新しい MAPI 添付ファイルにメッセージを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="66367-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="66367-122">[OpenTnefStreamEx](opentnefstreamex.md)関数を使用してデコードの TNEF ストリームを開きます。</span><span class="sxs-lookup"><span data-stu-id="66367-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="66367-123">TNEF ストリームをデコードし、新しいメッセージにカプセル化されたプロパティを書き込むには、 [ITnef::ExtractProps](itnef-extractprops.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="66367-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="66367-124">エンコードのプロパティは、デコードすると nonencoded プロパティを nonencoded プロパティの重複するエンコード済みのプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="66367-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="66367-125">[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを使用すると、メッセージのテキスト内のタグからの添付ファイルの位置を復元するのにメッセージのテキストを解析します。</span><span class="sxs-lookup"><span data-stu-id="66367-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

