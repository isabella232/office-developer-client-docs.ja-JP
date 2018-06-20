---
title: エラー処理のための戦略
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804014"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="a07b4-103">エラー処理のための戦略</span><span class="sxs-lookup"><span data-stu-id="a07b4-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="a07b4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a07b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a07b4-105">インターフェイス メソッドは仮想であるため、1 つの呼び出しから返される値の完全なセットを呼び出し元として認識することはできません。</span><span class="sxs-lookup"><span data-stu-id="a07b4-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="a07b4-106">メソッドの実装の 1 つが 5 つの値を返す可能性があります。別、8 つを返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="a07b4-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="a07b4-107">MAPI ドキュメント内の参照エントリは、各メソッドに返すことができるいくつかの値を一覧表示します。これらは、クライアントまたはサービス プロバイダーが確認し、特別な意味を持っているために処理される値です。</span><span class="sxs-lookup"><span data-stu-id="a07b4-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="a07b4-108">その他の値を返すことができますが、意味のあるできないため、それらを処理するために特別なコードが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="a07b4-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="a07b4-109">成功または失敗の簡単なチェックで十分です。</span><span class="sxs-lookup"><span data-stu-id="a07b4-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="a07b4-110">インターフェイスのメソッドのいくつかは、警告を返します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="a07b4-111">メソッドは、クライアントまたはサービス プロバイダーを呼び出すには、警告メッセージを返すことができる場合、は、0 または 0 以外のチェックではなく、戻り値をテストするのには**HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="a07b4-112">警告、0 以外の値がエラー コード点で異なります、上位ビットの設定はありません。</span><span class="sxs-lookup"><span data-stu-id="a07b4-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="a07b4-113">クライアントまたはサービス プロバイダーが、マクロを使用しない場合に、障害の警告を区別できない場合がありますが可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a07b4-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="a07b4-114">ほとんどのインターフェイスのメソッドと関数は、HRESULT 値を返す、いくつかの関数は、符号なしの long 値を返します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="a07b4-115">また、MAPI 環境で使用されるいくつかの方法は、COM から、MAPI エラー値ではなく COM エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="a07b4-116">呼び出しを行うときは、次のガイドラインに留意してください。</span><span class="sxs-lookup"><span data-stu-id="a07b4-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="a07b4-117">依存しないようにするか、 **IUnknown::AddRef**または**が**からの戻り値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="a07b4-118">これらの戻り値は、診断のためだけにします。</span><span class="sxs-lookup"><span data-stu-id="a07b4-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="a07b4-119">**IUnknown::QueryInterface**は、常に MAPI エラーではなく、FACILITY_NULL または FACILITY_RPC、施設では、汎用の COM エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="a07b4-120">他のすべてのインターフェイス メソッドでは、FACILITY_ITF、または FACILITY_RPC の機能を持つ MAPI インターフェイスのエラーまたは FACILITY_NULL エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="a07b4-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="a07b4-121">MAPI のサポートされていないメソッドの呼び出しが行われると、次の 4 つの可能なエラーのいずれかが返されます。</span><span class="sxs-lookup"><span data-stu-id="a07b4-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="a07b4-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a07b4-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="a07b4-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="a07b4-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="a07b4-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a07b4-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="a07b4-125">MAPI_E_VERSION。</span><span class="sxs-lookup"><span data-stu-id="a07b4-125">MAPI_E_VERSION.</span></span> 
  

