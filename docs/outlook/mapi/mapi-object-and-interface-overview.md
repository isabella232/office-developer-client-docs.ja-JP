---
title: MAPI オブジェクトとインターフェイスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fcd85bf518f4e6466bf15a09e417767bc34df78d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345788"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="2e2ec-103">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="2e2ec-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="2e2ec-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e2ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e2ec-105">MAPI オブジェクトは、1 つ以上の MAPI インターフェイスまたは関連する関数のコレクションから継承された C++ オブジェクト クラスまたは C データ構造です。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="2e2ec-106">関連する関数のこれらのコレクションは、純粋な仮想関数として C++ 開発者に知られています。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="2e2ec-107">純粋な仮想関数の場合、MAPI は実装ではなく関数プロトタイプのみを提供します。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="2e2ec-108">クライアント アプリケーション、サービス プロバイダー、または MAPI が、インターフェイスから継承し、Messaging API の関数の説明に準拠するオブジェクト クラスを作成することで、この実装を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="2e2ec-109">MAPI インターフェイスは、継承されたクラスを通じてのみインスタンス化できます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="2e2ec-110">[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから最終的に継承されるインターフェイスから継承する各オブジェクトには、さまざまな MAPI オブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="2e2ec-111">**IUnknown は** OLE コンポーネント オブジェクト モデル (COM) ベース インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="2e2ec-112">MAPI オブジェクトには、通信と制御のための標準的なメカニズムが提供されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="2e2ec-113">COM は、オブジェクト実装者がメモリ管理、パラメーター管理、マルチスレッドなどの問題を処理する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="2e2ec-114">このモデルに準拠することで、オブジェクト実装者は、オブジェクトに含まれるインターフェイスで指定されたコントラクトに従います。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="2e2ec-115">多くの MAPI インターフェイスは **IUnknown** から直接継承されます。他のインターフェイスは [、IMAPIProp : IUnknown](imapipropiunknown.md) for property management および [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access の 2 つのベース インターフェイスのいずれかを介して間接的に継承されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="2e2ec-116">基本インターフェイスは、独立したスタンドアロン オブジェクトとして実装されません。これらは、派生インターフェイスを実装する他のオブジェクト、オブジェクトの一部として常に実装されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="2e2ec-117">MAPI では、1 つ以上の MAPI コンポーネントによって実装されるさまざまな種類のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="2e2ec-118">クライアントによって実装されたオブジェクトは、MAPI、サービス プロバイダー、およびカスタム フォーム コンポーネントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="2e2ec-119">サービス プロバイダーによって実装されるオブジェクトは、通常、MAPI およびクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="2e2ec-120">フォーム ライブラリ プロバイダーとフォーム サーバーによって実装されたオブジェクトは、他のフォーム コンポーネントやクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e2ec-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e2ec-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e2ec-121">See also</span></span>



[<span data-ttu-id="2e2ec-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e2ec-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="2e2ec-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2e2ec-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="2e2ec-124">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="2e2ec-124">MAPI Concepts</span></span>](mapi-concepts.md)

