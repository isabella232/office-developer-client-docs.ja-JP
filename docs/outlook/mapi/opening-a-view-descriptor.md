---
title: ビュー記述子を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413039"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="139fd-103">ビュー記述子を開く</span><span class="sxs-lookup"><span data-stu-id="139fd-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="139fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="139fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="139fd-105">多くのフォルダーは、通常のビュー、既定のビュー、または任意の数のカスタマイズされたビューで開く場合があります。</span><span class="sxs-lookup"><span data-stu-id="139fd-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="139fd-106">ビューでは、フォルダーの内容を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="139fd-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="139fd-107">通常のビューは、代替ビューがない場合や、フォルダーを初めて開く場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="139fd-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="139fd-108">別のビューが存在する場合は、そのビューを使用してフォルダーを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="139fd-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="139fd-109">ビューは、ビュー記述子と呼ばれるメッセージで説明されます。</span><span class="sxs-lookup"><span data-stu-id="139fd-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="139fd-110">ビュー記述子は通常、関連付けられたメッセージとして作成され、共通または個人用のビュー フォルダーまたは任意の IPM フォルダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="139fd-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="139fd-111">ビュー記述子を開く方法</span><span class="sxs-lookup"><span data-stu-id="139fd-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="139fd-112">[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出して、フォルダーに関連付けられたコンテンツ テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="139fd-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="139fd-113">ビュー記述子用に予約されているメッセージ クラスを含むメッセージのみを検索する制限を作成し [、IMAPITable::Restrict](imapitable-restrict.md) を呼び出してテーブルを制限し [、IMAPITable::QueryRows](imapitable-queryrows.md) を使用して適切な行を取得します。</span><span class="sxs-lookup"><span data-stu-id="139fd-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="139fd-114">フォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_DEFAULT_VIEW_ENTRYID **(** [PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="139fd-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="139fd-115">**PR_DEFAULT_VIEW_ENTRYID** には、フォルダーの既定のビュー記述子を含むメッセージのエントリ識別子が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="139fd-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="139fd-116">この呼び出しは、フォルダーが [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) と [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)の呼び出しで MAPI_ASSOCIATED フラグの使用をサポートしている場合に成功します。</span><span class="sxs-lookup"><span data-stu-id="139fd-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="139fd-117">ビュー [記述子のエントリ識別子を使用して IMsgStore::OpenEntry](imsgstore-openentry.md) を呼び出して開きます。</span><span class="sxs-lookup"><span data-stu-id="139fd-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

