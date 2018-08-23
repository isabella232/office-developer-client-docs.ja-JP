---
title: ビュー記述子を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 525c817cfc3bdcf96455d35025e85486ec8b5b42
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801682"
---
# <a name="opening-a-view-descriptor"></a><span data-ttu-id="93fd3-103">ビュー記述子を開く</span><span class="sxs-lookup"><span data-stu-id="93fd3-103">Opening a view descriptor</span></span>
  
<span data-ttu-id="93fd3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93fd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93fd3-105">標準表示モード、既定のビューまたは個人用ビューの任意の数に多くのフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="93fd3-105">Many folders can be opened with a normal view, a default view, or any number of personalized views.</span></span> <span data-ttu-id="93fd3-106">ビューでは、フォルダーの内容を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="93fd3-106">A view describes how to display the contents of a folder.</span></span> <span data-ttu-id="93fd3-107">標準のビューは、別のビューがない場合に、最初にフォルダーを開くときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93fd3-107">The normal view is used when there is no alternative view and when you are opening the folder for the first time.</span></span> <span data-ttu-id="93fd3-108">代替ビューが存在する場合は、フォルダーを開くに使用してください。</span><span class="sxs-lookup"><span data-stu-id="93fd3-108">When an alternative view does exist, you must use it to open the folder.</span></span>
  
<span data-ttu-id="93fd3-109">ビューは、ビュー記述子と呼ばれるメッセージの説明です。</span><span class="sxs-lookup"><span data-stu-id="93fd3-109">A view is described in a message known as a view descriptor.</span></span> <span data-ttu-id="93fd3-110">ビュー記述子では、通常、関連付けられているメッセージとして作成し、[共通] または [個人用のビュー フォルダーまたは IPM の任意のフォルダー内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="93fd3-110">View descriptors are typically created as associated messages and can appear in either the common or personal view folders or in any IPM folder.</span></span>
  
### <a name="to-open-a-view-descriptor"></a><span data-ttu-id="93fd3-111">ビュー記述子を開く</span><span class="sxs-lookup"><span data-stu-id="93fd3-111">To open a view descriptor</span></span>
  
1. <span data-ttu-id="93fd3-112">フォルダーの内容を関連するテーブルを取得するために[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93fd3-112">Call [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) to retrieve the associated contents table for the folder.</span></span> 
    
2. <span data-ttu-id="93fd3-113">ビュー記述子用に予約されたメッセージ クラスのメッセージだけを検索する制限を作成し、テーブルを制限する[IMAPITable::Restrict](imapitable-restrict.md)と、適切な行を取得するために[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出すか、.</span><span class="sxs-lookup"><span data-stu-id="93fd3-113">Create a restriction that locates only messages with the message class reserved for view descriptors and call [IMAPITable::Restrict](imapitable-restrict.md) to limit the table and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the appropriate rows, or...</span></span>
    
   <span data-ttu-id="93fd3-114">**PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) のプロパティを取得するために、フォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93fd3-114">Call the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="93fd3-115">**PR_DEFAULT_VIEW_ENTRYID**には、フォルダーの既定のビューの記述子が含まれるメッセージのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="93fd3-115">**PR_DEFAULT_VIEW_ENTRYID** contains the entry identifier for the message containing the default view descriptor for a folder.</span></span> <span data-ttu-id="93fd3-116">フォルダーは、 [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)および[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)への呼び出しに MAPI_ASSOCIATED フラグの使用をサポートしている場合、この呼び出しは成功します。</span><span class="sxs-lookup"><span data-stu-id="93fd3-116">This call will succeed if the folder supports the use of the MAPI_ASSOCIATED flag on calls to [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) and [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).</span></span>
    
3. <span data-ttu-id="93fd3-117">開くビュー記述子のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93fd3-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with the entry identifier of the view descriptor to open it.</span></span> 
    

