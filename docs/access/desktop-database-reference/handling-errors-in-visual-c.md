---
title: Visual C++ でのエラー処理
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292028"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="4aa9e-102">Visual C++ でのエラー処理</span><span class="sxs-lookup"><span data-stu-id="4aa9e-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="4aa9e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4aa9e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4aa9e-104">COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターンコードを返します。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="4aa9e-105">import \#ディレクティブは、各 "raw" メソッドまたはプロパティの前後にラッパーコードを生成し、返された HRESULT をチェックします。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="4aa9e-106">hresult が失敗を示している場合、ラッパーコードは、hresult リターン\_コード\_を\_引数として com 問題 errorex () を呼び出すことによって com エラーをスローします。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="4aa9e-107">COM エラーオブジェクトは、 **try-catch**ブロックでキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="4aa9e-108">(効率を上げるために、 \_com\_error オブジェクトへの参照をキャッチします)。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="4aa9e-p102">ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="4aa9e-111">import \#ディレクティブは、ADO .dll で宣言されているメソッドおよびプロパティに対してのみエラー処理ルーチンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="4aa9e-112">しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="4aa9e-113">例については、トピック「Visual C++ Extensions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4aa9e-113">See the topic Visual C++ Extensions for examples.</span></span>

