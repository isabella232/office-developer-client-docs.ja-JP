---
title: TNEF カスタム添付ファイル処理を使用したメッセージの受信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328428"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="a62a6-103">TNEF カスタム添付ファイル処理を使用したメッセージの受信</span><span class="sxs-lookup"><span data-stu-id="a62a6-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="a62a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a62a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a62a6-105">カスタマイズされた添付ファイル処理を伴う TNEF メッセージを受信するには</span><span class="sxs-lookup"><span data-stu-id="a62a6-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="a62a6-106">受信メッセージから新しい MAPI メッセージに、すべての送信機テーブルプロパティ (メッセージングシステムがサポートするもの) をインポートします。</span><span class="sxs-lookup"><span data-stu-id="a62a6-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="a62a6-107">これには、TNEF データストリームを含むメッセージテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a6-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="a62a6-108">TNEF ストリームを含む特殊な添付ファイルを識別し、デコードします。</span><span class="sxs-lookup"><span data-stu-id="a62a6-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="a62a6-109">受信メッセージからすべての添付ファイルを新しい mapi メッセージの mapi 添付ファイルに抽出します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="a62a6-110">回復されたファイル名、または添付ファイルの他の識別マーカーを、 [ITnef:: ExtractProps](itnef-extractprops.md)メソッドを使用して、新しい添付ファイルの**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティに配置する必要があります。後で、適切な添付ファイルを、メッセージテキストでエンコードされた添付ファイルタグに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a62a6-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="a62a6-111">デコードされた TNEF ストリームをラップする OLE **IStream**インターフェイスを作成し、そのオブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで新しい MAPI メッセージと共に使用します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="a62a6-112">**ITnef:: ExtractProps**メソッドを呼び出して、TNEF データストリームからメッセージのノン非対称テーブルプロパティを回復します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="a62a6-113">MAPI_CREATE および MAPI_MODIFY フラグセットを使用して、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="a62a6-114">この呼び出しは、メッセージテキストから attachment タグを削除し、それを MAPI メッセージの添付ファイルの位置情報に変換します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="a62a6-115">MAPI スプーラーを経由してメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="a62a6-115">Deliver the message through the MAPI spooler.</span></span>
    

