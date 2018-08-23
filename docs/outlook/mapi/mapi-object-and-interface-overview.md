---
title: MAPI オブジェクトとインターフェイスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d4ece3af-cb54-4727-8072-0c055381ec11
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8882457ff99f4150f2c9b086b92af32de29d60a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801395"
---
# <a name="mapi-object-and-interface-overview"></a><span data-ttu-id="0b43b-103">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="0b43b-103">MAPI Object and Interface Overview</span></span>

  
  
<span data-ttu-id="0b43b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b43b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b43b-105">MAPI オブジェクトは、オブジェクト クラスの C++ または C のデータ構造体の 1 つまたは複数の MAPI インターフェイス、または関連する関数のコレクションから継承します。</span><span class="sxs-lookup"><span data-stu-id="0b43b-105">A MAPI object is a C++ object class or C data structure inherited from one or more MAPI interfaces, or collections of related functions.</span></span> <span data-ttu-id="0b43b-106">関連する関数のこれらのコレクションは、C++ 開発者にとって、純粋仮想関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0b43b-106">These collections of related functions are known to C++ developers as pure virtual functions.</span></span> <span data-ttu-id="0b43b-107">純粋仮想関数では、MAPI には、のみ関数プロトタイプ実装ではなくが用意されています。</span><span class="sxs-lookup"><span data-stu-id="0b43b-107">For a pure virtual function, MAPI supplies only the function prototype, not an implementation.</span></span> <span data-ttu-id="0b43b-108">クライアント アプリケーション、サービス プロバイダー、または MAPI を提供するこの実装はメッセージング API の関数の説明に準拠しているインターフェイスを継承するオブジェクト クラスを作成して予定です。</span><span class="sxs-lookup"><span data-stu-id="0b43b-108">It is expected that a client application, a service provider, or MAPI will provide this implementation by creating an object class that inherits from the interface and conforms to the function descriptions of the Messaging API.</span></span> <span data-ttu-id="0b43b-109">MAPI インターフェイスは、継承クラスでのみインスタンス化できます。</span><span class="sxs-lookup"><span data-stu-id="0b43b-109">A MAPI interface can be instantiated only through an inherited class.</span></span>
  
<span data-ttu-id="0b43b-110">別の MAPI オブジェクトが多く、最終的には、 [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx)インターフェイスから継承されているインターフェイスから継承する各オブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="0b43b-110">There are many different MAPI objects, each object inheriting from an interface that is ultimately inherited from the [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="0b43b-111">**IUnknown**は、OLE コンポーネント オブジェクト モデル (COM) の基本インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="0b43b-111">**IUnknown** is the OLE Component Object Model (COM) base interface.</span></span> <span data-ttu-id="0b43b-112">通信と制御のための標準的なメカニズムに MAPI オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b43b-112">It provides MAPI objects with a standard mechanism for communication and control.</span></span> <span data-ttu-id="0b43b-113">COM オブジェクトの実装がメモリ管理では、パラメーターの管理などの問題を処理する方法を決定し、マルチ スレッドです。</span><span class="sxs-lookup"><span data-stu-id="0b43b-113">COM dictates how object implementers handle issues such as memory management, parameter management, and multithreading.</span></span> <span data-ttu-id="0b43b-114">このモデルに準拠する、ことでは、オブジェクトの実装側は、オブジェクトに含まれているインタ フェースが指定されている契約に準拠します。</span><span class="sxs-lookup"><span data-stu-id="0b43b-114">By conforming to this model, an object implementer adheres to a contract as specified by the interfaces included in the object.</span></span> 
  
<span data-ttu-id="0b43b-115">他で継承されていない直接他の 2 つの基本インターフェイスのいずれかの中に、多数の MAPI インターフェイスが**IUnknown**から直接継承されます: [IMAPIProp: IUnknown](imapipropiunknown.md)のプロパティの管理と[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)フォルダーのとアドレス帳にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0b43b-115">Many MAPI interfaces are inherited directly from **IUnknown**, while others are inherited indirectly through one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) for property management and [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) for folder and address book access.</span></span> <span data-ttu-id="0b43b-116">独立したスタンドアロン オブジェクトとしての基本インターフェイスを実装しません。常に他のオブジェクトの一部として実装される、派生インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="0b43b-116">Base interfaces are never implemented as separate, standalone objects; they are always implemented as part of other objects, objects that implement derived interfaces.</span></span> 
  
<span data-ttu-id="0b43b-117">1 つまたは複数の MAPI コンポーネントによって実装されている各、MAPI は、多くの種類のオブジェクトを定義します。</span><span class="sxs-lookup"><span data-stu-id="0b43b-117">MAPI defines many types of objects, each implemented by one or more MAPI components.</span></span> <span data-ttu-id="0b43b-118">クライアントによって実装されたオブジェクトは、MAPI によって、サービス プロバイダー、およびカスタム フォームのコンポーネントに使用されます。</span><span class="sxs-lookup"><span data-stu-id="0b43b-118">Objects implemented by clients are used by MAPI, by service providers, and by custom form components.</span></span> <span data-ttu-id="0b43b-119">サービス プロバイダーによって実装されたオブジェクトは、MAPI によって、クライアントが通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="0b43b-119">Objects implemented by service providers are typically used by MAPI and by clients.</span></span> <span data-ttu-id="0b43b-120">オブジェクトは、フォーム ライブラリのプロバイダーによって実装されているし、他のフォームのコンポーネントとクライアントによってフォームのサーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="0b43b-120">Objects implemented by form library providers and form servers are used by other form components and by clients.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b43b-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b43b-121">See also</span></span>



[<span data-ttu-id="0b43b-122">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b43b-122">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="0b43b-123">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0b43b-123">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="0b43b-124">MAPI の概念</span><span class="sxs-lookup"><span data-stu-id="0b43b-124">MAPI Concepts</span></span>](mapi-concepts.md)

