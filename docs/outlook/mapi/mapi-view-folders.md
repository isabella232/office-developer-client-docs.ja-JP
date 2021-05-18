---
title: MAPI ビュー フォルダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412535"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="17482-103">MAPI ビュー フォルダー</span><span class="sxs-lookup"><span data-stu-id="17482-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="17482-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17482-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17482-105">ビュー フォルダーは、関連情報を含むルート フォルダーで、対人間メッセージ (IPM) フォルダーのコンテンツの代替表示レイアウトを定義します。</span><span class="sxs-lookup"><span data-stu-id="17482-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="17482-106">ビュー フォルダーはメッセージ ストアのルートの下に存在するため、一般的なクライアント アプリケーションには表示されません。</span><span class="sxs-lookup"><span data-stu-id="17482-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="17482-107">すべてのメッセージ ストアにビュー フォルダーが含まれる場合があります。セッションの既定のメッセージ ストアとして動作するように構成されているメッセージ ストアだけが、それらを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="17482-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="17482-108">MAPI では、次の 2 つのビュー フォルダーがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="17482-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="17482-109">Common — 共通ビュー フォルダーには、メッセージ ストアに標準のビューが含まれているので、メッセージ ストアにアクセスするクライアントの任意のユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="17482-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="17482-110">共通ビュー フォルダーのエントリ識別子は、ストアのプロパティ **(** [PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) PR_COMMON_VIEWS_ENTRYIDに格納されます。</span><span class="sxs-lookup"><span data-stu-id="17482-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="17482-111">個人用 - 個人用ビュー フォルダーには、特定のユーザーによって定義されたビューが含まれる。</span><span class="sxs-lookup"><span data-stu-id="17482-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="17482-112">MAPI では、個人用 **PR_VIEWS_ENTRYID** のエントリ識別子を保持するプロパティ [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="17482-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="17482-113">たとえば、個人用ビューを使用すると、1 人のユーザーが送信者別に並べ替えたメッセージのグループを確認し、メッセージの件名と受信日のみを一覧に表示できます。別のユーザーは、日付順に並べ替えた同じグループを見て、件名、送信者、メッセージ サイズを一覧に表示できます。</span><span class="sxs-lookup"><span data-stu-id="17482-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17482-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="17482-114">See also</span></span>



<span data-ttu-id="17482-115">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="17482-115">[MAPI Folders](mapi-folders.md)</span></span>

