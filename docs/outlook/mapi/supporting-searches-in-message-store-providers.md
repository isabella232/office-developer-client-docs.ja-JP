---
title: メッセージストアプロバイダーでの検索のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349589"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="4fa49-103">メッセージストアプロバイダーでの検索のサポート</span><span class="sxs-lookup"><span data-stu-id="4fa49-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="4fa49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa49-105">多くの場合、クライアントアプリケーションには、メッセージストア内のメッセージを検索するために使用されるユーザーインターフェイスコンポーネントがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="4fa49-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="4fa49-106">検索条件は、 [IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドと[IMAPIContainer:: getsearchcriteria](imapicontainer-getsearchcriteria.md)メソッドを使って、 [IMAPIContainer: imapiprop](imapicontainerimapiprop.md)インターフェイスで指定します。</span><span class="sxs-lookup"><span data-stu-id="4fa49-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="4fa49-107">クライアントは、メッセージストアオブジェクトの**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) プロパティを使用して、検索結果のフォルダーが格納されているメッセージストア内のルートフォルダーを特定します。</span><span class="sxs-lookup"><span data-stu-id="4fa49-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="4fa49-108">検索結果フォルダーは、多くの場合、メッセージストアの最上位レベルにあるフォルダーで、IPM フォルダーツリーには含まれていないため、非表示になります。</span><span class="sxs-lookup"><span data-stu-id="4fa49-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="4fa49-109">メッセージストアプロバイダーが永続的な検索結果フォルダーを使用するか、クライアントが開くときに1つを作成するかどうかは、 **PR_FINDER_ENTRYID**プロパティに格納されているエントリ識別子が実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="4fa49-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="4fa49-110">メッセージストアプロバイダーでは、メッセージストアの作成時に作成されたパーマネントフォルダーを使用する方が簡単です。これにより、フォルダーが開かれるたびにエントリ識別子をチェックして、を作成するかどうかを確認するのが困難になります。検索結果フォルダー。</span><span class="sxs-lookup"><span data-stu-id="4fa49-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="4fa49-111">ただし、すべてのメッセージストアプロバイダーがこれを実行できるわけではありません。特に、従来のデータベースに MAPI インターフェイスを提供する読み取り専用のメッセージストアまたはストアは、基礎となるストレージメカニズムでは、通常は許可されていないか、または永続的な検索結果フォルダーを作成できません。</span><span class="sxs-lookup"><span data-stu-id="4fa49-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4fa49-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fa49-112">See also</span></span>



<span data-ttu-id="4fa49-113">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="4fa49-113">[Message Store Features](message-store-features.md)</span></span>

