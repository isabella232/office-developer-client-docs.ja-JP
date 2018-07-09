---
title: MAPI オブジェクトを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800931"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="be922-103">MAPI オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="be922-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="be922-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be922-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be922-105">MAPI オブジェクトは、C++ のクラスや言語によっては、C のデータ構造を使用して実装できる API のクライアントの設定やサービス プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="be922-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="be922-106">MAPI サービス プロバイダー インターフェイスと C または C++ でサービス プロバイダーを記述できます。クライアント アプリケーションは、C または C++ を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="be922-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="be922-107">可能であれば、クライアントとオブジェクト指向プログラミング ・ インタ フェースを使用するサービス プロバイダーは、C を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be922-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="be922-108">C++ は、MAPI は、オブジェクト指向のテクノロジでは、および C++ に適していますより簡単にオブジェクト指向開発のための優先の選択です。</span><span class="sxs-lookup"><span data-stu-id="be922-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="be922-109">生成されるコードよりシンプルかつ簡単に維持するために簡単にします。</span><span class="sxs-lookup"><span data-stu-id="be922-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="be922-110">C++ 開発者は主に MAPI ドキュメントが書き込まれますC++ ではすべてこのリファレンスでは、MAPI インターフェイス メソッドの構文の説明です。</span><span class="sxs-lookup"><span data-stu-id="be922-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="be922-111">開発者は、MAPI を呼び出すためのソリューションを開発するのには、Microsoft Visual Studio、サードパーティ製の開発ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="be922-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="be922-112">開発者が C またはアンマネージ C++ を使用する必要がありますが、MAPI のソリューションを作成するのには C++ が管理されていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be922-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="be922-113">MAPI オブジェクトが実装されている場合、クライアントまたはサービス プロバイダーはインターフェイスのメソッド、プライベート メソッドの実装に固有のコードと状態情報を維持するためのプライベート データ メンバーをサポートするためのコードのすべてのコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="be922-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="be922-114">インターフェイス メソッドのコードは、正常な動作を文書化する MAPI によって公開された仕様に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="be922-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="be922-115">Mapidefs.h ヘッダー ファイルとクライアントとのいずれかの言語サービス プロバイダーを使用して MAPI オブジェクトの定義に役立つ OLE ヘッダー ファイル内の多くのマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="be922-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="be922-116">などの MAPI インターフェイスの各メソッドを定義するマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="be922-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="be922-117">[IUnknown](http://msdn.microsoft.com/ja-jp/library/ms680509%28v=VS.85%29.aspx)インターフェイスのメソッドを定義するマクロは、Mapidefs.h に次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="be922-117">The macro to define the methods of the [IUnknown](http://msdn.microsoft.com/ja-jp/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="be922-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="be922-118">See also</span></span>



[<span data-ttu-id="be922-119">MAPI オブジェクトとインターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="be922-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

