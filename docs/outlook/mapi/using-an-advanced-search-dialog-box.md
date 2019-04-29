---
title: '[高度な検索] ダイアログボックスを使用する'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437302"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="4423a-103">[高度な検索] ダイアログボックスを使用する</span><span class="sxs-lookup"><span data-stu-id="4423a-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="4423a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4423a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4423a-105">アドレス帳のコンテナーには、クライアントが**PR_DISPLAY_NAME**以外のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を検索できる高度な検索機能をサポートしているものがあります。</span><span class="sxs-lookup"><span data-stu-id="4423a-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="4423a-106">高度な検索をサポートするアドレス帳コンテナーには、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) という名前のコンテナーオブジェクトプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="4423a-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="4423a-107">この container オブジェクトは、[検索] ダイアログボックスについて説明する表示テーブルへのアクセスを提供します。このダイアログボックスは、高度な検索条件を入力および編集するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4423a-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="4423a-108">**アドレス帳コンテナーに対して高度な検索を実行するには**</span><span class="sxs-lookup"><span data-stu-id="4423a-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="4423a-109">コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出し、プロパティタグと IID_IMAPIContainer のインターフェイス識別子に**PR_SEARCH**を指定します。</span><span class="sxs-lookup"><span data-stu-id="4423a-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="4423a-110">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) をプロパティタグと IID_IMAPITable のインターフェイス識別子に指定して、search オブジェクトの**imapiprop:: openproperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4423a-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="4423a-111">検索オブジェクトの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、高度な検索で使用されるプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="4423a-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="4423a-112">検索オブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、高度な検索条件を保存します。</span><span class="sxs-lookup"><span data-stu-id="4423a-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="4423a-113">この一連の呼び出しでは、クライアントが search オブジェクトの**getsearchcriteria**メソッドを呼び出すときに、制限が有効になります。</span><span class="sxs-lookup"><span data-stu-id="4423a-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

