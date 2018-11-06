---
title: ADO ファミリのライブラリ
TOCTitle: The ADO family of libraries
ms:assetid: 9e794509-d0a8-2e5b-02a8-65e26f059c4e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249724(v=office.15)
ms:contentKeyID: 48546656
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 821de4312d3fa76468311305b18eaaa156e05318
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999044"
---
# <a name="the-ado-family-of-libraries"></a>ADO ファミリのライブラリ

**適用されます**Access 2013、Office 2013。

ADO ファミリは、ADO (RDS を含む)、ADO MD、および ADOX という 3 つの主要ライブラリで構成されています。

## <a name="ado"></a>ADO

ADO により、クライアント アプリケーションが、OLE DB プロバイダーを通じてデータベース サーバーのデータにアクセスし、これを処理できるようになります。 ADO の主な利点は、使用が簡単で、高速に動作し、メモリのオーバーヘッドが小さく、ディスクの使用量が少ないことです。 ADO には、クライアント/サーバーおよび web ベースのアプリケーションを構築するための主要な機能がサポートされています。

ADO では、リモート データ サービス (RDS) をサーバーからクライアント アプリケーションまたは web ページへのデータは、クライアント上のデータを操作し、ラウンド トリップで 1 つのサーバーに更新プログラムを返すを移動することができますが機能もあります。

## <a name="ado-md"></a>ADO MD

Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) により、Microsoft Visual Basic、Microsoft Visual C++、Microsoft Visual J++ などの言語から、多次元データに簡単にアクセスできるようになります。ADO MD は、ADO を拡張して、 **CubeDef** オブジェクトや **Cellset** オブジェクトなどの多次元データ専用オブジェクトを使用できるようにしたものです。ADO MD を使用すると、多次元スキーマを参照し、キューブを照会して、その結果を取得できます。

ADO と同様、ADO MD でも、基になる OLE DB プロバイダーを使用してデータにアクセスします。ADO MD を使用して作業するには、プロバイダーが OLE DB for OLAP 仕様で定義された多次元データ プロバイダー (MDP) である必要があります。MDP は、データを表形式のビューで表示する表形式データ プロバイダー (TDP) とは異なり、データを多次元のビューで表示します。使用する OLE DB for OLAP プロバイダーでサポートされている具体的な構文または動作の詳細については、そのプロバイダーのドキュメントを参照してください。

## <a name="adox"></a>ADOX

Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO のオブジェクトとプログラミング モデルを拡張したものです。ADOX には、セキュリティのためのオブジェクトに加え、スキーマの作成および修正のためのオブジェクトが用意されています。ADOX では、オブジェクト ベースの手法を使用してスキーマを操作するため、使用される構文の違いにかかわらず、さまざまなデータ ソースで動作するコードを記述できます。

ADOX は、ADO のコア オブジェクトに添付されるライブラリで、テーブルやプロシージャなどのスキーマ オブジェクトを作成、修正、および削除するための追加のオブジェクトを公開します。また、ユーザーとグループを管理したり、オブジェクトに対する権限を付与および削除したりするためのセキュリティ オブジェクトも備えています。

