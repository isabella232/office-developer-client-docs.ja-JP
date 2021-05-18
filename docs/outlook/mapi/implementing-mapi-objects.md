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
# <a name="implementing-mapi-objects"></a><span data-ttu-id="deb69-103">MAPI オブジェクトの実装</span><span class="sxs-lookup"><span data-stu-id="deb69-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="deb69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="deb69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="deb69-105">MAPI オブジェクトは、クライアントまたはサービス プロバイダーが使用している言語と API セットに応じて、C++ クラスまたは C データ構造を使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="deb69-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="deb69-106">サービス プロバイダーは、MAPI サービス プロバイダー インターフェイスを使用して C または C++ で記述できます。クライアント アプリケーションは、C または C++ を使用できます。</span><span class="sxs-lookup"><span data-stu-id="deb69-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="deb69-107">可能であれば、オブジェクト指向プログラミング インターフェイスを使用するクライアントとサービス プロバイダーは C++ を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="deb69-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="deb69-108">MAPI はオブジェクト指向のテクノロジであり、C++ はオブジェクト指向の開発に容易に対応できるので、C++ が推奨される選択肢です。</span><span class="sxs-lookup"><span data-stu-id="deb69-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="deb69-109">結果として得られるコードは、より簡単で簡単になり、保守が容易になります。</span><span class="sxs-lookup"><span data-stu-id="deb69-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="deb69-110">MAPI ドキュメントは、主に C++ 開発者向けです。このリファレンスの MAPI インターフェイス メソッドの構文の説明はすべて C++ です。</span><span class="sxs-lookup"><span data-stu-id="deb69-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="deb69-111">開発者は、MAPI Microsoft Visual Studioソリューションを開発するために、サードパーティの開発ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="deb69-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="deb69-112">開発者は C またはアンマネージ C++を使用する必要がありますが、MAPI ソリューションを記述するには管理 C++ を使用しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="deb69-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="deb69-113">MAPI オブジェクトを実装すると、クライアントまたはサービス プロバイダーは、すべてのインターフェイス メソッドのコード、実装に固有のプライベート メソッドのコード、および状態情報を維持するためのプライベート データ メンバーをサポートするコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="deb69-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="deb69-114">インターフェイス メソッドのコードは、MAPI によって発行された仕様に従って、予期される動作を文書化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="deb69-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="deb69-115">Mapidefs.h ヘッダー ファイルと OLE ヘッダー ファイルには、クライアントとサービス プロバイダーが MAPI オブジェクトの定義を支援するために使用できるマクロが多数存在します。</span><span class="sxs-lookup"><span data-stu-id="deb69-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="deb69-116">たとえば、各 MAPI インターフェイスのメソッドを定義するマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="deb69-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="deb69-117">[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、Mapidefs.h に次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="deb69-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="deb69-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="deb69-118">See also</span></span>



[<span data-ttu-id="deb69-119">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="deb69-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

