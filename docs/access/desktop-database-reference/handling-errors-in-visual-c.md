---
title: Visual C++ でのエラー処理
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bb499b24b151f93d68ef28594217f6707bb48b34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615446"
---
# <a name="handling-errors-in-visual-c"></a>Visual C++ でのエラー処理


**適用先**: Access 2013、Office 2013

COM では、ほとんどの操作は、関数が正常に完了したかどうかを示す HRESULT 戻りコードを返します。 import ディレクティブは、各 "raw" メソッドまたはプロパティの周囲にラッパー コードを生成し、返される \# HRESULT をチェックします。 HRESULT がエラーを示す場合、ラッパー コードは、HRESULT 戻りコードを引数として com issue errorex() を呼び出すことによって \_ \_ COM \_ エラーをスローします。 COM エラー オブジェクトは **、try-catch ブロックでキャッチ** できます。 (効率を高めるには、com エラー オブジェクトへの参照 \_ を \_ キャッチします)。

ここでは、発生するエラーは ADO エラーです。ADO エラーは、ADO 操作の失敗によって発生します。基になるプロバイダーによって返されたエラーは、 **Connection** オブジェクトの **Errors** コレクションに **Error** オブジェクトとして格納されます。

import ディレクティブは、ADO プロパティで宣言されたメソッドとプロパティのエラー処理ルーチン \# のみを作成.dll。 しかし、独自のエラー チェック マクロやインライン関数を記述することにより、上記と同じエラー処理機構を利用できます。 例については、トピック「Visual C++ Extensions」を参照してください。

