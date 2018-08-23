---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799635"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="f8799-103">配布リストのメンバーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="f8799-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="f8799-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f8799-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f8799-105">**配布リストのメンバーを取得するには**</span><span class="sxs-lookup"><span data-stu-id="f8799-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="f8799-106">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_DISPLAY_TYPE** ([など、取得するにはメンバーのプロパティを使用してサイズ プロパティ タグ配列を作成します。PidTagDisplayType](pidtagdisplaytype-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="f8799-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="f8799-107">配布リストを開くには、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8799-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="f8799-108">コンテンツ テーブルにアクセスするための配布リストの**IABContainer::GetContentsTable**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8799-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="f8799-109">すべての配布リストのメンバーを表すテーブルの行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f8799-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

