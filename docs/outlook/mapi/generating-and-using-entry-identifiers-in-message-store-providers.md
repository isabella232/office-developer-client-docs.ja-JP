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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299813"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="5230f-103">メッセージ ストア プロバイダーでのエントリ識別子の生成と使用</span><span class="sxs-lookup"><span data-stu-id="5230f-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="5230f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5230f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5230f-105">メッセージストア内に新しいフォルダーまたはメッセージを作成する場合、メッセージストアプロバイダーは、クライアントアプリケーションがそれを参照できるように、そのオブジェクトにエントリ識別子を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5230f-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="5230f-106">メッセージストアプロバイダーは、削除されたオブジェクトに対して、非アクティブな長期間のエントリ識別子を再利用するか、または新しい識別子を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5230f-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="5230f-107">メッセージストアプロバイダーには、1つまたは2つの要件はありません。ただし、メッセージストアプロバイダーが実行可能である場合は、古いアイテムを再利用するのではなく、新しいオブジェクトに対して、常に新しい長期エントリ識別子を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5230f-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="5230f-108">使用するオブジェクトが削除されたときに、短期入力識別子を再利用するのは問題ありません。</span><span class="sxs-lookup"><span data-stu-id="5230f-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="5230f-109">この削除の理由は、クライアントがエントリ id をキャッシュすることができるのは、長時間かかる場合があるためです。</span><span class="sxs-lookup"><span data-stu-id="5230f-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="5230f-110">このような状況で、メッセージストアプロバイダーがエントリ識別子を再使用する場合は、エントリ id を最初に取得したときよりも、クライアントがエントリ識別子を開いたときに別のオブジェクトを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="5230f-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="5230f-111">メッセージストアプロバイダーがエントリ識別子を再利用しない場合、または少なくとも、非常に長い時間がかからないエントリ識別子生成スキームを使用している場合、この問題は発生しません。</span><span class="sxs-lookup"><span data-stu-id="5230f-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="5230f-112">同様に、メッセージストアプロバイダーは、メッセージストアに移動されたときに、フォルダーおよびメッセージのエントリ識別子の保持を試みる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5230f-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="5230f-113">メッセージストアプロバイダーがこれを行うことができる場合、そのオブジェクトがストア内の別の場所に移動されても、ストア内のオブジェクトへの参照は無効になりません。</span><span class="sxs-lookup"><span data-stu-id="5230f-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5230f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="5230f-114">See also</span></span>

- <span data-ttu-id="5230f-115">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="5230f-115">[Message Store Features](message-store-features.md)</span></span>

