---
title: TNEF によるメッセージのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336702"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="64ab4-103">TNEF によるメッセージのエンコード</span><span class="sxs-lookup"><span data-stu-id="64ab4-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="64ab4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64ab4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64ab4-105">メッセージが送信されると、トランスポートプロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="64ab4-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="64ab4-106">次に、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスがファイルをラップします。</span><span class="sxs-lookup"><span data-stu-id="64ab4-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="64ab4-107">次に、トランスポートプロバイダーは、 [ITnef](itnefiunknown.md)メソッドを使用して、受信側トランスポートプロバイダーが簡単にプロパティを解読できるようにするタグ付き形式のストリームにメッセージプロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="64ab4-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="64ab4-108">**メッセージ全体を1つのファイルで表すには**</span><span class="sxs-lookup"><span data-stu-id="64ab4-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="64ab4-109">[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって、TNEF オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="64ab4-110">[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、メッセージに対して定義されているすべてのプロパティの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="64ab4-111">メッセージシステムでサポートされているすべてのプロパティを除外するには、 [imapiprop](imapipropiunknown.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="64ab4-112">適切なタイミングで、メッセージングシステムが必要とする形式で、これらのプロパティをメッセージングシステムに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="64ab4-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="64ab4-113">[ITnef:: addprops](itnef-addprops.md)を呼び出して、残りのプロパティ (すべての添付ファイルを含む) をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="64ab4-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="64ab4-114">要求されたすべてのプロパティが追加された後に、メッセージを TNEF ストリームにエンコードするには、 [ITnef:: Finish](itnef-finish.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="64ab4-115">タグ付きメッセージテキストを取得するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="64ab4-116">このタグ付きテキストは、OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスのメソッドを使用してメッセージングシステムに書き出されます。</span><span class="sxs-lookup"><span data-stu-id="64ab4-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="64ab4-117">[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、 **ITnef**オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="64ab4-118">**受信 TNEF メッセージを処理するには**</span><span class="sxs-lookup"><span data-stu-id="64ab4-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="64ab4-119">mapi スプーラーから mapi メッセージオブジェクトを取得し、新しい mapi メッセージにメッセージヘッダーのプロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="64ab4-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="64ab4-120">受信メッセージからの TNEF データを格納する[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを作成して初期化します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="64ab4-121">MAPI メッセージと[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="64ab4-122">[ITnef:: ExtractProps](itnef-extractprops.md)メソッドを呼び出して、TNEF データ内の情報をデコードします。</span><span class="sxs-lookup"><span data-stu-id="64ab4-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="64ab4-123">**ExtractProps**によってデコードされたすべてのプロパティは、受信メッセージのエンベロープからデコードされたプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="64ab4-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="64ab4-124">つまり、抽出された TNEF プロパティは、メッセージ内の既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="64ab4-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="64ab4-125">タグ付きメッセージテキストを処理するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)を呼び出し、テキストを解析して添付ファイルの位置を復元します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="64ab4-126">[imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出して、メッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="64ab4-127">[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、TNEF オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="64ab4-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

