---
title: メッセージストアプロバイダーに RTF テキストをサポートする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349617"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="6c789-103">メッセージストアプロバイダーに RTF テキストをサポートする</span><span class="sxs-lookup"><span data-stu-id="6c789-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="6c789-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c789-105">一部のクライアントアプリケーションでは、ユーザーがメッセージでリッチテキスト形式 (RTF) のテキストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c789-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="6c789-106">メッセージストアプロバイダーがメッセージ内の RTF テキストをサポートする必要がある場合は、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに加えて、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c789-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="6c789-107">主に、これは、両方のプロパティを格納し、 **PR_BODY**が**PR_RTF_COMPRESSED**のテキストのプレーンテキストバージョンを含んでいることを確認することを意味します。</span><span class="sxs-lookup"><span data-stu-id="6c789-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="6c789-108">[rtfsync](rtfsync.md)関数は、このために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6c789-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="6c789-109">メッセージストアオブジェクトの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに設定して、 **PR_BODY**および PR_ に関して、メッセージストアプロバイダーから期待されることをクライアントに通知する2つのフラグがあります。 \*\*\*\* メッセージストア内のメッセージの RTF_COMPRESSED プロパティ。</span><span class="sxs-lookup"><span data-stu-id="6c789-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="6c789-110">STORE_RTF_OK フラグは、ストアが**PR_RTF_COMPRESSED**プロパティから**PR_BODY**プロパティの値を動的に生成できることを示します。これにより、クライアントを明示的に同期する負荷が軽減されます。</span><span class="sxs-lookup"><span data-stu-id="6c789-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="6c789-111">STORE_UNCOMPRESSED_RTF フラグは、メッセージストアプロバイダーが**PR_RTF_COMPRESSED**内の圧縮されていないデータをサポートできることを示します。</span><span class="sxs-lookup"><span data-stu-id="6c789-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="6c789-112">rtf テキストをサポートしていないメッセージストアプロバイダーは、rtf テキストをサポートするクライアントアプリケーションと適切に相互運用するために**PR_BODY**プロパティが変更されたときに、 **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。.</span><span class="sxs-lookup"><span data-stu-id="6c789-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c789-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c789-113">See also</span></span>



<span data-ttu-id="6c789-114">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="6c789-114">[Message Store Features](message-store-features.md)</span></span>

