---
title: Visual C++ でエラーを処理する
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 937454a9277ec219f25a79074833138f6dd7f535
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887572"
---
# <a name="handling-errors-in-visual-c"></a>Visual C++ でエラーを処理する


**適用されます**Access 2013、Office 2013。

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターン コードを返します。 \#のインポート ディレクティブは、各「生」のメソッドまたはプロパティをラッパー コードを生成し、返された HRESULT を確認します。 ラッパー コードが呼び出すことによって COM エラーをスローする HRESULT は、エラーを示している場合\_com\_問題\_の errorex() には、引数としてコードが返されます。 COM エラー オブジェクトは、 **try-catch**ブロックでキャッチできます。 (効率のためへの参照をキャッチ、 \_com\_エラー オブジェクトです)。

ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。

\#のインポート ディレクティブだけのメソッドとプロパティは、ADO .dll で宣言されているエラー処理ルーチンを作成します。 しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。 例については、トピック「Visual C++ Extensions」を参照してください。

