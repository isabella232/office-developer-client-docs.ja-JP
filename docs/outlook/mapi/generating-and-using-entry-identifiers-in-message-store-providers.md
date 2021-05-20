---
title: メッセージ ストア プロバイダーでのエントリ識別子の生成と使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437680"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="339ea-103">メッセージ ストア プロバイダーでのエントリ識別子の生成と使用</span><span class="sxs-lookup"><span data-stu-id="339ea-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="339ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="339ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="339ea-105">新しいフォルダーまたはメッセージがメッセージ ストアに作成されると、メッセージ ストア プロバイダーは、クライアント アプリケーションが参照できるよう、そのオブジェクトにエントリ識別子を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="339ea-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="339ea-106">メッセージ ストア プロバイダーは、削除されたオブジェクトの古い長期エントリ識別子を再利用するか、新しい識別子を作成できます。</span><span class="sxs-lookup"><span data-stu-id="339ea-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="339ea-107">メッセージ ストア プロバイダーに対して、一方の方法または他の要件はありません。ただし、可能であれば、メッセージ ストア プロバイダーは、古いオブジェクトを再利用するのではなく、新しいオブジェクトの新しい長期エントリ識別子を常に生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="339ea-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="339ea-108">参照するオブジェクトが削除された場合は、短期エントリ識別子を再利用して問題ありません。</span><span class="sxs-lookup"><span data-stu-id="339ea-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="339ea-109">この削除の理由は、クライアントがエントリ識別子をキャッシュできる場合が多く、長時間保存される場合があるからです。</span><span class="sxs-lookup"><span data-stu-id="339ea-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="339ea-110">その場合、メッセージ ストア プロバイダーがエントリ識別子を再利用する場合、クライアントがエントリ識別子を最初に取得した場合とは異なるオブジェクトを参照できます。</span><span class="sxs-lookup"><span data-stu-id="339ea-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="339ea-111">メッセージ ストア プロバイダーがエントリ識別子を再利用しない場合、または少なくとも非常に長い時間繰り返されないエントリ識別子生成スキームを使用する場合、この問題は発生しません。</span><span class="sxs-lookup"><span data-stu-id="339ea-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="339ea-112">同様に、メッセージ ストア プロバイダーは、フォルダーとメッセージがメッセージ ストア内で移動するときに、エントリ識別子を保持しようとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="339ea-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="339ea-113">メッセージ ストア プロバイダーがこれを行う場合、オブジェクトをストア内の別の場所に移動すると、ストア内のオブジェクトへの参照は無効になります。</span><span class="sxs-lookup"><span data-stu-id="339ea-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="339ea-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="339ea-114">See also</span></span>

- <span data-ttu-id="339ea-115">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="339ea-115">[Message Store Features](message-store-features.md)</span></span>

