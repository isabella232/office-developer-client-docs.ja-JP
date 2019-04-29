---
title: 配布リストのメンバーへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412388"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="db7bd-103">配布リストのメンバーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="db7bd-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="db7bd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db7bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="db7bd-105">**配布リストのメンバーを取得するには**</span><span class="sxs-lookup"><span data-stu-id="db7bd-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="db7bd-106">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))、 **PR_DISPLAY_TYPE**など、取得するメンバーのプロパティを使用して、サイズが変更されたプロパティタグ配列を作成します ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="db7bd-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="db7bd-107">[IAddrBook:: openentry](iaddrbook-openentry.md)を呼び出して、配布リストを開きます。</span><span class="sxs-lookup"><span data-stu-id="db7bd-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="db7bd-108">配布リストの**IABContainer:: getcontentstable**メソッドを呼び出して、そのコンテンツテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="db7bd-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="db7bd-109">[hrqueryallrows](hrqueryallrows.md)を呼び出して、配布リストのメンバーを表すすべてのテーブルの行を取得します。</span><span class="sxs-lookup"><span data-stu-id="db7bd-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

