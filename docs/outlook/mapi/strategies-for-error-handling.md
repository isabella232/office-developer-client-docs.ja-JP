---
title: エラー処理の戦略
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424148"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="6dde2-103">エラー処理の戦略</span><span class="sxs-lookup"><span data-stu-id="6dde2-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="6dde2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dde2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dde2-105">インターフェイスメソッドは仮想になっているため、呼び出し元として、1つの呼び出しから返される可能性のある値の完全なセットを知ることはできません。</span><span class="sxs-lookup"><span data-stu-id="6dde2-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="6dde2-106">1つのメソッドの実装は5つの値を返す場合があります。別の場合は8を返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="6dde2-107">MAPI ドキュメントの参照エントリには、各メソッドに対して返すことができるいくつかの値が記載されています。これらの値は、クライアントまたはサービスプロバイダーが特別な意味を持つため、確認して処理することができます。</span><span class="sxs-lookup"><span data-stu-id="6dde2-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="6dde2-108">その他の値は返すことができますが、意味がないため、これらを処理するための特別なコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6dde2-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="6dde2-109">成功または失敗の簡単なチェックは、十分です。</span><span class="sxs-lookup"><span data-stu-id="6dde2-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="6dde2-110">インターフェイスメソッドのいくつかは、警告を返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="6dde2-111">クライアントまたはサービスプロバイダーが呼び出すメソッドが警告を返す場合は、 **HR_FAILED**マクロを使用して、ゼロまたは0以外のチェックではなく、戻り値をテストします。</span><span class="sxs-lookup"><span data-stu-id="6dde2-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="6dde2-112">警告は、0以外の場合でも、上位ビットが設定されていないというエラーコードとは異なります。</span><span class="sxs-lookup"><span data-stu-id="6dde2-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="6dde2-113">クライアントまたはサービスプロバイダーがマクロを使用しない場合は、エラーの原因となる警告が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="6dde2-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="6dde2-114">ほとんどのインターフェイスメソッドと関数は、HRESULT 値を返しますが、一部の関数は、符号なし長整数型 (long) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="6dde2-115">また、mapi 環境で使用されているいくつかのメソッドは、com からのものであり、mapi エラー値ではなく com エラー値を返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="6dde2-116">呼び出しを行うときは、次のガイドラインに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6dde2-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="6dde2-117">**iunknown:: AddRef**または**iunknown:: Release**の戻り値を使用したり、使用したりすることはありません。</span><span class="sxs-lookup"><span data-stu-id="6dde2-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="6dde2-118">これらの戻り値は、診断のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="6dde2-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="6dde2-119">**IUnknown:: QueryInterface**は、MAPI エラーではなく、ファシリティが FACILITY_NULL または FACILITY_RPC である汎用 COM エラーを常に返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="6dde2-120">他のすべてのインターフェイスメソッドは、FACILITY_ITF のファシリティ、FACILITY_RPC、または FACILITY_NULL のエラーを含む MAPI インターフェイスエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="6dde2-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="6dde2-121">サポートされていない MAPI メソッドに対して呼び出しを行った場合、次の4つのエラーのいずれかが返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="6dde2-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="6dde2-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6dde2-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="6dde2-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6dde2-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="6dde2-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6dde2-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="6dde2-125">MAPI_E_VERSION。</span><span class="sxs-lookup"><span data-stu-id="6dde2-125">MAPI_E_VERSION.</span></span> 
  

