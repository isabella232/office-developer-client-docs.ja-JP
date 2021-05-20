---
title: 送信メッセージの書式設定されたテキストのサポート クライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431604"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a><span data-ttu-id="f61a5-103">送信メッセージでの書式設定されたテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="f61a5-103">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>

  
  
<span data-ttu-id="f61a5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f61a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f61a5-105">クライアント アプリケーションは **、PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ **、PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ、または送信メッセージの **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f61a5-105">Client applications set the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, or the **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) property for an outgoing message.</span></span> <span data-ttu-id="f61a5-106">プレーン テキスト セットのみをサポートするクライアントは、PR_BODY **プロパティのみです** 。</span><span class="sxs-lookup"><span data-stu-id="f61a5-106">Clients that support only plain text set only the **PR_BODY** property.</span></span> <span data-ttu-id="f61a5-107">リッチ テキスト形式 (RTF) 対応のクライアントは、使用するメッセージ ストア プロバイダーに応じて、PR_BODY プロパティと **PR_RTF_COMPRESSED** プロパティの両方を設定するか、PR_RTF_COMPRESSED のみを設定できます。 </span><span class="sxs-lookup"><span data-stu-id="f61a5-107">Rich Text Format (RTF)-aware clients might set both **PR_BODY** and **PR_RTF_COMPRESSED** properties, or only **PR_RTF_COMPRESSED**, depending on the message store provider being used.</span></span> <span data-ttu-id="f61a5-108">HTML 対応のクライアントは、PR_HTMLプロパティ **を設定** します。</span><span class="sxs-lookup"><span data-stu-id="f61a5-108">HTML-aware clients set the **PR_HTML** property.</span></span> 
  
<span data-ttu-id="f61a5-109">クライアントは、メッセージ ストアの PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティをチェックして、ストアが RTF をサポートするかどうかを判断することが重要です。</span><span class="sxs-lookup"><span data-stu-id="f61a5-109">It is important for a client to check its message store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to determine whether the store supports RTF.</span></span> <span data-ttu-id="f61a5-110">メッセージ ストアが RTF 対応ではない場合、RTF 対応クライアントは、送信メッセージごとに PR_BODYプロパティ **PR_RTF_COMPRESSEDプロパティの** 両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="f61a5-110">If the message store is not RTF-aware, an RTF-aware client sets both the **PR_BODY** and **PR_RTF_COMPRESSED** properties for each outgoing message.</span></span> 
  
<span data-ttu-id="f61a5-111">メッセージ ストアが RTF 対応の場合は **、PR_RTF_COMPRESSEDプロパティのみを** 設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f61a5-111">If the message store is RTF-aware, only the **PR_RTF_COMPRESSED** property needs to be set.</span></span> 
  
 <span data-ttu-id="f61a5-112">**必要にPR_RTF_COMPRESSED同期プロセスが実行されるのを確認するには、RTF 対応のクライアント**</span><span class="sxs-lookup"><span data-stu-id="f61a5-112">**To set PR_RTF_COMPRESSED and ensure that the synchronization process occurs as necessary, RTF-aware clients**</span></span>
  
1. <span data-ttu-id="f61a5-113">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、PR_RTF_COMPRESSED** プロパティを開き、MAPI_CREATEフラグMAPI_MODIFYします。</span><span class="sxs-lookup"><span data-stu-id="f61a5-113">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, setting both the MAPI_CREATE and MAPI_MODIFY flags.</span></span> <span data-ttu-id="f61a5-114">MAPI_CREATE、新しいデータが古いデータに置き換わり、MAPI_MODIFY置き換えできます。</span><span class="sxs-lookup"><span data-stu-id="f61a5-114">MAPI_CREATE ensures that any new data replaces any old data and MAPI_MODIFY enables you to make those replacements.</span></span> 
    
2. <span data-ttu-id="f61a5-115">メッセージ ストアが PR_STORE_SUPPORT_MASK プロパティに STORE_UNCOMPRESSED_RTF ビットを設定する場合は、WrapCompressedRTFStream 関数を呼び出し **、STORE_UNCOMPRESSED_RTF** を渡して **、OpenProperty** から返される PR_RTF_COMPRESSED ストリームの非圧縮バージョンを取得します。 [](wrapcompressedrtfstream.md) </span><span class="sxs-lookup"><span data-stu-id="f61a5-115">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing STORE_UNCOMPRESSED_RTF if the message store sets the STORE_UNCOMPRESSED_RTF bit in its **PR_STORE_SUPPORT_MASK** property, to get an uncompressed version of the **PR_RTF_COMPRESSED** stream returned from **OpenProperty**.</span></span>
    
3. <span data-ttu-id="f61a5-116">**WrapCompressedRTFStream** から返される非圧縮ストリームにメッセージ テキスト データを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f61a5-116">Write the message text data to the uncompressed stream returned from **WrapCompressedRTFStream**.</span></span>
    
4. <span data-ttu-id="f61a5-117">圧縮されていないストリームと圧縮されたストリームの両方をコミットして解放します。</span><span class="sxs-lookup"><span data-stu-id="f61a5-117">Commit and release both the uncompressed and compressed streams.</span></span>
    
<span data-ttu-id="f61a5-118">この時点で、メッセージ ストア プロバイダーが RTF をサポートしている場合は、必要なすべての処理を行いました。</span><span class="sxs-lookup"><span data-stu-id="f61a5-118">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="f61a5-119">必要に応じて、メッセージ ストア プロバイダーに依存して、同期プロセスと PR_BODY プロパティ **の** 作成を処理できます。</span><span class="sxs-lookup"><span data-stu-id="f61a5-119">You can depend on the message store provider to handle the synchronization process and the creation of the **PR_BODY** property, if necessary.</span></span> <span data-ttu-id="f61a5-120">ただし、メッセージ ストア プロバイダーが RTF をサポートしていない場合は [、RTFSync](rtfsync.md) 関数を呼び出してテキストを書式設定と同期し、RTF_SYNC_RTF_CHANGEDする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f61a5-120">However, if the message store provider does not support RTF, you must call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting, setting the RTF_SYNC_RTF_CHANGED flag.</span></span> 
  

