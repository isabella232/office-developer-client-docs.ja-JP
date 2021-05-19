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
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="47ac5-103">TNEF によるメッセージのエンコード</span><span class="sxs-lookup"><span data-stu-id="47ac5-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="47ac5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ac5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ac5-105">メッセージが送信されると、トランスポート プロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="47ac5-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="47ac5-106">次に [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスがファイルにラップされます。</span><span class="sxs-lookup"><span data-stu-id="47ac5-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="47ac5-107">次に、トランスポート プロバイダーは [ITnef](itnefiunknown.md) メソッドを使用して、メッセージ プロパティをタグ付き形式でストリームに書き込み、受信トランスポート プロバイダーによってプロパティを簡単にデコードできます。</span><span class="sxs-lookup"><span data-stu-id="47ac5-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="47ac5-108">**1 つのファイル内のメッセージ全体を表す**</span><span class="sxs-lookup"><span data-stu-id="47ac5-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="47ac5-109">IStream オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡して[、TNEF](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="47ac5-110">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="47ac5-111">[IMAPIProp メソッドを](imapipropiunknown.md)使用して、メッセージング システムでサポートされているすべてのプロパティを除外します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="47ac5-112">適切な時点で、メッセージング システムに必要な形式でこれらのプロパティをメッセージング システムに書き込む。</span><span class="sxs-lookup"><span data-stu-id="47ac5-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="47ac5-113">[ITnef::AddProps](itnef-addprops.md)を呼び出して、すべての添付ファイルを含む残りのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="47ac5-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="47ac5-114">要求された [プロパティが追加された後、ITnef::Finish](itnef-finish.md) メソッドを呼び出して、メッセージを TNEF ストリームにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="47ac5-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="47ac5-115">タグ付 [きメッセージ テキストを取得するには、ITnef::OpenTaggedBody](itnef-opentaggedbody.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="47ac5-116">このタグ付きテキストは、OLE IStream インターフェイスのメソッドを使用してメッセージング システム [に書き込](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) まれます。</span><span class="sxs-lookup"><span data-stu-id="47ac5-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="47ac5-117">[IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)出して **、ITnef オブジェクトを解放** します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="47ac5-118">**受信 TNEF メッセージを処理するには**</span><span class="sxs-lookup"><span data-stu-id="47ac5-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="47ac5-119">MAPI スプーラーから MAPI メッセージ オブジェクトを取得し、新しい MAPI メッセージにメッセージ ヘッダー プロパティを書き込む。</span><span class="sxs-lookup"><span data-stu-id="47ac5-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="47ac5-120">受信メッセージの [TNEF](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) データを含む IStream オブジェクトを作成および初期化します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="47ac5-121">MAPI メッセージと [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) オブジェクトを [OpenTnefStreamEx 関数に渡](opentnefstreamex.md) します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="47ac5-122">[ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出して、TNEF データ内の情報をデコードします。</span><span class="sxs-lookup"><span data-stu-id="47ac5-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="47ac5-123">**ExtractProps でデコードされた内容は、** 受信メッセージのエンベロープからデコードされたプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="47ac5-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="47ac5-124">つまり、抽出された TNEF プロパティは、メッセージ内の既存のプロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="47ac5-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="47ac5-125">[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)を呼び出してタグ付きメッセージ テキストを処理し、テキストを解析して添付ファイルの位置を回復します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="47ac5-126">[IMAPIProp::SaveChanges を呼び出してメッセージを保存します](imapiprop-savechanges.md)。</span><span class="sxs-lookup"><span data-stu-id="47ac5-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="47ac5-127">[IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、TNEF オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="47ac5-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

