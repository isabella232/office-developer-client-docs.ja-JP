---
title: Visual C++ でエラーを処理する
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8feeb97e049d245da91371fdb5225a644d0e415
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477118"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="8fa6e-102">Visual C++ でエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="8fa6e-102">Handling Errors in Visual C++</span></span>


<span data-ttu-id="8fa6e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fa6e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8fa6e-104">COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターン コードを返します。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="8fa6e-105">\#のインポート ディレクティブは、各「生」のメソッドまたはプロパティをラッパー コードを生成し、返された HRESULT を確認します。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="8fa6e-106">ラッパー コードが呼び出すことによって COM エラーをスローする HRESULT は、エラーを示している場合\_com\_問題\_の errorex() には、引数としてコードが返されます。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="8fa6e-107">COM エラー オブジェクトは、 **try-catch**ブロックでキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="8fa6e-108">(効率のためへの参照をキャッチ、 \_com\_エラー オブジェクトです)。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="8fa6e-p102">ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="8fa6e-111">\#のインポート ディレクティブだけのメソッドとプロパティは、ADO .dll で宣言されているエラー処理ルーチンを作成します。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="8fa6e-112">しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="8fa6e-113">例については、トピック「Visual C++ Extensions」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8fa6e-113">See the topic Visual C++ Extensions for examples.</span></span>

