---
title: MAPI オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310172"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="5c32e-103">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="5c32e-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="5c32e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c32e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c32e-105">MAPI オブジェクトは、言語およびクライアントまたはサービスプロバイダーが使用している API セットに応じて、C++ のクラスまたは C データ構造を使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="5c32e-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="5c32e-106">サービスプロバイダーは、MAPI サービスプロバイダインターフェイスを使用して C または C++ で記述できます。クライアントアプリケーションは C または C++ を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5c32e-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="5c32e-107">可能な場合は、オブジェクト指向プログラミングインターフェイスを使用するクライアントおよびサービスプロバイダーに C++ を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c32e-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="5c32e-108">c++ は、MAPI はオブジェクト指向のテクノロジであり、c++ はオブジェクト指向の開発にもより容易に使用できるため、推奨される選択です。</span><span class="sxs-lookup"><span data-stu-id="5c32e-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="5c32e-109">生成されるコードはシンプルでわかりやすく、保守が容易になります。</span><span class="sxs-lookup"><span data-stu-id="5c32e-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="5c32e-110">MAPI ドキュメントは、主に C++ 開発者向けに記述されています。このリファレンスに記載されている MAPI インターフェイスメソッドのすべての構文の説明は、C++ に含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c32e-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="5c32e-111">開発者は、Microsoft Visual Studio およびサードパーティの開発ツールを使用して MAPI を呼び出すソリューションを開発できます。</span><span class="sxs-lookup"><span data-stu-id="5c32e-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="5c32e-112">開発者は c またはアンマネージ c++ を使用する必要がありますが、管理された c++ を使用して MAPI ソリューションを記述することはできません。</span><span class="sxs-lookup"><span data-stu-id="5c32e-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="5c32e-113">MAPI オブジェクトが実装されている場合、クライアントまたはサービスプロバイダーは、すべてのインターフェイスメソッドのコード、実装に固有のプライベートメソッドのコード、および状態情報を保持するためのプライベートデータメンバーをサポートするコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c32e-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="5c32e-114">インターフェイスメソッドのコードは、予期される動作を文書化する MAPI によって発行された仕様に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c32e-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="5c32e-115">mapidefs.h ヘッダーファイルと OLE ヘッダーファイルには多数のマクロがあり、どちらの言語のクライアントとサービスプロバイダーも MAPI オブジェクトの定義を支援するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c32e-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="5c32e-116">たとえば、各 MAPI インターフェイスのメソッドを定義するマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="5c32e-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="5c32e-117">[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、mapidefs.h で次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c32e-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="5c32e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c32e-118">See also</span></span>



[<span data-ttu-id="5c32e-119">MAPI のオブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="5c32e-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

