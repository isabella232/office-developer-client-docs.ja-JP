---
title: MAPI の戻り値の文書化
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429692"
---
# <a name="mapi-return-value-documentation"></a><span data-ttu-id="e9a3b-103">MAPI の戻り値の文書化</span><span class="sxs-lookup"><span data-stu-id="e9a3b-103">MAPI Return Value Documentation</span></span>

  
  
<span data-ttu-id="e9a3b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9a3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9a3b-105">このリファレンスに記載されている参照エントリは、クライアントアプリケーションによって何らかの処理を必要とする戻り値のみを文書化します。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-105">The reference entries in this Reference document only those return values that require some handling by client applications.</span></span> <span data-ttu-id="e9a3b-106">エラー状態をチェックすることによって検出できる一般的なエラー条件を示す戻り値は、このドキュメントには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-106">Return values that indicate common error conditions and can be deduced by checking for failure are not included in the documentation.</span></span> <span data-ttu-id="e9a3b-107">たとえば、多くのインターフェイスメソッドは、呼び出し元が入力パラメーターに間違った値を指定した場合に MAPI_E_INVALID_PARAMETER を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-107">For example, many interface methods can return MAPI_E_INVALID_PARAMETER if a caller specifies the wrong value for an input parameter.</span></span> <span data-ttu-id="e9a3b-108">この値は、通常、MAPI_E_INVALID_PARAMETER を特定する必要がなく、他のエラーとは異なる方法で処理する必要がないため、予想される戻り値のセットには表示されません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-108">This value is typically not listed in the set of expected return values because there is no need to look specifically for MAPI_E_INVALID_PARAMETER and no need to process it differently from any other error.</span></span> <span data-ttu-id="e9a3b-109">一方、一部のサービスプロバイダーはイベント通知をサポートしておらず、 **imapisession**を通じてクライアントによって作成された**Advise**メソッドに MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-109">On the other hand, some service providers do not support event notification and will return MAPI_E_NO_SUPPORT to the **Advise** method made by clients through **IMAPISession**.</span></span> <span data-ttu-id="e9a3b-110">クライアントは、この値を明示的に確認して、それが表す条件を処理するコードを提供する必要があるため、MAPI_E_NO_SUPPORT は[imapisession:: Advise](imapisession-advise.md)の戻り値の一覧に含まれています。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-110">Because clients need to explicitly check for this value and provide code for handling the condition that it represents should it occur, MAPI_E_NO_SUPPORT is included in the list of return values for [IMAPISession::Advise](imapisession-advise.md).</span></span>
  
<span data-ttu-id="e9a3b-111">次の表では、メソッドと関数から一般的に返されるエラー値と、クライアントまたはサービスプロバイダーの部分を明示的に処理する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-111">The following table describes error values that are commonly returned from methods and functions and require explicit handling on the part of a client or service provider.</span></span> <span data-ttu-id="e9a3b-112">これらの値は、無効な入力データを示す値、リソースの問題を示す値、文字セットの非互換性を示す値、および不明な配信が失敗したことを示す値の4つのカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-112">These values fall into four categories: values that indicate invalid input data, values that indicate resource problems, values that indicate character set incompatibility, and values that indicate failure of an unknown origin.</span></span>
  
|<span data-ttu-id="e9a3b-113">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="e9a3b-113">**Return value**</span></span>|<span data-ttu-id="e9a3b-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="e9a3b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9a3b-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9a3b-115">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="e9a3b-116">メソッドまたは関数に渡された1つ以上のパラメーターが有効ではありませんでした。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-116">One or more of the parameters passed into the method or functions were not valid.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-117">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e9a3b-117">MAPI_E_UNKNOWN_FLAGS</span></span>  <br/> |<span data-ttu-id="e9a3b-118">flags パラメーターの1つ以上の値が無効です。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-118">One or more values for a flags parameter were not valid.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-119">MAPI_E_DISK_ERROR</span><span class="sxs-lookup"><span data-stu-id="e9a3b-119">MAPI_E_DISK_ERROR</span></span>  <br/> |<span data-ttu-id="e9a3b-120">ディスクへの書き込み中またはディスクからの読み取り中に問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-120">There was a problem writing to or reading from disk.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-121">MAPI_E_NOT_ENOUGH_DISK</span><span class="sxs-lookup"><span data-stu-id="e9a3b-121">MAPI_E_NOT_ENOUGH_DISK</span></span>  <br/> |<span data-ttu-id="e9a3b-122">操作を完了するのに十分なディスク容量がありません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-122">Not enough disk space was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-123">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="e9a3b-123">MAPI_E_NOT_ENOUGH_MEMORY</span></span>  <br/> |<span data-ttu-id="e9a3b-124">メモリが不足しているため、操作を完了できません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-124">Not enough memory was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-125">MAPI_E_NOT_ENOUGH_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="e9a3b-125">MAPI_E_NOT_ENOUGH_RESOURCES</span></span>  <br/> |<span data-ttu-id="e9a3b-126">システムリソースが不足しているため、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-126">Not enough system resources were available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-127">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9a3b-127">MAPI_E_BAD_CHARWIDTH</span></span>  <br/> |<span data-ttu-id="e9a3b-128">呼び出し元と実装でサポートされている文字セットに互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-128">An incompatibility exists in the character sets supported by the caller and the implementation.</span></span>  <br/> |
|<span data-ttu-id="e9a3b-129">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="e9a3b-129">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="e9a3b-130">予期しないまたは不明な送信元のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-130">An error of unexpected or unknown origin occurred.</span></span>  <br/> |
   
<span data-ttu-id="e9a3b-131">MAPI の戻り値を表す定数は、MAPICODE に示されています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-131">The constants that represent MAPI return values are listed in the MAPICODE.H header file.</span></span> <span data-ttu-id="e9a3b-132">一部の定数は Win32 エラーに対応しています。これらの定数を数値にマッピングする方法については、Win32 ヘッダーファイル winerror.h を参照してください。H.</span><span class="sxs-lookup"><span data-stu-id="e9a3b-132">Some of the constants map to Win32 errors; the mapping of these constants to numeric values can be found in the Win32 header file, WINERROR.H.</span></span>
  
<span data-ttu-id="e9a3b-133">呼び出し元によって渡された無効なデータに関するエラーは、MAPI またはマクロのセットによって提供されるパラメーター検証 API 関数のどちらかによって決定できます。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-133">Errors regarding invalid data passed in by a caller can be determined through either the parameter validation API functions provided by MAPI or a set of macros.</span></span> 
  
<span data-ttu-id="e9a3b-134">文字セットの非互換性は、次のいずれかの状況が発生した場合に生じます。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-134">Character set incompatibility arises when either of the following situations occurs:</span></span>
  
- <span data-ttu-id="e9a3b-135">クライアントまたはサービスプロバイダーがメソッドまたは関数呼び出しに MAPI_UNICODE フラグを設定していますが、実装で UNICODE がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-135">A client or service provider sets the MAPI_UNICODE flag on a method or function call and the implementation does not support Unicode.</span></span> <span data-ttu-id="e9a3b-136">MAPI_UNICODE を設定すると、入力として渡された文字文字列が unicode 文字列であること、および出力として返される文字文字列が unicode 文字列であることが想定されます。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-136">Setting MAPI_UNICODE indicates that character strings passed in as input are Unicode strings and that character strings passed back as output are expected to be Unicode strings.</span></span>
    
- <span data-ttu-id="e9a3b-137">クライアントまたはサービスプロバイダーは、メソッドまたは関数呼び出しに MAPI_UNICODE フラグを設定しません。実装では、UNICODE のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e9a3b-137">A client or service provider does not set the MAPI_UNICODE flag on a method or function call and the implementation only supports Unicode.</span></span>
    

