---
title: メッセージ ストア プロバイダーでの検索のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573195"
---
# <a name="supporting-searches-in-message-store-providers"></a><span data-ttu-id="72a8f-103">メッセージ ストア プロバイダーでの検索のサポート</span><span class="sxs-lookup"><span data-stu-id="72a8f-103">Supporting Searches in Message Store Providers</span></span>

  
  
<span data-ttu-id="72a8f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72a8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72a8f-105">クライアント アプリケーションでは、メッセージ ・ ストア内のメッセージを検索するのには熱心なユーザー インターフェイス コンポーネントがいくつかが頻繁にあります。</span><span class="sxs-lookup"><span data-stu-id="72a8f-105">Client applications frequently have some user interface components devoted to searching for messages in a message store.</span></span> <span data-ttu-id="72a8f-106">検索条件が指定の[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) 、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)および[IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md)メソッドを使用してインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="72a8f-106">Search criteria are specified in the [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) interface by means of the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) and [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) methods.</span></span> 
  
<span data-ttu-id="72a8f-107">クライアントは、検索結果のフォルダーを含むメッセージ ストアのルート フォルダーを識別するのには、メッセージ ストア オブジェクトの**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) のプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="72a8f-107">Clients use the message store object's **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to identify the root folder in the message store that contains folders for search results.</span></span> <span data-ttu-id="72a8f-108">検索結果フォルダーは、多くの場合、IPM のフォルダー ツリーの一部ではないと、そのため、非表示になっているメッセージ ストアの最上部にあるフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="72a8f-108">The search-results folder is often a folder at the top level of the message store that is not part of the IPM folder tree and is, therefore, hidden.</span></span>
  
<span data-ttu-id="72a8f-109">メッセージ ストア プロバイダーが検索結果の永続的なフォルダーを使用して、またはクライアントを開くと、 **PR_FINDER_ENTRYID**プロパティに格納されているエントリの識別子を作成するかどうかは、実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="72a8f-109">Whether your message store provider uses a permanent search-results folder or creates one when a client opens the entry identifier stored in the **PR_FINDER_ENTRYID** property is an implementation detail.</span></span> <span data-ttu-id="72a8f-110">エントリの識別子を作成するかどうかを確認するのには任意のフォルダーを開くたびにチェックの問題を避けることができますので、メッセージ ストアを作成するときに作成される永続的なフォルダーを使用するのには、メッセージ ストア プロバイダーをいくらか簡単には、検索結果のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="72a8f-110">It is somewhat easier for your message store provider to use a permanent folder that is created when the message store is created, because doing so avoids the complication of checking the entry identifier whenever any folder is opened to see whether to create a search-results folder.</span></span> <span data-ttu-id="72a8f-111">ただし、すべてのメッセージ ストア プロバイダーが行うことです。特に、読み取り専用のメッセージ ストアまたは多くの場合、従来のデータベースに MAPI インターフェイスを提供するストアは許可されていませんか、基になるストレージ機構で検索結果の永続的なフォルダーを作成することができません。</span><span class="sxs-lookup"><span data-stu-id="72a8f-111">However, not all message store providers can do that; notably, read-only message stores or stores that provide a MAPI interface to a legacy database often are not allowed or are unable to create a permanent search-results folder in the underlying storage mechanism.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72a8f-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="72a8f-112">See also</span></span>



<span data-ttu-id="72a8f-113">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="72a8f-113">[Message Store Features](message-store-features.md)</span></span>

