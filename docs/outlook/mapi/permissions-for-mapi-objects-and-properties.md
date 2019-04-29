---
title: MAPI のオブジェクトおよびプロパティのアクセス許可
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
# <a name="permissions-for-mapi-objects-and-properties"></a><span data-ttu-id="71b4e-103">MAPI のオブジェクトおよびプロパティのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="71b4e-103">Permissions for MAPI Objects and Properties</span></span>

  
  
<span data-ttu-id="71b4e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71b4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71b4e-105">アクセス許可、または permissable 操作のセットは、MAPI オブジェクトと、それらのオブジェクトによってサポートされる個々のプロパティの特性になることがあります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-105">Access permission, or the set of permissable operations, can be a characteristic of MAPI objects and of individual properties supported by those objects.</span></span> <span data-ttu-id="71b4e-106">オブジェクトアクセスは、オブジェクトの親によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-106">Object access is determined by an object's parent.</span></span> <span data-ttu-id="71b4e-107">メッセージの場合、フォルダーはアクセス許可を決定します。</span><span class="sxs-lookup"><span data-stu-id="71b4e-107">For a message, its folder determines access permissions.</span></span> <span data-ttu-id="71b4e-108">メッセージングユーザーまたは配布リストのアドレス帳コンテナーは、この判断を行います。</span><span class="sxs-lookup"><span data-stu-id="71b4e-108">For a messaging user or distribution list, its address book container makes this determination.</span></span> <span data-ttu-id="71b4e-109">メッセージなどのオブジェクトが2つのフォルダーに存在する場合、そのオブジェクトの2つのコピーに対するアクセス許可が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-109">When an object such as a message resides in two folders, the permissions for the two copies of the object can be different.</span></span> 
  
<span data-ttu-id="71b4e-110">これらのオブジェクトを使用しているクライアントは、 [imapisession:: openentry](imapisession-openentry.md)呼び出しで MAPI_BEST_ACCESS フラグを設定することにより、オブジェクトに対して許可されている最高レベルのアクセス権を要求できます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-110">Clients using these objects can request the highest level of access permitted for the object by setting the MAPI_BEST_ACCESS flag on the [IMAPISession::OpenEntry](imapisession-openentry.md) call.</span></span> <span data-ttu-id="71b4e-111">オブジェクトを実装するサービスプロバイダーによっては、クライアントに必要なアクセス許可レベルが付与されていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-111">Depending on the service provider implementing the object, the client may or may not be granted the level of access necessary.</span></span> <span data-ttu-id="71b4e-112">クライアントは、オブジェクトの**GetProps**メソッドを呼び出して**PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティを取得することによって、付与されたアクセスのレベルを判断できます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-112">Clients can determine the level of access that they were granted by calling the object **GetProps** method to retrieve the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property.</span></span> <span data-ttu-id="71b4e-113">ただし、サービスプロバイダーはこのプロパティの値を動的に生成する必要があるため、クライアントは必要な場合にのみ取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="71b4e-113">However, because the service provider must dynamically generate the value for this property, it is recommended that clients retrieve it only when necessary.</span></span> 
  
<span data-ttu-id="71b4e-114">フォルダー、アドレス帳コンテナー、配布リストなどのコンテナーが変更できるかどうかを確認するには、 **GetProps**メソッドを呼び出して**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="71b4e-114">To determine whether a container such as a folder, address book container, or distribution list allows modification, call its **GetProps** method to retrieve the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span> <span data-ttu-id="71b4e-115">コンテナーレベルのアクセスは、クライアントがユーザーインターフェイスを表示する方法に基づいて影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-115">Container level access affects clients in terms of how they display their user interfaces.</span></span> <span data-ttu-id="71b4e-116">また、コンテナー内のオブジェクトの実装には、ユーザーインターフェイスの表示とその一般的な実装の観点からも影響します。</span><span class="sxs-lookup"><span data-stu-id="71b4e-116">It also impacts the implementers of objects within containers in terms of their user interface display and their general implementation.</span></span> 
  
<span data-ttu-id="71b4e-117">特定のプロパティへのアクセスは、プロパティを所有するオブジェクトの MAPI によって設定されたプロパティスキーマによって決まります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-117">Access to a particular property is determined by the property schema set up by MAPI for the object that owns the property.</span></span> <span data-ttu-id="71b4e-118">プロパティスキーマは、オブジェクトの必須およびオプションのプロパティのセットとそのアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="71b4e-118">Property schemas specify the set of required and optional properties for an object and their access permission.</span></span> <span data-ttu-id="71b4e-119">オブジェクトの親によって決定されるオブジェクトアクセスとは異なり、プロパティアクセスはグローバルになります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-119">Unlike object access which is determined by the object's parent, property access is global.</span></span> <span data-ttu-id="71b4e-120">オブジェクトの親のアクセス要件に関係なく、すべてのオブジェクトには、スキーマで決定されたプロパティに対して同じアクセス許可があります。</span><span class="sxs-lookup"><span data-stu-id="71b4e-120">Every object, regardless of the access requirements of the object's parent, has the same permissions for the property as determined by the schema.</span></span>
  
<span data-ttu-id="71b4e-121">プロパティが読み取り専用の場合は、常に**GetProps**または**openproperty**呼び出しで使用できます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-121">When a property is read-only, it will always be available with a **GetProps** or **OpenProperty** call.</span></span> <span data-ttu-id="71b4e-122">ただし、プロパティをサポートしているオブジェクトの実装によっては、次の2つの結果があります。この場合、 **setprops**メソッドはプロパティを変更し、削除するために**deleteprops**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="71b4e-122">However, depending on the implementation of the object supporting the property, there are two possible outcomes for the **SetProps** method for modifying a property and the **DeleteProps** method for removing it:</span></span> 
  
- <span data-ttu-id="71b4e-123">Fail および return MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="71b4e-123">Fail and return MAPI_E_NO_ACCESS</span></span>
    
- <span data-ttu-id="71b4e-124">操作を実行せずに成功する</span><span class="sxs-lookup"><span data-stu-id="71b4e-124">Succeed with no action taken</span></span>
    
<span data-ttu-id="71b4e-125">プロパティとオブジェクトへのアクセスは、 **imapiprop**インターフェイスから継承する[ipropdata](ipropdataimapiprop.md)インターフェイスを使用して取得または設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-125">Property and object access can also be retrieved or set by using the [IPropData](ipropdataimapiprop.md) interface that inherits from the **IMAPIProp** interface.</span></span> <span data-ttu-id="71b4e-126">MAPI では、メモリ内のデータに基づく**ipropdata**の実装が提供されます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-126">MAPI provides an implementation of **IPropData** that is based on data in memory.</span></span> <span data-ttu-id="71b4e-127">サービスプロバイダーは、状態オブジェクトの場合や、組み込みトランザクションを持たないデータベースを使用している場合など、特定の状況で**imapiprop**を実装するために**ipropdata**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="71b4e-127">Service providers can use **IPropData** to implement **IMAPIProp** in certain circumstances, such as for their status object or if they are using a database that does not have built-in transactions.</span></span> <span data-ttu-id="71b4e-128">**ipropdata**はメモリ内でのみ動作するため、データをロックおよびロック解除する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="71b4e-128">**IPropData** works exclusively in memory, making it unnecessary to lock and unlock data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71b4e-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="71b4e-129">See also</span></span>



[<span data-ttu-id="71b4e-130">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="71b4e-130">MAPI Property Overview</span></span>](mapi-property-overview.md)

