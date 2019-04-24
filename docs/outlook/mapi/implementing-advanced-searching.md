---
title: 高度な検索の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332817"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="5e95d-103">高度な検索の実装</span><span class="sxs-lookup"><span data-stu-id="5e95d-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="5e95d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e95d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e95d-105">アドレス帳のコンテナーには、クライアントが**PR_DISPLAY_NAME**以外のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を検索できる高度な検索機能をサポートしているものがあります。</span><span class="sxs-lookup"><span data-stu-id="5e95d-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="5e95d-106">高度な検索をサポートするには、プロバイダーが他のコンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティを通じてアクセスできる特別なコンテナーを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e95d-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="5e95d-107">**PR_SEARCH**には、高度な検索条件を入力および編集するために使用するダイアログボックスについて説明する表示テーブルへのアクセスを提供する container オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e95d-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="5e95d-108">**高度な検索をサポートするには**</span><span class="sxs-lookup"><span data-stu-id="5e95d-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="5e95d-109">各検索基準のプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="5e95d-110">コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドの、 **PR_SEARCH**プロパティを処理するコードセクションで、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="5e95d-111">クライアントが**IMAPIContainer**インターフェイスを要求していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="5e95d-112">不適切なインターフェイスが要求されている場合は、エラーが発生し、MAPI_E_INTERFACE_NOT_SUPPORTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="5e95d-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="5e95d-113">**IMAPIContainer**インターフェイスをサポートする新しい検索オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="5e95d-114">この時点で、検索コンテナーの**imapiprop:: openproperty**メソッドが**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを取得するための呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="5e95d-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="5e95d-115">プロバイダーでは、通常、コンテナーの [高度な検索] ダイアログボックスを記述する[builddisplaytable](builddisplaytable.md)を呼び出すことによって、表示テーブルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e95d-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="5e95d-116">MAPI [検索] ダイアログボックスを表示し、ユーザーが適切な条件を入力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5e95d-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="5e95d-117">ユーザーが完了すると、MAPI はコンテナーの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、検索条件を格納します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="5e95d-118">検索コンテナーの contents テーブルを要求する呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="5e95d-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="5e95d-119">コンテンツテーブルに、条件に一致するコンテナー内のすべてのエントリを設定します。</span><span class="sxs-lookup"><span data-stu-id="5e95d-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

