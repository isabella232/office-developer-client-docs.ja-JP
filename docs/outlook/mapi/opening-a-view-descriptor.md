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
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="db72b-103">ビュー記述子を開く</span><span class="sxs-lookup"><span data-stu-id="db72b-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="db72b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db72b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db72b-105">通常のビュー、既定のビュー、または任意の数の個人用ビューを使用して、多くのフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="db72b-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="db72b-106">ビューは、フォルダーの内容を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="db72b-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="db72b-107">標準表示モードは、代替ビューがない場合、またはフォルダーを初めて開いたときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="db72b-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="db72b-108">代替ビューが存在する場合は、それを使用してフォルダーを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="db72b-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="db72b-109">ビューは、ビュー記述子と呼ばれるメッセージで記述されます。</span><span class="sxs-lookup"><span data-stu-id="db72b-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="db72b-110">通常は、関連付けられたメッセージとして作成され、[共通] または [個人用ビュー] フォルダーまたは任意の IPM フォルダーに表示することができます。</span><span class="sxs-lookup"><span data-stu-id="db72b-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="db72b-111">ビュー記述子を開くには</span><span class="sxs-lookup"><span data-stu-id="db72b-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="db72b-112">[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)を呼び出して、フォルダーの関連付けられたコンテンツテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="db72b-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="db72b-113">ビュー記述子に予約されたメッセージクラスを持つメッセージのみを特定する制限[](imapitable-restrict.md)を作成し、次のように、適切な行を取得するには、テーブルと imapitable:: [QueryRows](imapitable-queryrows.md)を制限します。</span><span class="sxs-lookup"><span data-stu-id="db72b-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="db72b-114">フォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、その**PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="db72b-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="db72b-115">**PR_DEFAULT_VIEW_ENTRYID**には、フォルダーの既定のビュー記述子を含むメッセージのエントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="db72b-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="db72b-116">フォルダーが[imapifolder:: CreateMessage](imapifolder-createmessage.md)および[IMAPIContainer:: getcontentstable](imapicontainer-getcontentstable.md)への呼び出しで MAPI_ASSOCIATED フラグの使用をサポートしている場合、この呼び出しは成功します。</span><span class="sxs-lookup"><span data-stu-id="db72b-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="db72b-117">を開くには、 [IMsgStore:: openentry](imsgstore-openentry.md)という名前のビュー記述子のエントリ識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="db72b-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

