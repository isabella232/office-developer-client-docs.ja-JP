---
title: '第 12 章: RDS チュートリアル'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9455d7b2a9df98671f8ce6f9d8a939fcadc56f79
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936946"
---
# <a name="chapter-12-rds-tutorial"></a>第 12 章: RDS チュートリアル


**適用されます**Access 2013、Office 2013。

このチュートリアルでは、RDS プログラミング モデルを使用してデータ ソースのクエリおよび更新を行う方法について説明します。 最初に、このタスクの実行に必要な手順を説明します。 Microsoft Visual Basic Scripting Edition および Microsoft Visual J では、ADO の Windows Foundation クラス (ADO/WFC) が特徴で、チュートリアルが繰り返されます。

このチュートリアルは、次の 2 つの理由から、複数の言語でコーディングされています。

- RDS の文書は、Visual Basic でのコーディングを前提にしています。そのため、Visual Basic のプログラマには便利ですが、他の言語を使用するプログラマには不便な場合があります。

- RDS の特定の機能についてわからない場合に、他の言語について多少の知識があれば、他の言語で記述された同じ機能を参照することによって問題を解決できる可能性があります。

## <a name="how-the-tutorial-is-presented"></a>チュートリアルを表示する方法

このチュートリアルは、RDS プログラミング モデルに基づいています。プログラミング モデルの各手順を 1 つずつ説明します。さらに、それぞれの手順に Visual Basic コードの一部を示してあります。

他の言語についても、コード例を最小限の説明と共に取り上げています。各プログラム言語のチュートリアルの手順には、プログラミング モデルとチュートリアルの説明にある手順に対応する番号が付いています。この手順番号を利用して、対応するチュートリアルの説明を参照してください。

RDS プログラミング モデルについて、次に説明します。チュートリアルを使用するうえでのガイドラインとして使用してください。

## <a name="rds-programming-model-with-objects"></a>オブジェクトと、RDS プログラミング モデル

- サーバーで呼び出されるプログラムを指定し、クライアントからそのプログラムを参照するための経路 (プロキシ) を取得します。

- サーバー プログラムを呼び出します。データ ソースおよび発行するコマンドを識別するためのパラメーターをサーバー プログラムに渡します。

- サーバー プログラムは、データ ソースから [Recordset](recordset-object-ado.md) オブジェクトを取得します。通常は ADO を使用して取得します。また、サーバー上で **Recordset** オブジェクトを処理することもできます。

- サーバー プログラムは、結果の **Recordset** オブジェクトをクライアント アプリケーションに返します。

- クライアント側では、ビジュアル コントロールを使用すると、必要に応じてフォームに **Recordset** オブジェクトを簡単に配置できます。

- **Recordset** オブジェクトに加えられた変更がサーバーに送り返され、その変更がデータ ソースに反映されます。

このチュートリアルの手順は、以下です。

- [手順 1: サーバー プログラムを指定します。](step-1-specify-a-server-program-rds-tutorial.md)
- [手順 2: サーバー プログラムを呼び出す](step-2-invoke-the-server-program-rds-tutorial.md)
- [手順 3: サーバーが Recordset を取得します。](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [手順 4: サーバーは、レコード セットを返します。](step-4-server-returns-the-recordset-rds-tutorial.md)
- [手順 5: DataControl 行われる使用可能です](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [手順 6: 変更は、サーバーに送信されます。](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [RDS チュートリアル (VBScript)](rds-tutorial-vbscript.md)
- [RDS チュートリアル (Visual j)](rds-tutorial-visual-j.md)