---
title: メッセージ ストア プロバイダーでの RTF 形式テキストのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804070"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a><span data-ttu-id="f3723-103">メッセージ ストア プロバイダーでの RTF 形式テキストのサポート</span><span class="sxs-lookup"><span data-stu-id="f3723-103">Supporting RTF Text for Message Store Providers</span></span>

  
  
<span data-ttu-id="f3723-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3723-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3723-105">一部のクライアント アプリケーションは、メッセージでリッチ テキスト形式 (RTF) のテキストを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="f3723-105">Some client applications allow users to use Rich Text Format (RTF) text in their messages.</span></span> <span data-ttu-id="f3723-106">メッセージは、メッセージ内の rtf 形式のテキストをサポートするためにプロバイダーのニーズを保存する場合 ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティだけでなく、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3723-106">If your message store provider needs to support RTF text in messages, it needs to handle the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, in addition to the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property.</span></span> <span data-ttu-id="f3723-107">主に、つまり、両方のプロパティを格納する**PR_BODY には** **PR_RTF_COMPRESSED**内のテキストのプレーン テキスト版が含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3723-107">Primarily, this means storing both properties, and making sure that **PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="f3723-108">[](rtfsync.md)関数は、この目的のために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f3723-108">The [RTFSync](rtfsync.md) function is useful for this purpose.</span></span> 
  
<span data-ttu-id="f3723-109">2 つのフラグ メッセージ ストア オブジェクトの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティで設定可能なメッセージ ストア プロバイダー **PR_BODY**と**PR_ の点から何を期待できることをクライアントに通知します。RTF_COMPRESSED**メッセージ ・ ストア内のメッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="f3723-109">There are two flags that can be set in the message store object's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property that tell clients what they can expect from the message store provider with respect to the **PR_BODY** and **PR_RTF_COMPRESSED** properties on messages in the message store.</span></span> <span data-ttu-id="f3723-110">STORE_RTF_OK フラグは、ことストアから生成できます**PR_BODY**プロパティの値、 **PR_RTF_COMPRESSED**プロパティ、動的にクライアントが明示的に同期する際の負担を軽減するを示します。</span><span class="sxs-lookup"><span data-stu-id="f3723-110">The STORE_RTF_OK flag indicates that the store can generate the value of the **PR_BODY** property from the **PR_RTF_COMPRESSED** property dynamically, which relieves clients from the burden of synchronizing them explicitly.</span></span> <span data-ttu-id="f3723-111">STORE_UNCOMPRESSED_RTF フラグは、メッセージ ストア プロバイダーが**PR_RTF_COMPRESSED**の非圧縮データをサポートできることを示します。</span><span class="sxs-lookup"><span data-stu-id="f3723-111">The STORE_UNCOMPRESSED_RTF flag indicates that the message store provider can support uncompressed data in **PR_RTF_COMPRESSED**.</span></span>
  
<span data-ttu-id="f3723-112">Rtf 形式のテキストをサポートしていないメッセージ ストア プロバイダーは rtf 形式のテキストをサポートしているクライアント アプリケーションと適切に相互運用するために**PR_BODY**プロパティが変更されたときに**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティを削除する必要があります。.</span><span class="sxs-lookup"><span data-stu-id="f3723-112">Message store providers that do not support RTF text need to delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property when the **PR_BODY** property changes in order to interoperate properly with client applications that do support RTF text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3723-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3723-113">See also</span></span>



<span data-ttu-id="f3723-114">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="f3723-114">[Message Store Features](message-store-features.md)</span></span>

