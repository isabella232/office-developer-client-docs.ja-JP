---
title: MAPI オブジェクトとプロパティのアクセス許可
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4efa9cd1596cffe19a19a62059f81fa553343d77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436175"
---
# <a name="permissions-for-mapi-objects-and-properties"></a><span data-ttu-id="88c1c-103">MAPI オブジェクトとプロパティのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="88c1c-103">Permissions for MAPI Objects and Properties</span></span>

  
  
<span data-ttu-id="88c1c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88c1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88c1c-105">アクセス許可、または一連の許可可能な操作は、MAPI オブジェクトの特性であり、それらのオブジェクトでサポートされる個々のプロパティの特性になります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-105">Access permission, or the set of permissable operations, can be a characteristic of MAPI objects and of individual properties supported by those objects.</span></span> <span data-ttu-id="88c1c-106">オブジェクト アクセスは、オブジェクトの親によって決まります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-106">Object access is determined by an object's parent.</span></span> <span data-ttu-id="88c1c-107">メッセージの場合、そのフォルダーはアクセス許可を決定します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-107">For a message, its folder determines access permissions.</span></span> <span data-ttu-id="88c1c-108">メッセージング ユーザーまたは配布リストの場合、そのアドレス帳コンテナーは、この決定を行います。</span><span class="sxs-lookup"><span data-stu-id="88c1c-108">For a messaging user or distribution list, its address book container makes this determination.</span></span> <span data-ttu-id="88c1c-109">メッセージなどのオブジェクトが 2 つのフォルダーに存在する場合、オブジェクトの 2 つのコピーのアクセス許可は異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-109">When an object such as a message resides in two folders, the permissions for the two copies of the object can be different.</span></span> 
  
<span data-ttu-id="88c1c-110">これらのオブジェクトを使用するクライアントは [、IMAPISession::OpenEntry](imapisession-openentry.md) 呼び出しで MAPI_BEST_ACCESS フラグを設定することで、オブジェクトに対して許可される最高レベルのアクセスを要求できます。</span><span class="sxs-lookup"><span data-stu-id="88c1c-110">Clients using these objects can request the highest level of access permitted for the object by setting the MAPI_BEST_ACCESS flag on the [IMAPISession::OpenEntry](imapisession-openentry.md) call.</span></span> <span data-ttu-id="88c1c-111">オブジェクトを実装するサービス プロバイダーによっては、クライアントに必要なアクセス レベルが付与される場合と許可されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-111">Depending on the service provider implementing the object, the client may or may not be granted the level of access necessary.</span></span> <span data-ttu-id="88c1c-112">クライアントは、オブジェクト GetProps メソッドを呼び出して、オブジェクト [(PidTagAccess)](pidtagaccess-canonical-property.md)プロパティを取得することで、付与 **された** アクセスのレベルPR_ACCESS決定できます。 </span><span class="sxs-lookup"><span data-stu-id="88c1c-112">Clients can determine the level of access that they were granted by calling the object **GetProps** method to retrieve the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property.</span></span> <span data-ttu-id="88c1c-113">ただし、サービス プロバイダーは、このプロパティの値を動的に生成する必要があるため、クライアントは必要な場合にのみ取得をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88c1c-113">However, because the service provider must dynamically generate the value for this property, it is recommended that clients retrieve it only when necessary.</span></span> 
  
<span data-ttu-id="88c1c-114">フォルダー、アドレス帳コンテナー、配布リストなどのコンテナーで変更を許可するかどうかを確認するには **、GetProps** メソッドを呼び出して PR_ACCESS_LEVEL ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティ **を** 取得します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-114">To determine whether a container such as a folder, address book container, or distribution list allows modification, call its **GetProps** method to retrieve the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span> <span data-ttu-id="88c1c-115">コンテナー レベルのアクセスは、ユーザー インターフェイスの表示方法に関してクライアントに影響します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-115">Container level access affects clients in terms of how they display their user interfaces.</span></span> <span data-ttu-id="88c1c-116">また、ユーザー インターフェイスの表示と一般的な実装の観点から、コンテナー内のオブジェクトの実装者にも影響します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-116">It also impacts the implementers of objects within containers in terms of their user interface display and their general implementation.</span></span> 
  
<span data-ttu-id="88c1c-117">特定のプロパティへのアクセスは、プロパティを所有するオブジェクトに対して MAPI によって設定されたプロパティ スキーマによって決まります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-117">Access to a particular property is determined by the property schema set up by MAPI for the object that owns the property.</span></span> <span data-ttu-id="88c1c-118">プロパティ スキーマは、オブジェクトの必須プロパティとオプション プロパティのセットとそのアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-118">Property schemas specify the set of required and optional properties for an object and their access permission.</span></span> <span data-ttu-id="88c1c-119">オブジェクトの親によって決定されるオブジェクト アクセスとは異なり、プロパティ アクセスはグローバルです。</span><span class="sxs-lookup"><span data-stu-id="88c1c-119">Unlike object access which is determined by the object's parent, property access is global.</span></span> <span data-ttu-id="88c1c-120">すべてのオブジェクトは、オブジェクトの親のアクセス要件に関係なく、スキーマによって決定されるのと同じプロパティのアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="88c1c-120">Every object, regardless of the access requirements of the object's parent, has the same permissions for the property as determined by the schema.</span></span>
  
<span data-ttu-id="88c1c-121">プロパティが読み取り専用の場合 **、GetProps** または **OpenProperty** 呼び出しで常に使用できます。</span><span class="sxs-lookup"><span data-stu-id="88c1c-121">When a property is read-only, it will always be available with a **GetProps** or **OpenProperty** call.</span></span> <span data-ttu-id="88c1c-122">ただし、プロパティをサポートするオブジェクトの実装によっては、プロパティを変更するための **SetProps** メソッドと、プロパティを削除するための **DeleteProps** メソッドの 2 つの結果があります。</span><span class="sxs-lookup"><span data-stu-id="88c1c-122">However, depending on the implementation of the object supporting the property, there are two possible outcomes for the **SetProps** method for modifying a property and the **DeleteProps** method for removing it:</span></span> 
  
- <span data-ttu-id="88c1c-123">失敗して、エラーを返MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="88c1c-123">Fail and return MAPI_E_NO_ACCESS</span></span>
    
- <span data-ttu-id="88c1c-124">アクションを実行しないで成功する</span><span class="sxs-lookup"><span data-stu-id="88c1c-124">Succeed with no action taken</span></span>
    
<span data-ttu-id="88c1c-125">プロパティおよびオブジェクト アクセスは **、IMAPIProp** インターフェイスから継承する [IPropData](ipropdataimapiprop.md)インターフェイスを使用して取得または設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="88c1c-125">Property and object access can also be retrieved or set by using the [IPropData](ipropdataimapiprop.md) interface that inherits from the **IMAPIProp** interface.</span></span> <span data-ttu-id="88c1c-126">MAPI は、メモリ内 **のデータに基づく IPropData** の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="88c1c-126">MAPI provides an implementation of **IPropData** that is based on data in memory.</span></span> <span data-ttu-id="88c1c-127">サービス プロバイダーは **、IPropData** を使用して、ステータス オブジェクトや組み込みのトランザクションを持つデータベースを使用している場合など、特定の状況で **IMAPIProp** を実装できます。</span><span class="sxs-lookup"><span data-stu-id="88c1c-127">Service providers can use **IPropData** to implement **IMAPIProp** in certain circumstances, such as for their status object or if they are using a database that does not have built-in transactions.</span></span> <span data-ttu-id="88c1c-128">**IPropData は** メモリ内で排他的に動作し、データのロックとロック解除を不要にしています。</span><span class="sxs-lookup"><span data-stu-id="88c1c-128">**IPropData** works exclusively in memory, making it unnecessary to lock and unlock data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88c1c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="88c1c-129">See also</span></span>



[<span data-ttu-id="88c1c-130">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="88c1c-130">MAPI Property Overview</span></span>](mapi-property-overview.md)

