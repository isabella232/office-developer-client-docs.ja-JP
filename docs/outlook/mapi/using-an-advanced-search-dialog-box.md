---
title: '[高度な検索] ダイアログ ボックスの使用'
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
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="b3733-103">[高度な検索] ダイアログ ボックスの使用</span><span class="sxs-lookup"><span data-stu-id="b3733-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="b3733-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3733-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3733-105">一部のアドレス帳コンテナーは高度な検索機能をサポートしています。これにより、クライアントは、ユーザー以外のプロパティ[(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)をPR_DISPLAY_NAME検索できます。</span><span class="sxs-lookup"><span data-stu-id="b3733-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="b3733-106">高度な検索をサポートするアドレス帳コンテナーには、PR_SEARCH ([PidTagSearch](pidtagsearch-canonical-property.md)) というコンテナー **オブジェクト プロパティ** があります。</span><span class="sxs-lookup"><span data-stu-id="b3733-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="b3733-107">このコンテナー オブジェクトは、検索ダイアログ ボックス (高度な検索条件の入力と編集に使用されるダイアログ ボックス) を説明する表示テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3733-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="b3733-108">**アドレス帳コンテナーで高度な検索を実行するには**</span><span class="sxs-lookup"><span data-stu-id="b3733-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="b3733-109">コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出し、プロパティ **タグ** PR_SEARCHインターフェイス識別子のIID_IMAPIContainerを指定します。</span><span class="sxs-lookup"><span data-stu-id="b3733-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="b3733-110">プロパティ タグの PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) とインターフェイス識別子の **IID_IMAPITable** を指定して、検索オブジェクトの **IMAPIProp::OpenProperty** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3733-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="b3733-111">検索オブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、高度な検索で使用するプロパティの値を確立します。</span><span class="sxs-lookup"><span data-stu-id="b3733-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="b3733-112">高度な検索条件を保存するには、検索オブジェクトの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b3733-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="b3733-113">この一連の呼び出しは、クライアントが検索オブジェクトの **GetSearchCriteria** メソッドを呼び出す際に使用できる制限になります。</span><span class="sxs-lookup"><span data-stu-id="b3733-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

