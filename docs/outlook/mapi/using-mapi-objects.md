---
title: MAPI オブジェクトの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d732efe5276f4756f43b4aca46e1c33d6f103844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329679"
---
# <a name="using-mapi-objects"></a><span data-ttu-id="e186f-103">MAPI オブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="e186f-103">Using MAPI objects</span></span>

<span data-ttu-id="e186f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e186f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e186f-105">クライアントおよびサービスプロバイダーは、インターフェイス実装のメソッドを呼び出すことによって MAPI オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="e186f-105">Clients and service providers use MAPI objects by calling the methods in their interface implementations.</span></span> <span data-ttu-id="e186f-106">MAPI オブジェクトを使用できるのは、この方法のみです。MAPI インターフェイスの外部にあるオブジェクトによって実装されるメソッドは、パブリックにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="e186f-106">This is the only way that MAPI objects can be used; methods that are implemented by an object outside of a MAPI interface are not publicly accessible.</span></span> <span data-ttu-id="e186f-107">オブジェクトのすべてのインターフェイスは継承によって関連付けられているため、オブジェクトのユーザーは、基本インターフェイスまたは継承されたインターフェイスのいずれかで、同じインターフェイスに属するかのようにメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-107">Because all of an object's interfaces are related through inheritance, an object's user can call methods in either the base interface or one of the inherited interfaces as if they belong to the same interface.</span></span> 
  
<span data-ttu-id="e186f-108">オブジェクトのユーザーがメソッドを呼び出す必要があり、そのオブジェクトが継承に関連するいくつかのインターフェイスを実装している場合、ユーザーはそのメソッドが属するインターフェイスを知る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e186f-108">When an object's user wants to make a call to a method and that object implements several interfaces related through inheritance, the user need not know to which interface the method belongs.</span></span> <span data-ttu-id="e186f-109">ユーザーは、オブジェクトへの単一のポインターを使用して、インターフェイスのいずれかのメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-109">The user can call any of the methods on any of the interfaces with a single pointer to the object.</span></span> <span data-ttu-id="e186f-110">たとえば、次の図は、クライアントアプリケーションが folder オブジェクトを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e186f-110">For example, the following illustration shows how a client application uses a folder object.</span></span> <span data-ttu-id="e186f-111">Folder オブジェクトは[imapifolder: IMAPIContainer](imapifolderimapicontainer.md) interface を実装します。このインターフェイスは、 [imapifolder: iunknown](imapipropiunknown.md)および[IMAPIContainer: imapifolder](imapicontainerimapiprop.md)を介して[iunknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)を間接的に継承します。</span><span class="sxs-lookup"><span data-stu-id="e186f-111">Folder objects implement the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface, which inherits from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectly through [IMAPIProp : IUnknown](imapipropiunknown.md) and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="e186f-112">クライアントは、imapiprop [:: GetProps](imapiprop-getprops.md)などの**imapiprop**のメソッドのいずれかを呼び出し、同じオブジェクトポインターを使用した場合と同じ方法で、imapiprop [:: CreateMessage](imapifolder-createmessage.md)のような imapiprop:: [IMAPIContainer](imapifolderimapicontainer.md)メソッドの1つを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-112">A client can call one of the **IMAPIProp** methods, such as [IMAPIProp::GetProps](imapiprop-getprops.md), and one of the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) methods, such as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), in the same way with the same object pointer.</span></span> <span data-ttu-id="e186f-113">クライアントは、これらの呼び出しが異なるインターフェイスに属していることを認識していないか、または影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="e186f-113">A client is not aware of or affected by the fact that these calls belong to different interfaces.</span></span>
  
<span data-ttu-id="e186f-114">**クライアントがフォルダー オブジェクトを使用**</span><span class="sxs-lookup"><span data-stu-id="e186f-114">**Client use of a folder object**</span></span>
  
<span data-ttu-id="e186f-115">![クライアントでの folder オブジェクトの使用](media/amapi_40.gif "クライアントでの folder オブジェクトの使用")</span><span class="sxs-lookup"><span data-stu-id="e186f-115">![Client use of a folder object](media/amapi_40.gif "Client use of a folder object")</span></span>
  
<span data-ttu-id="e186f-116">これらの呼び出しは、呼び出しを行うクライアントが C または C++ で記述されているかどうかによって、コードによって異なる方法で変換されます。</span><span class="sxs-lookup"><span data-stu-id="e186f-116">These calls translate into code differently depending on whether the client making the calls is written in C or C++.</span></span> <span data-ttu-id="e186f-117">メソッドへの呼び出しを行う前に、インターフェイス実装へのポインターを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e186f-117">Before any call to a method can be made, a pointer to the interface implementation must be retrieved.</span></span> <span data-ttu-id="e186f-118">インターフェイスポインターは、次の方法で取得できます。</span><span class="sxs-lookup"><span data-stu-id="e186f-118">Interface pointers can be obtained in the following ways:</span></span>
  
- <span data-ttu-id="e186f-119">別のオブジェクトに対するメソッドの呼び出し。</span><span class="sxs-lookup"><span data-stu-id="e186f-119">Calling a method on a different object.</span></span>
    
- <span data-ttu-id="e186f-120">API 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="e186f-120">Calling an API function.</span></span>
    
- <span data-ttu-id="e186f-121">ターゲットオブジェクトで[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="e186f-121">Calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method on the target object.</span></span> 
    
<span data-ttu-id="e186f-122">MAPI には、インターフェイス実装へのポインターを返すメソッドと API 関数がいくつか用意されています。</span><span class="sxs-lookup"><span data-stu-id="e186f-122">MAPI provides several methods and API functions that return pointers to interface implementations.</span></span> <span data-ttu-id="e186f-123">たとえば、クライアントは[imapisession:: getmsgstorestable](imapisession-getmsgstorestable.md)メソッドを呼び出して、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスを介してメッセージストアプロバイダ情報へのアクセスを提供する table オブジェクトへのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-123">For example, clients can call the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method to retrieve a pointer to a table object that provides access to message store provider information through the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="e186f-124">サービスプロバイダーは、 [CreateTable](createtable.md) API 関数を呼び出して、テーブルデータオブジェクトへのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-124">Service providers can call the API function [CreateTable](createtable.md) to retrieve a pointer to a table data object.</span></span> <span data-ttu-id="e186f-125">使用可能な関数またはメソッドがなく、クライアントまたはサービスプロバイダーが既にオブジェクトへのポインターを持っている場合は、オブジェクトの**QueryInterface**メソッドを呼び出して、そのオブジェクトのインターフェイス実装へのポインターを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="e186f-125">When there is no function or method available and clients or service providers already have a pointer to an object, they can call the object's **QueryInterface** method to retrieve a pointer to another of the object's interface implementations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e186f-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="e186f-126">See also</span></span>

- [<span data-ttu-id="e186f-127">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="e186f-127">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

