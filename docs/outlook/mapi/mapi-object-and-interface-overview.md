---
title: MAPI のオブジェクトとインターフェイスの概要
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
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="ea06a-103">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="ea06a-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="ea06a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea06a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea06a-105">mapi オブジェクトは、1つ以上の mapi インターフェイスまたは関連する関数のコレクションから継承された C++ オブジェクトクラスまたは c データ構造です。</span><span class="sxs-lookup"><span data-stu-id="ea06a-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="ea06a-106">これらの関連する関数のコレクションは、C++ 開発者が純粋仮想関数として知られています。</span><span class="sxs-lookup"><span data-stu-id="ea06a-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="ea06a-107">純粋仮想関数の場合、MAPI は関数プロトタイプのみを提供し、実装は提供しません。</span><span class="sxs-lookup"><span data-stu-id="ea06a-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="ea06a-108">クライアントアプリケーション、サービスプロバイダー、または MAPI がこの実装を提供することは、インターフェイスを継承するオブジェクトクラスを作成し、メッセージング API の関数の説明に準拠していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="ea06a-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="ea06a-109">MAPI インターフェイスは、継承されたクラスによってのみインスタンス化できます。</span><span class="sxs-lookup"><span data-stu-id="ea06a-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="ea06a-110">さまざまな MAPI オブジェクトがあります。各オブジェクトは、最終的に[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから継承されるインターフェイスから継承します。</span><span class="sxs-lookup"><span data-stu-id="ea06a-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="ea06a-111">**IUnknown**は、OLE コンポーネントオブジェクトモデル (COM) 基本インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="ea06a-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="ea06a-112">これは、通信と制御のための標準的なメカニズムを使用して MAPI オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="ea06a-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="ea06a-113">COM は、オブジェクトの実装者がメモリ管理、パラメーター管理、マルチスレッドなどの問題をどのように処理するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ea06a-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="ea06a-114">このモデルに準拠することにより、オブジェクトの実装者は、オブジェクトに含まれているインターフェイスで指定されたコントラクトに準拠します。</span><span class="sxs-lookup"><span data-stu-id="ea06a-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="ea06a-115">多くの MAPI インターフェイスは**IUnknown**から直接継承されていますが、他のインターフェイスは、 [imapiprop: iunknown](imapipropiunknown.md) for property management and [IMAPIContainer: imapiprop](imapicontainerimapiprop.md) for folder およびという2つの基本インターフェイスのいずれかによって間接的に継承されます。アドレス帳へのアクセス。</span><span class="sxs-lookup"><span data-stu-id="ea06a-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="ea06a-116">基本インターフェイスは、独立したスタンドアロンオブジェクトとしては実装されません。これらは常に、派生インターフェイスを実装するオブジェクトである他のオブジェクトの一部として実装されます。</span><span class="sxs-lookup"><span data-stu-id="ea06a-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="ea06a-117">mapi は、それぞれが1つ以上の mapi コンポーネントによって実装された、さまざまな種類のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="ea06a-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="ea06a-118">クライアントによって実装されたオブジェクトは、MAPI、サービスプロバイダー、およびカスタムフォームコンポーネントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea06a-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="ea06a-119">サービスプロバイダーによって実装されるオブジェクトは、通常、MAPI およびクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea06a-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="ea06a-120">フォームライブラリプロバイダおよびフォームサーバーによって実装されたオブジェクトは、他のフォームコンポーネントおよびクライアントによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea06a-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ea06a-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="ea06a-121">See also</span></span>



[<span data-ttu-id="ea06a-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ea06a-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ea06a-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ea06a-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="ea06a-124">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="ea06a-124">MAPI Concepts</span></span>](mapi-concepts.md)

