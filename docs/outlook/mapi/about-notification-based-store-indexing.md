---
title: 通知ベースのストアインデックス作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409175"
---
# <a name="about-notification-based-store-indexing"></a><span data-ttu-id="3c1c6-103">通知ベースのストアインデックス作成について</span><span class="sxs-lookup"><span data-stu-id="3c1c6-103">About Notification-Based Store Indexing</span></span>

  
  
<span data-ttu-id="3c1c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c1c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c1c6-105">mapi ストアプロバイダーでは、mapi プロトコルハンドラーがストア内のメッセージをクロールしてインデックスを作成するか、インデックス付けするメッセージがある場合に、ストアがインデクサーに通知を送信するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-105">A MAPI store provider can specify whether the MAPI Protocol Handler crawls and indexes messages in the store, or whether the store sends notifications to the indexer when there are messages to be indexed.</span></span> <span data-ttu-id="3c1c6-106">後者は通知ベースのインデックス作成と呼ばれ、通知ベースのインデックスをサポートするストアは pusher ストアと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-106">The latter is known as notification-based indexing, and a store that supports notification-based indexing is a known as a pusher store.</span></span>
  
<span data-ttu-id="3c1c6-107">通知ベースのインデックス処理をサポートするストアプロバイダーは、 **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティの**STORE_PUSHER_OK**フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-107">A store provider that supports notification-based indexing sets the **STORE_PUSHER_OK** flag in the **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** property.</span></span> <span data-ttu-id="3c1c6-108">MAPI プロトコルハンドラーまたはクライアントは、 **PR_STORE_SUPPORT_MASK**プロパティを取得してストアの特性を決定できます。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-108">The MAPI Protocol Handler or a client can get the **PR_STORE_SUPPORT_MASK** property to determine the characteristics of the store.</span></span> 
  
<span data-ttu-id="3c1c6-109">添付ファイル、フォルダー、またはメッセージがインデックス化されるたびに、ストアプロバイダーは、インデックスを作成するオブジェクトを識別する MAPI Uniform resource Locator (URL) を生成し、それをインデクサーに送信します。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-109">Whenever there is an attachment, folder, or a message to be indexed, the store provider generates a MAPI Uniform Resource Locator (URL) identifying the object to be indexed and sends it to the indexer.</span></span> <span data-ttu-id="3c1c6-110">この mapi URL は Unicode でエンコードされ、mapi プロトコルハンドラーに対して一意にオブジェクトを識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-110">This MAPI URL is encoded in Unicode and must uniquely identify the object to the MAPI Protocol Handler.</span></span> <span data-ttu-id="3c1c6-111">mapi url の詳細については、「[通知ベースのインデックス作成の mapi url につい](about-mapi-urls-for-notification-based-indexing.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-111">For more information about MAPI URLs, see [About MAPI URLs for Notification-Based Indexing](about-mapi-urls-for-notification-based-indexing.md).</span></span>
  
<span data-ttu-id="3c1c6-112">pusher ストアでシャットダウンが発生する前に、インデクサーは常にすべてのインデックスを作成することはできないため、pusher ストアは、プッシュする必要のあるものを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-112">Because an indexer cannot always index everything before a shutdown occurs in a pusher store, the pusher store must persist what needs to be pushed.</span></span> <span data-ttu-id="3c1c6-113">ストアプロバイダーは、インデックスを必要とするオブジェクトについての通知を送信するときに、通知構造の**uleventtype**メンバーで通知**[](notification.md)** タイプ**fnevIndexing**を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-113">When a store provider sends a notification about an object that needs to be indexed, it specifies the notification type **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure.</span></span> <span data-ttu-id="3c1c6-114">**NOTIFICATION** 構造の **info** メンバーには、**[EXTENDED_NOTIFICATION](extended_notification.md)** 構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-114">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span> <span data-ttu-id="3c1c6-115">ストアプロバイダーは、 **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** プロパティでプロセスを識別します。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-115">The store provider identifies the process in the **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** property.</span></span> <span data-ttu-id="3c1c6-116">また、 [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)構造体のプロセスを識別し、この情報を**EXTENDED_NOTIFICATION**構造の**p傾斜 entparameters**メンバーの一部として渡します。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-116">It also identifies the process in the [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md) structure, and passes this information as part of the **pbEventParameters** member of the **EXTENDED_NOTIFICATION** structure.</span></span> <span data-ttu-id="3c1c6-117">プロセスがシャットダウンまたはクラッシュした場合、MAPI プロトコルハンドラーはすぐにそのことを検出し、pusher ストアのインデックス作成を停止できます。</span><span class="sxs-lookup"><span data-stu-id="3c1c6-117">If the process is shut down or crashes, the MAPI Protocol Handler will be able to immediately detect that and stop indexing the pusher store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c1c6-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c1c6-118">See also</span></span>



[<span data-ttu-id="3c1c6-119">ストア API について</span><span class="sxs-lookup"><span data-stu-id="3c1c6-119">About the Store API</span></span>](about-the-store-api.md)
  
[<span data-ttu-id="3c1c6-120">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="3c1c6-120">MAPI Constants</span></span>](mapi-constants.md)

