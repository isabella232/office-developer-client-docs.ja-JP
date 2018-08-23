---
title: 通知ベースのストア インデックス作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799601"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="c25b5-103">通知ベースのストア インデックス作成について</span><span class="sxs-lookup"><span data-stu-id="c25b5-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="c25b5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c25b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c25b5-105">MAPI ストア プロバイダーは、ストアでの MAPI プロトコル ハンドラーのクロールとインデックスのメッセージかどうか、またはかどうか、ストアに通知を送信、インデクサー インデックスを作成するメッセージがある場合に指定できます。</span><span class="sxs-lookup"><span data-stu-id="c25b5-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="c25b5-106">後者し、呼ばれ通知ベースのインデックス作成、通知ベースのインデックス作成をサポートしているストアは、プッシュ型ストアとして、知られています。</span><span class="sxs-lookup"><span data-stu-id="c25b5-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="c25b5-107">**[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティのインデックス設定の通知に基づく**STORE_PUSHER_OK**フラグをサポートしているストア プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="c25b5-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="c25b5-108">MAPI プロトコル ハンドラー、またはクライアントは、ストアの特性を決定する**PR_STORE_SUPPORT_MASK**プロパティを取得できます。</span><span class="sxs-lookup"><span data-stu-id="c25b5-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="c25b5-109">添付ファイル、フォルダー、またはインデックスを作成するメッセージがある場合、ストア プロバイダーは、MAPI (URL) オブジェクトを識別するインデックスを作成するを生成し、インデクサーに送信します。</span><span class="sxs-lookup"><span data-stu-id="c25b5-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="c25b5-110">この MAPI URL は Unicode でエンコードされてされ、MAPI プロトコル ハンドラー オブジェクトを一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25b5-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="c25b5-111">MAPI Url の詳細については、[通知ベースのインデックス作成用に MAPI Url について](about-mapi-urls-for-notification-based-indexing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25b5-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="c25b5-112">インデクサー常にインデックスを作成できませんすべてのプッシュ型ストアのシャット ダウンが発生する前に、ためプッシュ型ストアがプッシュする必要のあるを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25b5-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="c25b5-113">ストア プロバイダーは、インデックスを作成する必要のあるオブジェクトに通知を送信するときは、**[通知](notification.md)** の構造体の**ulEventType**メンバーに通知の種類の**fnevIndexing**を指定します。</span><span class="sxs-lookup"><span data-stu-id="c25b5-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="c25b5-114">**通知**の構造体のメンバー**情報**には、 **[EXTENDED_NOTIFICATION](extended_notification.md)** 構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c25b5-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="c25b5-115">ストア プロバイダーは、 **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** プロパティにはそのプロセスを識別します。</span><span class="sxs-lookup"><span data-stu-id="c25b5-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="c25b5-116">また、 [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)構造で、プロセスを識別し、 **pbEventParameters** 、 **EXTENDED_NOTIFICATION**構造体のメンバーの一部としてこの情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="c25b5-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="c25b5-117">プロセスがシャット ダウンまたはクラッシュした場合、MAPI プロトコル ハンドラーはすぐに検出して、プッシュ型ストアのインデックス作成を停止することになります。</span><span class="sxs-lookup"><span data-stu-id="c25b5-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c25b5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c25b5-118">See also</span></span>



[<span data-ttu-id="c25b5-119">ストア API について</span><span class="sxs-lookup"><span data-stu-id="c25b5-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="c25b5-120">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="c25b5-120">MAPI Constants</span></span>](mapi-constants.md)

