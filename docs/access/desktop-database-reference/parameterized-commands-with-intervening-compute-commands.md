---
title: 計算の間にあるコマンドを使用してパラメーター化されたコマンド
TOCTitle: Parameterized commands with intervening COMPUTE commands
ms:assetid: ff3724cd-040b-4b5f-bb9b-e6a38fd938c9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250311(v=office.15)
ms:contentKeyID: 48548959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76093082419684cd236f4766da6afc07faf2cf20
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946798"
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>計算の間にあるコマンドを使用してパラメーター化されたコマンド


**適用されます**Access 2013、Office 2013。

通常、パラメーター化された Shape APPEND コマンドには、クエリ コマンドを使って親 **Recordset** を作成する句と、パラメーター化されたクエリ コマンド (パラメーター プレースホルダーである疑問符 "?" を含んでいるコマンド) を使って子 **Recordset** を作成する別の句があります。そのため、シェイプされた **Recordset** には、上位レベルに親、下位レベルに子の、2 つのレベルがあります。

子 **Recordset** を作成する句は、任意の数の入れ子になった Shape COMPUTE コマンドにすることができ、入れ子の最も深いレベルのコマンドにパラメーター化されたクエリを含めます。シェイプされた **Recordset** は複数のレベルを持ち、親が最上位レベルを、子が最下位レベルを占め、Shape COMPUTE コマンドによって生成された任意の数の **Recordset** が中間のレベルを占めます。

この機能の典型的な使用例は、集計関数と Shape COMPUTE コマンドのグループ化機能を呼び出して、子 **Recordset** に関する分析情報を含む中間の **Recordset** を作成する場合です。また、これはパラメーター化された Shape コマンドであるため、親のチャプター列にアクセスするたびに新しい子 **Recordset** が取得されます。中間のレベルは子から派生するため、これらのレベルも再計算されます。

