---
title: MAPI オブジェクトを使用します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804210"
---
# <a name="using-mapi-objects"></a><span data-ttu-id="c88e6-103">MAPI オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88e6-103">Using MAPI objects</span></span>

<span data-ttu-id="c88e6-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c88e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c88e6-105">クライアントとサービス ・ プロバイダーは、そのインターフェイスの実装でのメソッドの呼び出しによって MAPI オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88e6-105">Clients and service providers use MAPI objects by calling the methods in their interface implementations.</span></span> <span data-ttu-id="c88e6-106">MAPI オブジェクトを使用することができることの唯一の方法は、このMAPI インターフェイスの外部オブジェクトによって実装されるメソッドは、パブリックにアクセス可能ではありません。</span><span class="sxs-lookup"><span data-stu-id="c88e6-106">This is the only way that MAPI objects can be used; methods that are implemented by an object outside of a MAPI interface are not publicly accessible.</span></span> <span data-ttu-id="c88e6-107">すべてのオブジェクトのインターフェイスは継承によって関連しているために、オブジェクトのユーザーは同じインターフェイスに属しているかのように基本インターフェイスまたは継承されたインターフェイスのいずれかのいずれかのメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c88e6-107">Because all of an object's interfaces are related through inheritance, an object's user can call methods in either the base interface or one of the inherited interfaces as if they belong to the same interface.</span></span> 
  
<span data-ttu-id="c88e6-108">メソッドへの呼び出しを実行しようとしているオブジェクトのユーザーと、そのオブジェクトには、継承によって関連するいくつかのインターフェイスが実装されて、ユーザー知る必要はありませんどのインタ フェースにメソッドが属しています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-108">When an object's user wants to make a call to a method and that object implements several interfaces related through inheritance, the user need not know to which interface the method belongs.</span></span> <span data-ttu-id="c88e6-109">ユーザーは、オブジェクトへのポインターを 1 つのインターフェイスのいずれかの任意のメソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c88e6-109">The user can call any of the methods on any of the interfaces with a single pointer to the object.</span></span> <span data-ttu-id="c88e6-110">たとえば、次の図では、folder オブジェクトをクライアント アプリケーションが使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-110">For example, the following illustration shows how a client application uses a folder object.</span></span> <span data-ttu-id="c88e6-111">フォルダー オブジェクトの実装、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)から間接的に[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)から継承するインターフェイスは、 [IMAPIProp: IUnknown](imapipropiunknown.md)と[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="c88e6-111">Folder objects implement the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface, which inherits from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirectly through [IMAPIProp : IUnknown](imapipropiunknown.md) and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="c88e6-112">**IMAPIProp**メソッドで、 [IMAPIProp::GetProps](imapiprop-getprops.md)などの 1 つは、いずれかのクライアントが呼び出すことができます、 [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)などのメソッドを[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)、同じオブジェクトへのポインターと同じようにします。</span><span class="sxs-lookup"><span data-stu-id="c88e6-112">A client can call one of the **IMAPIProp** methods, such as [IMAPIProp::GetProps](imapiprop-getprops.md), and one of the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) methods, such as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), in the same way with the same object pointer.</span></span> <span data-ttu-id="c88e6-113">クライアントは、、またはこれらの呼び出しは、別のインターフェイスに属しているという事実によって影響を受ける。</span><span class="sxs-lookup"><span data-stu-id="c88e6-113">A client is not aware of or affected by the fact that these calls belong to different interfaces.</span></span>
  
<span data-ttu-id="c88e6-114">**クライアントがフォルダー オブジェクトを使用**</span><span class="sxs-lookup"><span data-stu-id="c88e6-114">**Client use of a folder object**</span></span>
  
<span data-ttu-id="c88e6-115">![クライアントは、フォルダー オブジェクトの使用](media/amapi_40.gif "クライアントは、フォルダー オブジェクトの使用")</span><span class="sxs-lookup"><span data-stu-id="c88e6-115">![Client use of a folder object](media/amapi_40.gif "Client use of a folder object")</span></span>
  
<span data-ttu-id="c88e6-116">これらの呼び出しは、C または C++ の呼び出しを行うクライアントを作成するかどうかに応じて異なる方法でコードに変換します。</span><span class="sxs-lookup"><span data-stu-id="c88e6-116">These calls translate into code differently depending on whether the client making the calls is written in C or C++.</span></span> <span data-ttu-id="c88e6-117">メソッドへの呼び出しをする前に、インターフェイスの実装へのポインターを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c88e6-117">Before any call to a method can be made, a pointer to the interface implementation must be retrieved.</span></span> <span data-ttu-id="c88e6-118">インターフェイス ポインターは、次の方法で入手できます。</span><span class="sxs-lookup"><span data-stu-id="c88e6-118">Interface pointers can be obtained in the following ways:</span></span>
  
- <span data-ttu-id="c88e6-119">別のオブジェクトのメソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-119">Calling a method on a different object.</span></span>
    
- <span data-ttu-id="c88e6-120">API 関数を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-120">Calling an API function.</span></span>
    
- <span data-ttu-id="c88e6-121">ターゲット オブジェクトの[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-121">Calling the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method on the target object.</span></span> 
    
<span data-ttu-id="c88e6-122">MAPI には、いくつかのメソッドとインターフェイスの実装へのポインターを返す API 関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="c88e6-122">MAPI provides several methods and API functions that return pointers to interface implementations.</span></span> <span data-ttu-id="c88e6-123">クライアントが、メッセージ ストア プロバイダーの情報へのアクセスを提供するテーブル オブジェクトへのポインターを取得するために[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)メソッドを呼び出すことができますたとえば、 [IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="c88e6-123">For example, clients can call the [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) method to retrieve a pointer to a table object that provides access to message store provider information through the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="c88e6-124">サービス プロバイダーは、 [CreateTable](createtable.md)をテーブルのデータ オブジェクトへのポインターを取得するために API 関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="c88e6-124">Service providers can call the API function [CreateTable](createtable.md) to retrieve a pointer to a table data object.</span></span> <span data-ttu-id="c88e6-125">ない関数またはメソッドと、クライアントまたはサービス プロバイダー オブジェクトへのポインターがある、それらオブジェクトのインターフェイスの実装のもう 1 つへのポインターを取得するオブジェクトの**QueryInterface**メソッドを呼び出せます。</span><span class="sxs-lookup"><span data-stu-id="c88e6-125">When there is no function or method available and clients or service providers already have a pointer to an object, they can call the object's **QueryInterface** method to retrieve a pointer to another of the object's interface implementations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c88e6-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c88e6-126">See also</span></span>

- [<span data-ttu-id="c88e6-127">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="c88e6-127">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

