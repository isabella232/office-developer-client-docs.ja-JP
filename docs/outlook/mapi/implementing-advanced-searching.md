---
title: 実装する高度な検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4430b52b470b89bd7d81922b98b121b3a455768f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800927"
---
# <a name="implementing-advanced-searching"></a><span data-ttu-id="d3d18-103">実装する高度な検索</span><span class="sxs-lookup"><span data-stu-id="d3d18-103">Implementing Advanced Searching</span></span>

  
  
<span data-ttu-id="d3d18-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3d18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3d18-105">いくつかのアドレス帳コンテナーは、クライアントの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 以外のプロパティで検索できるようにする、高度な検索機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3d18-105">Some address book containers support an advanced searching capability that allows clients to search on properties other than **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span> <span data-ttu-id="d3d18-106">高度な検索をサポートするために、プロバイダーは、他のコンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティを通じてアクセスできる特別なコンテナーを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d3d18-106">To support advanced searches, your provider must implement a special container that is accessible through the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property of your other containers.</span></span> <span data-ttu-id="d3d18-107">**PR_SEARCH**を入力し、高度な検索条件を編集するために使用するダイアログ ボックスについて説明する表示のテーブルへのアクセスを提供するコンテナー オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3d18-107">**PR_SEARCH** contains a container object that provides access to a display table that describes the dialog box used to enter and edit the advanced search criteria.</span></span> 
  
 <span data-ttu-id="d3d18-108">**サポートするには、高度な検索**</span><span class="sxs-lookup"><span data-stu-id="d3d18-108">**To support advanced searching**</span></span>
  
1. <span data-ttu-id="d3d18-109">検索条件の各プロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-109">Define a property for each of your search criteria.</span></span>
    
2. <span data-ttu-id="d3d18-110">コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッド内のコードのセクションでは、 **PR_SEARCH**プロパティを処理します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-110">In the section of code in your container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method that handles the **PR_SEARCH** property:</span></span> 
    
1. <span data-ttu-id="d3d18-111">クライアントが**IMAPIContainer**インターフェイスを要求していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d3d18-111">Check that the client is requesting the **IMAPIContainer** interface.</span></span> <span data-ttu-id="d3d18-112">不適切なインターフェイスが要求されている場合は、失敗し、MAPI_E_INTERFACE_NOT_SUPPORTED を返します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-112">If an inappropriate interface is being requested, fail and return MAPI_E_INTERFACE_NOT_SUPPORTED.</span></span> 
    
2. <span data-ttu-id="d3d18-113">**IMAPIContainer**インターフェイスをサポートする新しい検索オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-113">Create a new search object that supports the **IMAPIContainer** interface.</span></span> 
    
3. <span data-ttu-id="d3d18-114">この時点で、コールされます検索コンテナーの**IMAPIProp::OpenProperty**メソッドに、 **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-114">At this point, a call will be made to your search container's **IMAPIProp::OpenProperty** method to retrieve its **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="d3d18-115">プロバイダーは、 [BuildDisplayTable](builddisplaytable.md)コンテナーの高度な検索] ダイアログ ボックスについて説明するを呼び出すことによって通常の表示のテーブルを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3d18-115">Your provider must supply a display table, typically through a call to [BuildDisplayTable](builddisplaytable.md), that describes the container's advanced search dialog box.</span></span>
    
4. <span data-ttu-id="d3d18-116">MAPI では、ユーザーが適切な検索条件を入力できるように、[検索] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-116">MAPI displays the search dialog box, allowing the user to enter the appropriate criteria.</span></span> <span data-ttu-id="d3d18-117">ユーザーが終了すると、MAPI は、検索条件を格納するコンテナーの[IMAPIProp::SetProps](imapiprop-setprops.md)のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d3d18-117">When the user has finished, MAPI calls the container's [IMAPIProp::SetProps](imapiprop-setprops.md) method to store the search criteria.</span></span> 
    
5. <span data-ttu-id="d3d18-118">検索コンテナーのコンテンツ テーブルを要求するための呼び出しを行われます。</span><span class="sxs-lookup"><span data-stu-id="d3d18-118">A call will be made to request your search container's contents table.</span></span> <span data-ttu-id="d3d18-119">内容をテーブルにすると、すべての条件に一致するコンテナー内のエントリにします。</span><span class="sxs-lookup"><span data-stu-id="d3d18-119">Populate the contents table with all of the entries in the container that match the criteria.</span></span>
    

