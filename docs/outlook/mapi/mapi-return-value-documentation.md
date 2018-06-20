---
title: MAPI の戻り値のドキュメント
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801449"
---
# <a name="mapi-return-value-documentation"></a><span data-ttu-id="49192-103">MAPI の戻り値のドキュメント</span><span class="sxs-lookup"><span data-stu-id="49192-103">MAPI Return Value Documentation</span></span>

  
  
<span data-ttu-id="49192-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="49192-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="49192-105">この参照の参照のエントリは、クライアント アプリケーションによっていくつかの処理を必要とする戻り値だけを文書化します。</span><span class="sxs-lookup"><span data-stu-id="49192-105">The reference entries in this Reference document only those return values that require some handling by client applications.</span></span> <span data-ttu-id="49192-106">共通のエラー条件を指定してエラーを確認することで推定できますが、戻り値は、ドキュメントには含まれません。</span><span class="sxs-lookup"><span data-stu-id="49192-106">Return values that indicate common error conditions and can be deduced by checking for failure are not included in the documentation.</span></span> <span data-ttu-id="49192-107">などの多くのインターフェイスのメソッドは、呼び出し元が入力パラメーターに間違った値を指定した場合、MAPI_E_INVALID_PARAMETER を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="49192-107">For example, many interface methods can return MAPI_E_INVALID_PARAMETER if a caller specifies the wrong value for an input parameter.</span></span> <span data-ttu-id="49192-108">この値は通常表示されない予期される戻り値のセットで MAPI_E_INVALID_PARAMETER 用に特別に確認する必要があると、他のエラーから異なる方法で処理する必要はありませんがないためです。</span><span class="sxs-lookup"><span data-stu-id="49192-108">This value is typically not listed in the set of expected return values because there is no need to look specifically for MAPI_E_INVALID_PARAMETER and no need to process it differently from any other error.</span></span> <span data-ttu-id="49192-109">その一方で、サービス プロバイダーによってはイベント通知をサポートしていないと、 **IMAPISession**によって、クライアントが**アドバイズ**メソッドに MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="49192-109">On the other hand, some service providers do not support event notification and will return MAPI_E_NO_SUPPORT to the **Advise** method made by clients through **IMAPISession**.</span></span> <span data-ttu-id="49192-110">クライアントは、明示的にこの値をチェックし、その条件を処理するためのコードにする必要がありますを提供する必要があるために発生する、MAPI_E_NO_SUPPORT は[IMAPISession::Advise](imapisession-advise.md)の戻り値の一覧に含まれています。</span><span class="sxs-lookup"><span data-stu-id="49192-110">Because clients need to explicitly check for this value and provide code for handling the condition that it represents should it occur, MAPI_E_NO_SUPPORT is included in the list of return values for [IMAPISession::Advise](imapisession-advise.md).</span></span>
  
<span data-ttu-id="49192-111">次の表では、メソッドおよび関数から返される通常し、クライアントまたはサービス プロバイダー側で明示的な処理を必要とするエラー値について説明します。</span><span class="sxs-lookup"><span data-stu-id="49192-111">The following table describes error values that are commonly returned from methods and functions and require explicit handling on the part of a client or service provider.</span></span> <span data-ttu-id="49192-112">これらの値は次の 4 つのカテゴリに分類されます: 無効な入力データを示す値、リソースの問題を示す、文字セットの非互換性を示す値と値を原因不明のエラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="49192-112">These values fall into four categories: values that indicate invalid input data, values that indicate resource problems, values that indicate character set incompatibility, and values that indicate failure of an unknown origin.</span></span>
  
|<span data-ttu-id="49192-113">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="49192-113">**Return value**</span></span>|<span data-ttu-id="49192-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="49192-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49192-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49192-115">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="49192-116">1 つ以上のパラメーターがメソッドに渡される、または機能が無効であった。</span><span class="sxs-lookup"><span data-stu-id="49192-116">One or more of the parameters passed into the method or functions were not valid.</span></span>  <br/> |
|<span data-ttu-id="49192-117">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="49192-117">MAPI_E_UNKNOWN_FLAGS</span></span>  <br/> |<span data-ttu-id="49192-118">Flags パラメーターの 1 つまたは複数の値が無効でした。</span><span class="sxs-lookup"><span data-stu-id="49192-118">One or more values for a flags parameter were not valid.</span></span>  <br/> |
|<span data-ttu-id="49192-119">MAPI_E_DISK_ERROR</span><span class="sxs-lookup"><span data-stu-id="49192-119">MAPI_E_DISK_ERROR</span></span>  <br/> |<span data-ttu-id="49192-120">書き込みまたはディスクからの読み取りに問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="49192-120">There was a problem writing to or reading from disk.</span></span>  <br/> |
|<span data-ttu-id="49192-121">MAPI_E_NOT_ENOUGH_DISK</span><span class="sxs-lookup"><span data-stu-id="49192-121">MAPI_E_NOT_ENOUGH_DISK</span></span>  <br/> |<span data-ttu-id="49192-122">十分なディスク領域は、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="49192-122">Not enough disk space was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="49192-123">MAPI_E_NOT_ENOUGH_MEMORY</span><span class="sxs-lookup"><span data-stu-id="49192-123">MAPI_E_NOT_ENOUGH_MEMORY</span></span>  <br/> |<span data-ttu-id="49192-124">十分なメモリ操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="49192-124">Not enough memory was available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="49192-125">MAPI_E_NOT_ENOUGH_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="49192-125">MAPI_E_NOT_ENOUGH_RESOURCES</span></span>  <br/> |<span data-ttu-id="49192-126">十分なシステム リソースは、操作を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="49192-126">Not enough system resources were available to complete the operation.</span></span>  <br/> |
|<span data-ttu-id="49192-127">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="49192-127">MAPI_E_BAD_CHARWIDTH</span></span>  <br/> |<span data-ttu-id="49192-128">互換性の問題は、呼び出し元との実装でサポートされている文字セットに存在します。</span><span class="sxs-lookup"><span data-stu-id="49192-128">An incompatibility exists in the character sets supported by the caller and the implementation.</span></span>  <br/> |
|<span data-ttu-id="49192-129">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="49192-129">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="49192-130">予期しない、または不明な発生元のエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="49192-130">An error of unexpected or unknown origin occurred.</span></span>  <br/> |
   
<span data-ttu-id="49192-131">MAPICODE は、MAPI の戻り値を表す定数の一覧です。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="49192-131">The constants that represent MAPI return values are listed in the MAPICODE.H header file.</span></span> <span data-ttu-id="49192-132">マップ クラスの定数の Win32 エラーです。数値を指定するこれらの定数へのマッピングは、Win32 ヘッダー ファイル、WINERROR を参照しています。H.</span><span class="sxs-lookup"><span data-stu-id="49192-132">Some of the constants map to Win32 errors; the mapping of these constants to numeric values can be found in the Win32 header file, WINERROR.H.</span></span>
  
<span data-ttu-id="49192-133">パラメーター検証 API 関数のいずれか MAPI またはマクロのセットによって提供される、呼び出し元によって渡される、無効なデータに関するエラーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="49192-133">Errors regarding invalid data passed in by a caller can be determined through either the parameter validation API functions provided by MAPI or a set of macros.</span></span> 
  
<span data-ttu-id="49192-134">文字セットの非互換性が発生した次のいずれかが発生したとき。</span><span class="sxs-lookup"><span data-stu-id="49192-134">Character set incompatibility arises when either of the following situations occurs:</span></span>
  
- <span data-ttu-id="49192-135">クライアントまたはサービス プロバイダーは、メソッドまたは関数の呼び出しに MAPI_UNICODE フラグを設定し、実装は Unicode をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="49192-135">A client or service provider sets the MAPI_UNICODE flag on a method or function call and the implementation does not support Unicode.</span></span> <span data-ttu-id="49192-136">設定 MAPI_UNICODE は、入力として渡される文字列が Unicode 文字列と、出力として渡される文字列が Unicode 文字列であると予測されることを示します。</span><span class="sxs-lookup"><span data-stu-id="49192-136">Setting MAPI_UNICODE indicates that character strings passed in as input are Unicode strings and that character strings passed back as output are expected to be Unicode strings.</span></span>
    
- <span data-ttu-id="49192-137">クライアントまたはサービス プロバイダーはメソッドまたは関数の呼び出しに MAPI_UNICODE フラグを設定しないと、実装には、Unicode のみサポートしています。</span><span class="sxs-lookup"><span data-stu-id="49192-137">A client or service provider does not set the MAPI_UNICODE flag on a method or function call and the implementation only supports Unicode.</span></span>
    

