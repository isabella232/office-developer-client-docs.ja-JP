---
title: TNEF メッセージをエンコードします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2cb5c9a971f95e309f0a91cf477eefe98fe3bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800023"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="56780-103">TNEF メッセージをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="56780-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="56780-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56780-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="56780-105">メッセージが送信されると、トランスポート プロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="56780-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="56780-106">次に、 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスは、ファイルを囲みます。</span><span class="sxs-lookup"><span data-stu-id="56780-106">Next, an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="56780-107">トランスポート プロバイダーは、ストリームに書き込むメッセージのプロパティ、受信側のトランスポート プロバイダーが簡単にデコードするのににはプロパティを有効にするタグ付きの形式で、 [ITnef](itnefiunknown.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="56780-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="56780-108">**1 つのファイル全体のメッセージを表す**</span><span class="sxs-lookup"><span data-stu-id="56780-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="56780-109">[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって TNEF オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="56780-109">Obtain a TNEF object by passing an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="56780-110">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="56780-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="56780-111">[IMAPIProp](imapipropiunknown.md)メソッドを使用すると、メッセージング システムでサポートされているすべてのプロパティを除外できます。</span><span class="sxs-lookup"><span data-stu-id="56780-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="56780-112">適切なタイミングでは、メッセージング システムに必要な形式でのメッセージング システムにこれらのプロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="56780-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="56780-113">すべての添付ファイルを含め、他のプロパティをエンコードするために[ITnef::AddProps](itnef-addprops.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56780-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="56780-114">要求されたすべてのプロパティを追加した後は、TNEF ストリームにメッセージをエンコードするために[ITnef::Finish](itnef-finish.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56780-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="56780-115">タグ付きのメッセージ テキストを取得する[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56780-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="56780-116">このタグ付きテキストは、OLE の[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスからメソッドを使用してメッセージング システムに書き出されます。</span><span class="sxs-lookup"><span data-stu-id="56780-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="56780-117">**ITnef**オブジェクトを解放する[が](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="56780-117">Call the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="56780-118">**TNEF メッセージの受信を処理するのには**</span><span class="sxs-lookup"><span data-stu-id="56780-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="56780-119">MAPI スプーラーから MAPI メッセージ オブジェクトを取得し、新しい MAPI メッセージにメッセージのヘッダー プロパティを記述します。</span><span class="sxs-lookup"><span data-stu-id="56780-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="56780-120">作成し、受信メッセージの TNEF データが含まれている[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="56780-120">Create and initialize an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="56780-121">MAPI メッセージと[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)オブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="56780-121">Pass the MAPI message and the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="56780-122">[ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出すことによって TNEF データ内の情報をデコードします。</span><span class="sxs-lookup"><span data-stu-id="56780-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="56780-123">**ExtractProps**でデコードされたものは、受信メッセージのエンベロープからデコードされたプロパティで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="56780-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="56780-124">TNEF プロパティの抽出されたメッセージでは、既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="56780-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="56780-125">[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)を呼び出すことによってタグ付けされたメッセージのテキストを処理し、添付ファイルの位置を回復するのにはテキストを解析します。</span><span class="sxs-lookup"><span data-stu-id="56780-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="56780-126">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すことによって、メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="56780-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="56780-127">[](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)メソッドを呼び出すことによって TNEF オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="56780-127">Release the TNEF object by calling the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

