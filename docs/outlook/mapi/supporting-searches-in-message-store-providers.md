---
title: メッセージ ストア プロバイダーでの検索のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425387"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="c5bb4-103">メッセージ ストア プロバイダーでの検索のサポート</span><span class="sxs-lookup"><span data-stu-id="c5bb4-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="c5bb4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5bb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5bb4-105">クライアント アプリケーションには、多くの場合、メッセージ ストア内のメッセージの検索に専念するユーザー インターフェイス コンポーネントがいくつか含まれます。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="c5bb4-106">検索基準は [、IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) インターフェイスで [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドと [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) メソッドによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="c5bb4-107">クライアントは、メッセージ ストア オブジェクトの **PR_FINDER_ENTRYID** ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)プロパティを使用して、検索結果のフォルダーを含むメッセージ ストア内のルート フォルダーを識別します。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="c5bb4-108">検索結果フォルダーは、多くの場合、IPM フォルダー ツリーの一部ではなく、非表示のメッセージ ストアのトップ レベルにあるフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="c5bb4-109">メッセージ ストア プロバイダーが永続的な検索結果フォルダーを使用するか、クライアントが PR_FINDER_ENTRYID プロパティに格納されているエントリ識別子を開く際 **に作成するかどうかは、実装** の詳細です。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="c5bb4-110">メッセージ ストア プロバイダーは、メッセージ ストアの作成時に作成される永続的なフォルダーを使用する方がやや簡単です。そのため、フォルダーを開くたびにエントリ識別子を確認して検索結果フォルダーを作成するかどうかを確認する複雑な問題が回避されます。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="c5bb4-111">ただし、すべてのメッセージ ストア プロバイダーがこれを実行できるわけではありません。特に、従来のデータベースに MAPI インターフェイスを提供する読み取り専用のメッセージ ストアまたはストアは、多くの場合、許可されないか、基になるストレージ メカニズムに永続的な検索結果フォルダーを作成できません。</span><span class="sxs-lookup"><span data-stu-id="c5bb4-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5bb4-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5bb4-112">See also</span></span>



<span data-ttu-id="c5bb4-113">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="c5bb4-113">[Message Store Features](message-store-features.md)</span></span>

