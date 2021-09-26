---
title: Microsoft ActiveX データ オブジェクト リファレンス
TOCTitle: Microsoft ActiveX Data Objects Reference
ms:assetid: 235fc575-8a2e-913c-fa3d-bb86256733f9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249010(v=office.15)
ms:contentKeyID: 48543728
ms.date: 09/18/2021
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 0a6e7090b1be0e5c31d670e7ff5c524f8c68e8cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606612"
---
# <a name="microsoft-activex-data-objects-reference"></a>Microsoft ActiveX データ オブジェクト リファレンス

**適用先:** Access 2013、Office 2013

## <a name="purpose"></a>用途

Microsoft ActiveX Data Objects (ADO) により、クライアント アプリケーションが、OLE DB プロバイダーを通じてデータベース サーバーのデータにアクセスし、これを操作できるようになります。ADO の主な利点は、使用が簡単で、高速に動作し、メモリのオーバーヘッドが小さく、ディスクの使用量が少ないことです。ADO では、クライアント/サーバー アプリケーションおよび Web ベース アプリケーションを構築するための重要な機能がサポートされています。

## <a name="rds"></a>RDS

ADO は、リモート データ サービス (RDS) の機能も備えています。これにより、データをサーバーからクライアント アプリケーションまたは Web ページへ移動し、クライアント側でデータを操作し、更新をサーバーに送り返すという操作を、1 回の往復処理で実行できます。

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) により、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から、多次元データに簡単にアクセスできるようになります。ADO MD は、Microsoft ActiveX Data Objects (ADO) を拡張して、CubeDef オブジェクトや Cellset オブジェクトなどの多次元データ専用オブジェクトを使用できるようにしたものです。ADO MD を使用すると、多次元スキーマを参照し、キューブを照会して、その結果を取得できます。

ADO と同様、ADO MD でも、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用して作業するためには、プロバイダーが OLE DB for OLAP の仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式のビューで表示する表形式データ プロバイダー (TDP) とは異なり、データを多次元のビューで表示します。使用する OLAP OLE DB プロバイダーでサポートされている具体的な構文や動作の詳細については、そのプロバイダーのドキュメントを参照してください。

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO のオブジェクトとプログラミング モデルを拡張したものです。ADOX には、セキュリティのためのオブジェクトに加え、スキーマの作成および修正のためのオブジェクトが用意されています。ADOX では、オブジェクト ベースの手法を使用してスキーマを操作するため、使用される構文の違いにかかわらず、さまざまなデータ ソースで動作するコードを記述できます。

ADOX は、ADO のコア オブジェクトに添付されるライブラリで、テーブルやプロシージャなどのスキーマ オブジェクトを作成、修正、および削除するための追加のオブジェクトを公開します。また、ユーザーとグループを管理したり、オブジェクトに対する権限を付与および削除したりするためのセキュリティ オブジェクトも備えています。

## <a name="ado-25-main-components"></a>ADO 2.5 メイン コンポーネント

- [プログラマー ガイド](ado-programmer-s-guide.md): ADO、RDS、ADO MD、および ADOX の使用方法の概要について説明します。

- [Programmer's reference](ado-programmer-s-reference-topics.md): この ADO のドキュメントのセクションには、ADO、RDS、ADO MD、および ADOX の各オブジェクト、コレクション、プロパティ、動的プロパティ、メソッド、イベント、および列挙型に関するトピックが含まれています。
