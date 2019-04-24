---
title: MAPI 文字セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319076"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="ae32d-103">MAPI 文字セット</span><span class="sxs-lookup"><span data-stu-id="ae32d-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="ae32d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae32d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae32d-105">MAPI 準拠のクライアントアプリケーションおよびサービスプロバイダーは、ANSI 文字 (1 バイト) または Unicode 文字 (2 バイト) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="ae32d-106">OEM 文字セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-106">OEM character sets are not supported.</span></span> <span data-ttu-id="ae32d-107">MAPI メソッドまたは関数に渡された OEM 文字列は、メソッドまたは関数が失敗する原因になります。</span><span class="sxs-lookup"><span data-stu-id="ae32d-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="ae32d-108">OEM 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI のメソッドまたは関数に渡す前に、それらのファイルを ANSI に変換するために注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae32d-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="ae32d-109">クライアントとサービスプロバイダーの両方で、Unicode 文字セットのサポートはオプションです。</span><span class="sxs-lookup"><span data-stu-id="ae32d-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="ae32d-110">すべてのサービスプロバイダーは、Unicode をサポートしているかどうかに関係なく、コンパイルできるようにコードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae32d-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="ae32d-111">クライアントは、サポートのレベルに応じて条件付きでコンパイルされますが、サービスプロバイダーには必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="ae32d-112">文字セットが変更されたときには、それらを再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="ae32d-113">サービスプロバイダーのコードでは、条件付きにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="ae32d-114">Unicode をサポートするクライアントまたはサービスプロバイダーが、入力パラメーターまたは出力パラメーターとして文字列を含むメソッド呼び出しを行うと、MAPI_UNICODE フラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="ae32d-115">このフラグを設定すると、すべての入力文字列が Unicode 文字列であることが実装に対して示されます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="ae32d-116">出力時に、このフラグを設定すると、実装から返されたすべての文字列が、可能であれば Unicode 文字列である必要があることが要求されます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="ae32d-117">Unicode をサポートするメソッドの実装は、要求に準拠します。Unicode のサポートを提供していないメソッドの実装は準拠していません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="ae32d-118">Unicode 形式ではない文字列プロパティの型は PT_STRING8 です。</span><span class="sxs-lookup"><span data-stu-id="ae32d-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="ae32d-119">MAPI は、ヘッダーファイル mapidefs.h で**fMapiUnicode**定数を定義します。H を既定の文字セットを表します。</span><span class="sxs-lookup"><span data-stu-id="ae32d-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="ae32d-120">クライアントまたはサービスプロバイダーが Unicode をサポートしている場合、 **fMapiUnicode**は MAPI_UNICODE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="ae32d-121">Unicode をサポートしていないクライアントおよびサービスプロバイダーは、 **fMapiUnicode**をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="ae32d-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="ae32d-122">Unicode をサポートしていないサービスプロバイダーは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ae32d-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="ae32d-123">文字セット間の変換を実行することを拒否します。</span><span class="sxs-lookup"><span data-stu-id="ae32d-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="ae32d-124">MAPI_UNICODE フラグをメソッド呼び出しに渡しません。</span><span class="sxs-lookup"><span data-stu-id="ae32d-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="ae32d-125">MAPI_UNICODE フラグが渡されると、MAPI_E_BAD_CHARWIDTH を返します。</span><span class="sxs-lookup"><span data-stu-id="ae32d-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="ae32d-126">ANSI 文字列プロパティを明示的に宣言します。</span><span class="sxs-lookup"><span data-stu-id="ae32d-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="ae32d-127">また、サービスプロバイダーが Unicode のみをサポートしており、クライアントが MAPI_UNICODE フラグを渡さない場合、MAPI_E_BAD_CHARWIDTH を返すこともできます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="ae32d-128">現在のバージョンの MAPI では、次の方法で Unicode がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ae32d-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="ae32d-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ae32d-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ae32d-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="ae32d-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="ae32d-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="ae32d-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="ae32d-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="ae32d-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="ae32d-133">[imapiprop:: GetLastError](imapiprop-getlasterror.md)(**IAddrBook**の実装のみ)</span><span class="sxs-lookup"><span data-stu-id="ae32d-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="ae32d-134">これらのメソッドでは、呼び出し元は、返される文字列を Unicode 文字列として受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="ae32d-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="ae32d-135">その他のメソッドの MAPI 実装から返される文字列は、ANSI 文字の文字列になります。</span><span class="sxs-lookup"><span data-stu-id="ae32d-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

