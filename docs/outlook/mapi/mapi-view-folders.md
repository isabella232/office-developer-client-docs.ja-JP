---
title: MAPI 表示フォルダー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357338"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="6af7e-103">MAPI 表示フォルダー</span><span class="sxs-lookup"><span data-stu-id="6af7e-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="6af7e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6af7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6af7e-105">フォルダーの表示は、関連情報が含まれているルートフォルダーで、個人間メッセージ (IPM) フォルダーの内容の代替の表示レイアウトを定義します。</span><span class="sxs-lookup"><span data-stu-id="6af7e-105">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders.</span></span> <span data-ttu-id="6af7e-106">表示フォルダーは、メッセージストアのルートの下に存在するため、一般的なクライアントアプリケーションでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6af7e-106">View folders reside under the root for the message store and, therefore, are not visible in the typical client application.</span></span> <span data-ttu-id="6af7e-107">すべてのメッセージストアに表示フォルダーが含まれているわけではありません。セッションの既定のメッセージストアとして機能するように構成されたメッセージストアのみを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6af7e-107">Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="6af7e-108">MAPI は、2つの表示フォルダーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6af7e-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="6af7e-109">common: common view フォルダーには、メッセージストアの標準のビューが含まれており、メッセージストアにアクセスするクライアントの任意のユーザーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="6af7e-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="6af7e-110">共通ビューフォルダーのエントリ識別子は、ストアの**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="6af7e-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="6af7e-111">personal —個人用ビューフォルダーには、特定のユーザーによって定義されたビューが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6af7e-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="6af7e-112">MAPI は、個人用ビューフォルダーのエントリ識別子を保持するための**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="6af7e-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="6af7e-113">個人用ビューを使用すると、たとえば1人のユーザーが、メッセージの件名と受信日のみを一覧表示し、送信者によって並べ替えられたメッセージのグループを確認できます。別のユーザーは、日付で並べ替えられた同じグループを調べ、件名、送信者、およびメッセージサイズを一覧表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6af7e-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6af7e-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="6af7e-114">See also</span></span>



<span data-ttu-id="6af7e-115">[MAPI �t�H���_�[](mapi-folders.md)</span><span class="sxs-lookup"><span data-stu-id="6af7e-115">[MAPI Folders](mapi-folders.md)</span></span>

