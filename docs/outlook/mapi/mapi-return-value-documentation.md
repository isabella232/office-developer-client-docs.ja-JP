---
title: MAPI 戻り値のドキュメント
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
# <a name="mapi-return-value-documentation"></a><span data-ttu-id="15455-103">MAPI 戻り値のドキュメント</span><span class="sxs-lookup"><span data-stu-id="15455-103">MAPI Return Value Documentation</span></span>

  
  
<span data-ttu-id="15455-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15455-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15455-105">このリファレンス ドキュメントの参照エントリは、クライアント アプリケーションによる処理が必要な戻り値のみを示します。</span><span class="sxs-lookup"><span data-stu-id="15455-105">The reference entries in this Reference document only those return values that require some handling by client applications.</span></span> <span data-ttu-id="15455-106">一般的なエラー状態を示す値を返し、エラーの確認によって誘導される可能性がある値は、ドキュメントには含まれません。</span><span class="sxs-lookup"><span data-stu-id="15455-106">Return values that indicate common error conditions and can be deduced by checking for failure are not included in the documentation.</span></span> <span data-ttu-id="15455-107">たとえば、呼び出し元が入力パラメーターに間違ったMAPI_E_INVALID_PARAMETER指定した場合、多くのインターフェイス メソッドでエラーが返される場合があります。</span><span class="sxs-lookup"><span data-stu-id="15455-107">For example, many interface methods can return MAPI_E_INVALID_PARAMETER if a caller specifies the wrong value for an input parameter.</span></span> <span data-ttu-id="15455-108">この値は通常、MAPI_E_INVALID_PARAMETER を特に探す必要はないので、予期される戻り値のセットには表示されません。他のエラーとは異なる方法で処理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="15455-108">This value is typically not listed in the set of expected return values because there is no need to look specifically for MAPI_E_INVALID_PARAMETER and no need to process it differently from any other error.</span></span> <span data-ttu-id="15455-109">一方、一部のサービス プロバイダーはイベント通知をサポートしていないので **、IMAPISession** を通じてクライアントMAPI_E_NO_SUPPORT **Advise** メソッドに戻ります。</span><span class="sxs-lookup"><span data-stu-id="15455-109">On the other hand, some service providers do not support event notification and will return MAPI_E_NO_SUPPORT to the **Advise** method made by clients through **IMAPISession**.</span></span> <span data-ttu-id="15455-110">クライアントはこの値を明示的にチェックし、それが発生した場合に表す条件を処理するコードを提供する必要があるため、MAPI_E_NO_SUPPORT は [IMAPISession::Advise](imapisession-advise.md)の戻り値の一覧に含まれています。</span><span class="sxs-lookup"><span data-stu-id="15455-110">Because clients need to explicitly check for this value and provide code for handling the condition that it represents should it occur, MAPI_E_NO_SUPPORT is included in the list of return values for [IMAPISession::Advise](imapisession-advise.md).</span></span>
  
<span data-ttu-id="15455-111">次の表では、メソッドや関数から一般的に返されるエラー値について説明し、クライアントまたはサービス プロバイダーの部分で明示的な処理を必要とします。</span><span class="sxs-lookup"><span data-stu-id="15455-111">The following table describes error values that are commonly returned from methods and functions and require explicit handling on the part of a client or service provider.</span></span> <span data-ttu-id="15455-112">これらの値は、無効な入力データを示す値、リソースの問題を示す値、文字セットの互換性を示す値、不明な発生元のエラーを示す値の 4 つのカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="15455-112">These values fall into four categories: values that indicate invalid input data, values that indicate resource problems, values that indicate character set incompatibility, and values that indicate failure of an unknown origin.</span></span>
  
|<span data-ttu-id="15455-113">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="15455-113">**Return value**</span></span>|<span data-ttu-id="15455-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="15455-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15455-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15455-115">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="15455-116">メソッドまたは関数に渡された 1 つ以上のパラメーターが無効です。</span><span class="sxs-lookup"><span data-stu-id="15455-116">One or more of the parameters passed into the method or functions were not valid.</span></span>  <br/> |
|<span data-ttu-id="15455-117">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="15455-117">MAPI_E_UNKNOWN_FLAGS</span></span>  <br/> |<span data-ttu-id="15455-118">flags パラメーターの 1 つ以上の値が無効です。</span><span class="sxs-lookup"><span data-stu-id="15455-118">One or more values for a flags parameter were not valid.</span></span>  <br/> |
|<span data-ttu-id="15455-119">MAPI_E_DISK_ERROR</span><span class="sxs-lookup"><span data-stu-id="15455-119">MAPI_E_DISK_ERROR</span></span>  <br/> |<span data-ttu-id="15455-120">ディスクへの書き込みまたはディスクからの読み取りに問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="15455-120">There was a problem writing to or reading from disk.</span></span>  <br/> |
|<span data-ttu-id="15455-121">MAPI_E_NOT_ENOUGH_DISK</span><span class="sxs-lookup"><span data-stu-id="15455-121">MAPI_E_NOT_ENOUGH_DISK</span></span>  <br/> |<span data-ttu-id="15455-122">操作を完了するために使用できるディスク領域が足りなかった。</span><span class="sxs-lookup"><span data-stu-id="15455-122">Not enough disk space was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="15455-123">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="15455-123">MAPI_E_NOT_ENOUGH_MEMORY</span></span>  <br/> |<span data-ttu-id="15455-124">操作を完了するのに十分なメモリが使用できません。</span><span class="sxs-lookup"><span data-stu-id="15455-124">Not enough memory was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="15455-125">MAPI_E_NOT_ENOUGH_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="15455-125">MAPI_E_NOT_ENOUGH_RESOURCES</span></span>  <br/> |<span data-ttu-id="15455-126">操作を完了するのに十分なシステム リソースが使用できません。</span><span class="sxs-lookup"><span data-stu-id="15455-126">Not enough system resources were available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="15455-127">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="15455-127">MAPI_E_BAD_CHARWIDTH</span></span>  <br/> |<span data-ttu-id="15455-128">非互換性は、呼び出し元と実装でサポートされる文字セットに存在します。</span><span class="sxs-lookup"><span data-stu-id="15455-128">An incompatibility exists in the character sets supported by the caller and the implementation.</span></span>  <br/> |
|<span data-ttu-id="15455-129">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="15455-129">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="15455-130">予期しない、または不明な発生源のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="15455-130">An error of unexpected or unknown origin occurred.</span></span>  <br/> |
   
<span data-ttu-id="15455-131">MAPI 戻り値を表す定数は、MAPICODE に一覧表示されます。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="15455-131">The constants that represent MAPI return values are listed in the MAPICODE.H header file.</span></span> <span data-ttu-id="15455-132">定数の一部は Win32 エラーにマップされます。これらの定数と数値のマッピングは、Win32 ヘッダー ファイル WINERROR.H で確認できます。</span><span class="sxs-lookup"><span data-stu-id="15455-132">Some of the constants map to Win32 errors; the mapping of these constants to numeric values can be found in the Win32 header file, WINERROR.H.</span></span>
  
<span data-ttu-id="15455-133">呼び出し元によって渡された無効なデータに関するエラーは、MAPI によって提供されるパラメーター検証 API 関数または一連のマクロを使用して判断できます。</span><span class="sxs-lookup"><span data-stu-id="15455-133">Errors regarding invalid data passed in by a caller can be determined through either the parameter validation API functions provided by MAPI or a set of macros.</span></span> 
  
<span data-ttu-id="15455-134">文字セットの非互換性は、次のいずれかの状況が発生した場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="15455-134">Character set incompatibility arises when either of the following situations occurs:</span></span>
  
- <span data-ttu-id="15455-135">クライアントまたはサービス プロバイダーは、メソッドMAPI_UNICODE呼び出しでこのフラグを設定し、実装は Unicode をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="15455-135">A client or service provider sets the MAPI_UNICODE flag on a method or function call and the implementation does not support Unicode.</span></span> <span data-ttu-id="15455-136">このMAPI_UNICODEは、入力として渡される文字列が Unicode 文字列であり、出力として返される文字列が Unicode 文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="15455-136">Setting MAPI_UNICODE indicates that character strings passed in as input are Unicode strings and that character strings passed back as output are expected to be Unicode strings.</span></span>
    
- <span data-ttu-id="15455-137">クライアントまたはサービス プロバイダーは、メソッドまたは関数呼び出しMAPI_UNICODEフラグを設定しません。実装は Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="15455-137">A client or service provider does not set the MAPI_UNICODE flag on a method or function call and the implementation only supports Unicode.</span></span>
    

