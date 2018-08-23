---
title: MAPI の文字セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5f7da3da8d23b28e13c39570b8f5971cb75a3310
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582533"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="c42d5-103">MAPI の文字セット</span><span class="sxs-lookup"><span data-stu-id="c42d5-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="c42d5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c42d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c42d5-105">MAPI 準拠のクライアント アプリケーションとサービス ・ プロバイダーは、ANSI 文字 (1 バイト)、または Unicode 文字 (2 バイト) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c42d5-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="c42d5-106">OEM 文字セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c42d5-106">OEM character sets are not supported.</span></span> <span data-ttu-id="c42d5-107">OEM 文字列は、MAPI メソッドに渡される、または関数と、そのメソッドまたは関数が失敗します。</span><span class="sxs-lookup"><span data-stu-id="c42d5-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="c42d5-108">OEM 文字セットでファイル名を使用するクライアント アプリケーションは、MAPI のメソッドまたは関数に渡す前に ANSI に変換するのには注意が必要である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c42d5-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="c42d5-109">Unicode をサポートしている文字セットは、クライアントとサービス ・ プロバイダーの両方はオプションです。</span><span class="sxs-lookup"><span data-stu-id="c42d5-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="c42d5-110">Unicode をサポートしているかどうかに関係なくコンパイルすることができるように、すべてのサービス プロバイダーでのコードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c42d5-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="c42d5-111">クライアントは、サポートのレベルに応じて条件付きでコンパイルしますが、サービス プロバイダーがありません。</span><span class="sxs-lookup"><span data-stu-id="c42d5-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="c42d5-112">文字セットが変更されたときに再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c42d5-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="c42d5-113">サービス プロバイダーのコードには何も条件付きにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c42d5-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="c42d5-114">クライアント、または Unicode の作成に入力パラメーターまたは出力パラメーターとして文字列を含むメソッドの呼び出しをサポートするサービス ・ プロバイダー、MAPI_UNICODE フラグが設定します。</span><span class="sxs-lookup"><span data-stu-id="c42d5-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="c42d5-115">このフラグを設定することを示します実装は、受信したすべての文字列を Unicode 文字列です。</span><span class="sxs-lookup"><span data-stu-id="c42d5-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="c42d5-116">出力では、このフラグ要求の実装から渡されるすべての文字列のバックアップを設定する必要があります Unicode 文字列可能な場合です。</span><span class="sxs-lookup"><span data-stu-id="c42d5-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="c42d5-117">Unicode をサポートしているメソッドの実装者は、要求に従いますUnicode サポートを提供していないメソッドの実装は準拠していません。</span><span class="sxs-lookup"><span data-stu-id="c42d5-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="c42d5-118">PT_STRING8 の種類は、Unicode 形式ではない文字列プロパティです。</span><span class="sxs-lookup"><span data-stu-id="c42d5-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="c42d5-119">MAPI では、ヘッダー ファイル MAPIDEFS に**fMapiUnicode**の定数を定義します。既定の文字セットを表す H をします。</span><span class="sxs-lookup"><span data-stu-id="c42d5-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="c42d5-120">クライアントまたはサービス プロバイダーは、Unicode をサポートする場合は、 **fMapiUnicode**が MAPI_UNICODE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c42d5-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="c42d5-121">クライアントと Unicode をサポートしていないサービス ・ プロバイダーは、 **fMapiUnicode**を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="c42d5-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="c42d5-122">Unicode をサポートしていないサービス ・ プロバイダーは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c42d5-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="c42d5-123">文字セット間で変換を実行することを拒否します。</span><span class="sxs-lookup"><span data-stu-id="c42d5-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="c42d5-124">メソッドの呼び出しで、MAPI_UNICODE フラグを渡すことはありません。</span><span class="sxs-lookup"><span data-stu-id="c42d5-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="c42d5-125">MAPI_E_BAD_CHARWIDTH は、MAPI_UNICODE フラグが渡されたときに返されます。</span><span class="sxs-lookup"><span data-stu-id="c42d5-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="c42d5-126">ANSI 文字列のプロパティを明示的に宣言します。</span><span class="sxs-lookup"><span data-stu-id="c42d5-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="c42d5-127">サービス プロバイダーでは、Unicode およびクライアントのみをサポートするときに MAPI_E_BAD_CHARWIDTH は、MAPI_UNICODE フラグを渡さないようにする必要を返すこともします。</span><span class="sxs-lookup"><span data-stu-id="c42d5-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="c42d5-128">現在のバージョンの MAPI では、次のメソッドの Unicode をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c42d5-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="c42d5-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c42d5-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="c42d5-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="c42d5-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="c42d5-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="c42d5-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="c42d5-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c42d5-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="c42d5-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md)(**IAddrBook**の実装のみ)</span><span class="sxs-lookup"><span data-stu-id="c42d5-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="c42d5-134">これらのメソッドの呼び出し元は、Unicode 文字列であると返される文字列を期待できます。</span><span class="sxs-lookup"><span data-stu-id="c42d5-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="c42d5-135">MAPI の実装の他のメソッドから返される文字列を ANSI 文字の文字列となります。</span><span class="sxs-lookup"><span data-stu-id="c42d5-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

