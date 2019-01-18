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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709475"
---
# <a name="handling-errors-in-visual-c"></a>Visual C++ でのエラー処理


**適用されます**Access 2013、Office 2013。

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターン コードを返します。 \#のインポート ディレクティブは、各「生」のメソッドまたはプロパティをラッパー コードを生成し、返された HRESULT を確認します。 ラッパー コードが呼び出すことによって COM エラーをスローする HRESULT は、エラーを示している場合\_com\_問題\_の errorex() には、引数としてコードが返されます。 COM エラー オブジェクトは、 **try-catch**ブロックでキャッチできます。 (効率のためへの参照をキャッチ、 \_com\_エラー オブジェクトです)。

ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。

\#のインポート ディレクティブだけのメソッドとプロパティは、ADO .dll で宣言されているエラー処理ルーチンを作成します。 しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。 例については、トピック「Visual C++ Extensions」を参照してください。

