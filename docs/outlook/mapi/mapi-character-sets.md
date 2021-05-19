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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417554"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="2c539-103">MAPI 文字セット</span><span class="sxs-lookup"><span data-stu-id="2c539-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="2c539-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c539-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c539-105">MAPI 準拠のクライアント アプリケーションとサービス プロバイダーは、ANSI 文字 (1 バイト) または Unicode 文字 (2 バイト) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2c539-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="2c539-106">OEM 文字セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c539-106">OEM character sets are not supported.</span></span> <span data-ttu-id="2c539-107">MAPI メソッドまたは関数に渡される OEM 文字列によって、そのメソッドまたは関数が失敗します。</span><span class="sxs-lookup"><span data-stu-id="2c539-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="2c539-108">OEM 文字セット内のファイル名を処理するクライアント アプリケーションは、MAPI メソッドまたは関数に渡す前に、ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="2c539-109">Unicode 文字セットのサポートは、クライアントとサービス プロバイダーの両方でオプションです。</span><span class="sxs-lookup"><span data-stu-id="2c539-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="2c539-110">すべてのサービス プロバイダーは、Unicode をサポートするかどうかに関係なくコンパイルできるよう、コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="2c539-111">クライアントは、サポートのレベルに応じて条件付きでコンパイルされますが、サービス プロバイダーはコンパイルしません。</span><span class="sxs-lookup"><span data-stu-id="2c539-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="2c539-112">文字セットが変更された場合は、再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="2c539-113">サービス プロバイダー コード内の条件を指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2c539-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="2c539-114">Unicode をサポートするクライアントまたはサービス プロバイダーが、文字列を入力パラメーターまたは出力パラメーターとして含むメソッド呼び出しを行う場合は、MAPI_UNICODEフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="2c539-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="2c539-115">このフラグを設定すると、すべての受信文字列が Unicode 文字列である実装が示されます。</span><span class="sxs-lookup"><span data-stu-id="2c539-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="2c539-116">出力時に、このフラグを設定すると、実装から返される文字列はすべて、可能であれば Unicode 文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="2c539-117">Unicode をサポートするメソッド実装者は要求に準拠します。Unicode サポートを提供しないメソッド実装者は準拠しない。</span><span class="sxs-lookup"><span data-stu-id="2c539-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="2c539-118">Unicode 形式ではない文字列プロパティは、文字列型PT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="2c539-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="2c539-119">MAPI は、ヘッダー ファイル MAPIDEFS で **fMapiUnicode** 定数を定義します。既定の文字セットを表す H。</span><span class="sxs-lookup"><span data-stu-id="2c539-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="2c539-120">クライアントまたはサービス プロバイダーが Unicode をサポートしている場合 **、fMapiUnicode** はユーザー設定にMAPI_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="2c539-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="2c539-121">Unicode をサポートしていないクライアントとサービス プロバイダーは **、fMapiUnicode を 0** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c539-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="2c539-122">Unicode をサポートしていないサービス プロバイダーは、次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="2c539-123">文字セット間の変換の実行を拒否します。</span><span class="sxs-lookup"><span data-stu-id="2c539-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="2c539-124">メソッド呼び出しでMAPI_UNICODEフラグを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="2c539-125">フラグMAPI_E_BAD_CHARWIDTH渡されたMAPI_UNICODEを返します。</span><span class="sxs-lookup"><span data-stu-id="2c539-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="2c539-126">ANSI 文字列プロパティを明示的に宣言します。</span><span class="sxs-lookup"><span data-stu-id="2c539-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="2c539-127">サービス プロバイダーは、Unicode のみをMAPI_E_BAD_CHARWIDTHし、クライアントがコード フラグを渡MAPI_UNICODEできます。</span><span class="sxs-lookup"><span data-stu-id="2c539-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="2c539-128">MAPI の現在のバージョンでは、次のメソッドで Unicode がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="2c539-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="2c539-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="2c539-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="2c539-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="2c539-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="2c539-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="2c539-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="2c539-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="2c539-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="2c539-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) **(IAddrBook 実装** のみ)</span><span class="sxs-lookup"><span data-stu-id="2c539-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="2c539-134">これらのメソッドでは、呼び出し元は、返される文字列が Unicode 文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c539-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="2c539-135">他のメソッドの MAPI 実装から返される文字列は、ANSI 文字文字列になります。</span><span class="sxs-lookup"><span data-stu-id="2c539-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

