---
title: 生成して、メッセージのエントリ id を使用してプロバイダーを格納します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565453"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a><span data-ttu-id="5022a-103">生成して、メッセージのエントリ id を使用してプロバイダーを格納します。</span><span class="sxs-lookup"><span data-stu-id="5022a-103">Generating and using entry identifiers in message store providers</span></span>

<span data-ttu-id="5022a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5022a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5022a-105">新しいフォルダーまたはメッセージがメッセージ ・ ストアに作成されると、メッセージ ストア プロバイダーが、クライアント アプリケーションが参照できるように、そのオブジェクトのエントリ id を割り当ています。</span><span class="sxs-lookup"><span data-stu-id="5022a-105">When a new folder or message is created in a message store, the message store provider has to assign that object an entry identifier so that client applications can refer to it.</span></span> <span data-ttu-id="5022a-106">メッセージ ストア プロバイダー削除されたオブジェクトの非アクティブの長期的なエントリ id を再利用するか、新しい id を作成します。</span><span class="sxs-lookup"><span data-stu-id="5022a-106">Message store providers can either reuse the defunct long-term entry identifiers of deleted objects or create new identifiers.</span></span> <span data-ttu-id="5022a-107">不要の方法の 1 つまたは別のメッセージ ストア プロバイダーです。ただし、実現可能な場合は、メッセージ ストア プロバイダーする必要がありますは常に生成の再利用の古いものではなく、新しいオブジェクトの新しい長期的なエントリ id です。</span><span class="sxs-lookup"><span data-stu-id="5022a-107">There is no requirement one way or the other for message store providers; however, if it is feasible, a message store provider should always generate new long-term entry identifiers for new objects rather than reusing old ones.</span></span> <span data-ttu-id="5022a-108">参照しているオブジェクトが削除されたときは、短期的なエントリ id を再利用するのには十分です。</span><span class="sxs-lookup"><span data-stu-id="5022a-108">It is fine to reuse short-term entry identifiers when the objects they refer to are deleted.</span></span>
  
<span data-ttu-id="5022a-109">この削除の理由は、クライアントことができますをキャッシュするエントリの識別子も長期間のです。</span><span class="sxs-lookup"><span data-stu-id="5022a-109">The reason for this deletion is that clients can cache entry identifiers, sometimes for long periods of time.</span></span> <span data-ttu-id="5022a-110">メッセージ ストア プロバイダーのエントリの識別子は再利用が発生した場合、エントリの識別子を取得するときよりも、エントリ id を開くと、クライアントに別のオブジェクトを参照するエントリの識別子のことができます。</span><span class="sxs-lookup"><span data-stu-id="5022a-110">If that happens and the message store provider does reuse entry identifiers, it is possible for the entry identifier to refer to a different object when the client opens the entry identifier than when it first obtained the entry identifier.</span></span> <span data-ttu-id="5022a-111">メッセージ ストア プロバイダーはエントリの識別子を再利用しないかどうか、またはエントリの識別子の生成の方式で、非常に長い時間が繰り返されないことを少なくとも使用: この問題が発生することはできません。</span><span class="sxs-lookup"><span data-stu-id="5022a-111">If the message store provider does not reuse entry identifiers — or at least uses an entry identifier generation scheme that does not repeat for a very long time — this problem cannot occur.</span></span>
  
<span data-ttu-id="5022a-112">同様に、メッセージ ストア プロバイダーは、メッセージ ・ ストアに移動したときに、フォルダーやメッセージのエントリ id を保持するために試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5022a-112">Similarly, message store providers should attempt to preserve entry identifiers for folders and messages when they are moved in the message store.</span></span> <span data-ttu-id="5022a-113">メッセージ ストア プロバイダーは、するには、ストア内のオブジェクトへの参照はオブジェクトがストア内の別の場所に移動すると、無効なはなりません。</span><span class="sxs-lookup"><span data-stu-id="5022a-113">If the message store provider can do that, references to objects in the store will not become invalid when the object is moved to a different location in the store.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5022a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="5022a-114">See also</span></span>

- <span data-ttu-id="5022a-115">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="5022a-115">[Message Store Features](message-store-features.md)</span></span>

