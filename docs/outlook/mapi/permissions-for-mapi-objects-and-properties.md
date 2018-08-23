---
title: MAPI オブジェクトおよびプロパティのアクセス許可
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aad19bbc016af6bdc0b17124b46112656af53a4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801716"
---
# <a name="permissions-for-mapi-objects-and-properties"></a><span data-ttu-id="458d3-103">MAPI オブジェクトおよびプロパティのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="458d3-103">Permissions for MAPI Objects and Properties</span></span>

  
  
<span data-ttu-id="458d3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="458d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="458d3-105">アクセス許可、または一連の permissable の操作には、MAPI オブジェクトおよびそれらのオブジェクトでサポートされている個々 のプロパティの特性がある場合ができます。</span><span class="sxs-lookup"><span data-stu-id="458d3-105">Access permission, or the set of permissable operations, can be a characteristic of MAPI objects and of individual properties supported by those objects.</span></span> <span data-ttu-id="458d3-106">オブジェクトへのアクセスは、オブジェクトの親によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="458d3-106">Object access is determined by an object's parent.</span></span> <span data-ttu-id="458d3-107">メッセージは、そのフォルダーはアクセス許可を決定します。</span><span class="sxs-lookup"><span data-stu-id="458d3-107">For a message, its folder determines access permissions.</span></span> <span data-ttu-id="458d3-108">メッセージングのユーザーまたは配布リスト、アドレス帳コンテナーはこの決定をなります。</span><span class="sxs-lookup"><span data-stu-id="458d3-108">For a messaging user or distribution list, its address book container makes this determination.</span></span> <span data-ttu-id="458d3-109">2 つのフォルダー、メッセージなどのオブジェクトが存在する場合、オブジェクトの 2 つのコピーのアクセス許可が異なる場合ができます。</span><span class="sxs-lookup"><span data-stu-id="458d3-109">When an object such as a message resides in two folders, the permissions for the two copies of the object can be different.</span></span> 
  
<span data-ttu-id="458d3-110">これらのオブジェクトを使用してクライアントに対するアクセス許可オブジェクトの[IMAPISession::OpenEntry](imapisession-openentry.md)の呼び出しで MAPI_BEST_ACCESS フラグを設定することで最高のレベルを要求できます。</span><span class="sxs-lookup"><span data-stu-id="458d3-110">Clients using these objects can request the highest level of access permitted for the object by setting the MAPI_BEST_ACCESS flag on the [IMAPISession::OpenEntry](imapisession-openentry.md) call.</span></span> <span data-ttu-id="458d3-111">オブジェクトを実装するサービス プロバイダーによって、クライアントは、必要なアクセス権のレベルは許可されません。</span><span class="sxs-lookup"><span data-stu-id="458d3-111">Depending on the service provider implementing the object, the client may or may not be granted the level of access necessary.</span></span> <span data-ttu-id="458d3-112">クライアントは、オブジェクト ([PidTagAccess](pidtagaccess-canonical-property.md)) である**PR_ACCESS**プロパティを取得するために**GetProps**メソッドを呼び出すことによって許可されたことをアクセスのレベルを決定できます。</span><span class="sxs-lookup"><span data-stu-id="458d3-112">Clients can determine the level of access that they were granted by calling the object **GetProps** method to retrieve the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property.</span></span> <span data-ttu-id="458d3-113">ただし、サービス プロバイダーは、このプロパティの値を動的に生成する必要があります、ためには、クライアントが必要な場合にのみを取得するをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="458d3-113">However, because the service provider must dynamically generate the value for this property, it is recommended that clients retrieve it only when necessary.</span></span> 
  
<span data-ttu-id="458d3-114">フォルダー、アドレス帳コンテナー、または配布リストなどのコンテナーに変更ができるかどうかを確認するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得するために**GetProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="458d3-114">To determine whether a container such as a folder, address book container, or distribution list allows modification, call its **GetProps** method to retrieve the **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span> <span data-ttu-id="458d3-115">コンテナー レベルのアクセスでは、クライアントで、ユーザー インターフェイスを表示する方法に影響します。</span><span class="sxs-lookup"><span data-stu-id="458d3-115">Container level access affects clients in terms of how they display their user interfaces.</span></span> <span data-ttu-id="458d3-116">ユーザー インターフェイスの表示と、一般的な実装ではコンテナー内のオブジェクトの実装も影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="458d3-116">It also impacts the implementers of objects within containers in terms of their user interface display and their general implementation.</span></span> 
  
<span data-ttu-id="458d3-117">特定のプロパティへのアクセスは、MAPI プロパティを所有するオブジェクトの設定、プロパティ スキーマによって決まります。</span><span class="sxs-lookup"><span data-stu-id="458d3-117">Access to a particular property is determined by the property schema set up by MAPI for the object that owns the property.</span></span> <span data-ttu-id="458d3-118">プロパティ スキーマは、オブジェクトとそのアクセス許可の必須およびオプションのプロパティのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="458d3-118">Property schemas specify the set of required and optional properties for an object and their access permission.</span></span> <span data-ttu-id="458d3-119">オブジェクトの親によって決定されるオブジェクトへのアクセスとは異なり、プロパティへのアクセスはグローバルです。</span><span class="sxs-lookup"><span data-stu-id="458d3-119">Unlike object access which is determined by the object's parent, property access is global.</span></span> <span data-ttu-id="458d3-120">オブジェクトの親のアクセスの要件にかかわらず、すべてのオブジェクトは、スキーマによって決定されたプロパティの同じ権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="458d3-120">Every object, regardless of the access requirements of the object's parent, has the same permissions for the property as determined by the schema.</span></span>
  
<span data-ttu-id="458d3-121">プロパティが読み取り専用の場合は、常に**GetProps**または**OpenProperty**の呼び出しで使用可能なことができます。</span><span class="sxs-lookup"><span data-stu-id="458d3-121">When a property is read-only, it will always be available with a **GetProps** or **OpenProperty** call.</span></span> <span data-ttu-id="458d3-122">ただし、プロパティをサポートするオブジェクトの実装によっては、プロパティとそれを削除するための**DeleteProps**メソッドを変更するための**SetProps**メソッドの 2 つの可能な結果があります。</span><span class="sxs-lookup"><span data-stu-id="458d3-122">However, depending on the implementation of the object supporting the property, there are two possible outcomes for the **SetProps** method for modifying a property and the **DeleteProps** method for removing it:</span></span> 
  
- <span data-ttu-id="458d3-123">失敗し、MAPI_E_NO_ACCESS を返す</span><span class="sxs-lookup"><span data-stu-id="458d3-123">Fail and return MAPI_E_NO_ACCESS</span></span>
    
- <span data-ttu-id="458d3-124">正常に処理は実行されません。</span><span class="sxs-lookup"><span data-stu-id="458d3-124">Succeed with no action taken</span></span>
    
<span data-ttu-id="458d3-125">プロパティとオブジェクト アクセスの取得または**IMAPIProp**インターフェイスを継承する[IPropData](ipropdataimapiprop.md)インターフェイスを使用して設定もできます。</span><span class="sxs-lookup"><span data-stu-id="458d3-125">Property and object access can also be retrieved or set by using the [IPropData](ipropdataimapiprop.md) interface that inherits from the **IMAPIProp** interface.</span></span> <span data-ttu-id="458d3-126">MAPI には、メモリ内のデータに基づく**IPropData**の実装が用意されています。</span><span class="sxs-lookup"><span data-stu-id="458d3-126">MAPI provides an implementation of **IPropData** that is based on data in memory.</span></span> <span data-ttu-id="458d3-127">サービス ・ プロバイダーは、状態オブジェクトのように特定の状況で**IMAPIProp**を実装するために**IPropData**を使用することができます。 または組み込みのトランザクションのないデータベースを使用している場合。</span><span class="sxs-lookup"><span data-stu-id="458d3-127">Service providers can use **IPropData** to implement **IMAPIProp** in certain circumstances, such as for their status object or if they are using a database that does not have built-in transactions.</span></span> <span data-ttu-id="458d3-128">**IPropData**は、ロックし、データのロックを解除する必要がないように、メモリ内でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="458d3-128">**IPropData** works exclusively in memory, making it unnecessary to lock and unlock data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="458d3-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="458d3-129">See also</span></span>



[<span data-ttu-id="458d3-130">MAPI のプロパティの概要</span><span class="sxs-lookup"><span data-stu-id="458d3-130">MAPI Property Overview</span></span>](mapi-property-overview.md)

