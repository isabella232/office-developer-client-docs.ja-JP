---
title: TNEF ユーザー設定添付ファイル処理を使用したメッセージの受信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588028"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="feac9-103">TNEF ユーザー設定添付ファイル処理を使用したメッセージの受信</span><span class="sxs-lookup"><span data-stu-id="feac9-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="feac9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feac9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feac9-105">TNEF メッセージを受信するには、添付ファイルの処理をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="feac9-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="feac9-106">転送可能なすべてのプロパティをインポートする、メッセージング システムをサポートしている-新しい MAPI メッセージへの受信メッセージから。</span><span class="sxs-lookup"><span data-stu-id="feac9-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="feac9-107">これには、TNEF データ ストリームが含まれているメッセージのテキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac9-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="feac9-108">識別し、特別な TNEF ストリームが含まれている添付ファイルをデコードします。</span><span class="sxs-lookup"><span data-stu-id="feac9-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="feac9-109">新しい MAPI メッセージに添付ファイルを MAPI への受信メッセージからのすべての添付ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="feac9-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="feac9-110">リカバリされたファイル名、または、添付ファイルを識別するその他のマーカー配置、 **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティに新しい添付ファイルする[ITnef::ExtractProps](itnef-extractprops.md)メソッド関連付けることができます後で正しい添付ファイル メッセージのテキストでエンコードされた添付ファイルのタグです。</span><span class="sxs-lookup"><span data-stu-id="feac9-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="feac9-111">TNEF ストリームをデコードの周りをラップし、 [OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで新しい MAPI メッセージには、そのオブジェクトを使用する OLE **IStream**インターフェイスを作成します。</span><span class="sxs-lookup"><span data-stu-id="feac9-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="feac9-112">TNEF データ ストリームからのメッセージの nontransmittable プロパティを回復する**ITnef::ExtractProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="feac9-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="feac9-113">タグと MAPI_MODIFY フラグのセットを使用して[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="feac9-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="feac9-114">この呼び出しは、メッセージから添付ファイル タグが削除、MAPI メッセージに添付ファイルの位置情報に変換して、します。</span><span class="sxs-lookup"><span data-stu-id="feac9-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="feac9-115">MAPI スプーラーによってメッセージを配信します。</span><span class="sxs-lookup"><span data-stu-id="feac9-115">Deliver the message through the MAPI spooler.</span></span>
    

