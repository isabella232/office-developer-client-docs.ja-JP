---
title: MAPI フォルダーの表示
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cb26771e9968175ab67366e35cf019ce23d51b8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801483"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="5c58f-103">MAPI フォルダーの表示</span><span class="sxs-lookup"><span data-stu-id="5c58f-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="5c58f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c58f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c58f-105">フォルダーの表示は、個人間メッセージ (IPM) のフォルダーの内容の別の表示のレイアウトを定義するのには関連する情報を含むルート フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="5c58f-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="5c58f-106">フォルダーの表示では、メッセージ ・ ストアのルートの下に存在する、したがって、一般的なクライアント アプリケーションで表示されているではありません。</span><span class="sxs-lookup"><span data-stu-id="5c58f-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="5c58f-107">すべてのメッセージ ストアには、フォルダー表示; にはが含まれています。セッションの既定のメッセージ ストアとして機能するように構成されている唯一のメッセージ ・ ストアには、それらを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c58f-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="5c58f-108">MAPI には、2 つのフォルダーの表示がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c58f-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="5c58f-109">共通、共通のフォルダー ビューにはには、メッセージ ・ ストアの標準であり、メッセージ ・ ストアにアクセスするクライアントのすべてのユーザーが使用できるビューが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c58f-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="5c58f-110">一般的なビュー フォルダーのエントリ id は、店舗の**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) のプロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5c58f-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="5c58f-111">個人、個人用ビューのフォルダーには、特定のユーザーが定義されているビューが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c58f-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="5c58f-112">MAPI では、個人用ビューのフォルダーのエントリ id を保持するための**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) のプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="5c58f-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="5c58f-113">個人用ビューを使用すると、たとえば、1 人のユーザー可能性があります見てメッセージの送信者にのみメッセージ件名および受入日付を一覧表示順のグループ他のユーザー、件名、送信者、およびメッセージのサイズを一覧表示、日付で並べ替えられた同じグループになります。</span><span class="sxs-lookup"><span data-stu-id="5c58f-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c58f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c58f-114">See also</span></span>



<span data-ttu-id="5c58f-115">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="5c58f-115">[MAPI Folders](mapi-folders.md)</span></span>

