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
# <a name="handling-errors-in-visual-c"></a>Visual C++ でのエラー処理


**適用先:** Access 2013、Office 2013

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT リターンコードを返します。 import \#ディレクティブは、各 "raw" メソッドまたはプロパティの前後にラッパーコードを生成し、返された HRESULT をチェックします。 hresult が失敗を示している場合、ラッパーコードは、hresult リターン\_コード\_を\_引数として com 問題 errorex () を呼び出すことによって com エラーをスローします。 COM エラーオブジェクトは、 **try-catch**ブロックでキャッチできます。 (効率を上げるために、 \_com\_error オブジェクトへの参照をキャッチします)。

ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。

import \#ディレクティブは、ADO .dll で宣言されているメソッドおよびプロパティに対してのみエラー処理ルーチンを作成します。 しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。 例については、トピック「Visual C++ Extensions」を参照してください。

