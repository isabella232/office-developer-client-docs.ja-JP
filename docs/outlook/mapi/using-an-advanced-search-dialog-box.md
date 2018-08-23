---
title: '[高度な検索] ダイアログ ボックスの使用'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588770"
---
# <a name="using-an-advanced-search-dialog-box"></a><span data-ttu-id="c4417-103">[高度な検索] ダイアログ ボックスの使用</span><span class="sxs-lookup"><span data-stu-id="c4417-103">Using an Advanced Search Dialog Box</span></span>

  
  
<span data-ttu-id="c4417-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4417-105">いくつかのアドレス帳コンテナーは、クライアントの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 以外のプロパティで検索できるようにする、高度な検索機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c4417-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="c4417-106">高度な検索をサポートしているアドレス帳コンテナーには、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) と呼ばれるコンテナー オブジェクト プロパティが設定されています。</span><span class="sxs-lookup"><span data-stu-id="c4417-106">Address book containers that support advanced searches have a container object property called **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span></span> <span data-ttu-id="c4417-107">このコンテナー オブジェクトは、[検索] ダイアログ ボックスを説明する表示のテーブルへのアクセスを提供: ダイアログ ボックスを入力し、高度な検索条件を編集するために使用します。</span><span class="sxs-lookup"><span data-stu-id="c4417-107">This container object provides access to a display table that describes the search dialog box — a dialog box used to enter and edit the advanced search criteria.</span></span>
  
 <span data-ttu-id="c4417-108">**アドレス帳コンテナーの高度な検索を実行するには**</span><span class="sxs-lookup"><span data-stu-id="c4417-108">**To perform an advanced search on an address book container**</span></span>
  
1. <span data-ttu-id="c4417-109">インターフェイス識別子のプロパティ タグと IID_IMAPIContainer の**PR_SEARCH**を指定するコンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4417-109">Call the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, specifying **PR_SEARCH** for the property tag and IID_IMAPIContainer for the interface identifier.</span></span> 
    
2. <span data-ttu-id="c4417-110">インターフェイス識別子のプロパティ タグと IID_IMAPITable の**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) を指定する、検索オブジェクトの**IMAPIProp::OpenProperty**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4417-110">Call the search object 's **IMAPIProp::OpenProperty** method, specifying **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> 
    
3. <span data-ttu-id="c4417-111">高度な検索で使用するプロパティの値を確立するための検索オブジェクトの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4417-111">Call the search object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to establish values for the properties to be used in the advanced search.</span></span> 
    
4. <span data-ttu-id="c4417-112">高度な検索条件を保存するのには、検索オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4417-112">Call the search object's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save the advanced search criteria.</span></span> 
    
<span data-ttu-id="c4417-113">この一連の呼び出しは、クライアントが検索オブジェクトの**GetSearchCriteria**メソッドを呼び出すときに使用される制限の中で発生します。</span><span class="sxs-lookup"><span data-stu-id="c4417-113">This sequence of calls results in a restriction being available when a client calls the search object's **GetSearchCriteria** method.</span></span> 
  

