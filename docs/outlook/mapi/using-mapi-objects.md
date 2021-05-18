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
# <a name="using-mapi-objects"></a><span data-ttu-id="cafe1-103">MAPI オブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="cafe1-103">Using MAPI objects</span></span>

<span data-ttu-id="cafe1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cafe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cafe1-105">クライアントとサービス プロバイダーは、インターフェイスの実装でメソッドを呼び出すことによって MAPI オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="cafe1-105">Clients and service providers use MAPI objects by calling the methods in their interface implementations.</span></span> <span data-ttu-id="cafe1-106">これは、MAPI オブジェクトを使用できる唯一の方法です。MAPI インターフェイスの外部のオブジェクトによって実装されるメソッドは、パブリックにアクセスできない。</span><span class="sxs-lookup"><span data-stu-id="cafe1-106">This is the only way that MAPI objects can be used; methods that are implemented by an object outside of a MAPI interface are not publicly accessible.</span></span> <span data-ttu-id="cafe1-107">オブジェクトのすべてのインターフェイスは継承によって関連付け可能なので、オブジェクトのユーザーは、基本インターフェイスまたは継承されたインターフェイスの 1 つのメソッドを、同じインターフェイスに属している場合と同様に呼び出す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cafe1-107">Because all of an object's interfaces are related through inheritance, an object's user can call methods in either the base interface or one of the inherited interfaces as if they belong to the same interface.</span></span> 
  
<span data-ttu-id="cafe1-108">オブジェクトのユーザーがメソッドを呼び出し、そのオブジェクトが継承によって関連する複数のインターフェイスを実装する場合、ユーザーはメソッドが属するインターフェイスを知る必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cafe1-108">When an object's user wants to make a call to a method and that object implements several interfaces related through inheritance, the user need not know to which interface the method belongs.</span></span> <span data-ttu-id="cafe1-109">ユーザーは、オブジェクトへの 1 つのポインターを使用して、インターフェイス上の任意のメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cafe1-109">The user can call any of the methods on any of the interfaces with a single pointer to the object.</span></span> <span data-ttu-id="cafe1-110">たとえば、次の図は、クライアント アプリケーションがフォルダー オブジェクトを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cafe1-110">For example, the following illustration shows how a client application uses a folder object.</span></span> <span data-ttu-id="cafe1-111">フォルダー オブジェクトは [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) インターフェイスを実装します [。IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) から [IMAPIProp : IUnknown](imapipropiunknown.md) と [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)を介して間接的に継承されます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-111">Folder objects implement the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface, which inherits from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectly through [IMAPIProp : IUnknown](imapipropiunknown.md) and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="cafe1-112">クライアントは [、IMAPIProp::GetProps](imapiprop-getprops.md)などの **IMAPIProp** メソッドのいずれかを呼び出し、IMAPIFolder : [IMAPIContainer メソッド (IMAPIFolder::CreateMessage](imapifolder-createmessage.md)など) を同じ方法で同じオブジェクト ポインターで呼び出します。 [](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="cafe1-112">A client can call one of the **IMAPIProp** methods, such as [IMAPIProp::GetProps](imapiprop-getprops.md), and one of the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) methods, such as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), in the same way with the same object pointer.</span></span> <span data-ttu-id="cafe1-113">クライアントは、これらの呼び出しが異なるインターフェイスに属しているという事実に気づいても影響を受けもしません。</span><span class="sxs-lookup"><span data-stu-id="cafe1-113">A client is not aware of or affected by the fact that these calls belong to different interfaces.</span></span>
  
<span data-ttu-id="cafe1-114">**クライアントがフォルダー オブジェクトを使用**</span><span class="sxs-lookup"><span data-stu-id="cafe1-114">**Client use of a folder object**</span></span>
  
<span data-ttu-id="cafe1-115">![フォルダー オブジェクトのクライアントの使用](media/amapi_40.gif "フォルダー オブジェクトのクライアントの使用")</span><span class="sxs-lookup"><span data-stu-id="cafe1-115">![Client use of a folder object](media/amapi_40.gif "Client use of a folder object")</span></span>
  
<span data-ttu-id="cafe1-116">これらの呼び出しは、呼び出しを行うクライアントが C または C++ で記述されるかどうかによって異なるコードに変換されます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-116">These calls translate into code differently depending on whether the client making the calls is written in C or C++.</span></span> <span data-ttu-id="cafe1-117">メソッドを呼び出す前に、インターフェイス実装へのポインターを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cafe1-117">Before any call to a method can be made, a pointer to the interface implementation must be retrieved.</span></span> <span data-ttu-id="cafe1-118">インターフェイス ポインターは、次の方法で取得できます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-118">Interface pointers can be obtained in the following ways:</span></span>
  
- <span data-ttu-id="cafe1-119">別のオブジェクトでメソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="cafe1-119">Calling a method on a different object.</span></span>
    
- <span data-ttu-id="cafe1-120">API 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="cafe1-120">Calling an API function.</span></span>
    
- <span data-ttu-id="cafe1-121">ターゲット オブジェクト [で IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cafe1-121">Calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method on the target object.</span></span> 
    
<span data-ttu-id="cafe1-122">MAPI には、インターフェイス実装へのポインターを返すいくつかのメソッドと API 関数が提供されています。</span><span class="sxs-lookup"><span data-stu-id="cafe1-122">MAPI provides several methods and API functions that return pointers to interface implementations.</span></span> <span data-ttu-id="cafe1-123">たとえば、クライアントは [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) メソッドを呼び出して [、IMAPITable : IUnknown](imapitableiunknown.md) インターフェイスを介してメッセージ ストア プロバイダー情報へのアクセスを提供するテーブル オブジェクトへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-123">For example, clients can call the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method to retrieve a pointer to a table object that provides access to message store provider information through the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="cafe1-124">サービス プロバイダーは、API 関数 CreateTable を呼 [び出して](createtable.md) 、テーブル データ オブジェクトへのポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-124">Service providers can call the API function [CreateTable](createtable.md) to retrieve a pointer to a table data object.</span></span> <span data-ttu-id="cafe1-125">使用可能な関数またはメソッドが存在し、クライアントまたはサービス プロバイダーがオブジェクトへのポインターを既に持っている場合は、オブジェクトの **QueryInterface** メソッドを呼び出して、オブジェクトのインターフェイス実装の別のポインターを取得できます。</span><span class="sxs-lookup"><span data-stu-id="cafe1-125">When there is no function or method available and clients or service providers already have a pointer to an object, they can call the object's **QueryInterface** method to retrieve a pointer to another of the object's interface implementations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cafe1-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="cafe1-126">See also</span></span>

- [<span data-ttu-id="cafe1-127">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="cafe1-127">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

