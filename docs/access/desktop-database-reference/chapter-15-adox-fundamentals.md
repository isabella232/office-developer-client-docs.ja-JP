---
title: '第 15 章: ADOX の基本事項'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 952599694588c5535d8d6d9e205e45d67b8b3020
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627094"
---
# <a name="chapter-15-adox-fundamentals"></a>第 15 章: ADOX の基本事項

**適用先**: Access 2013、Office 2013

Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO のオブジェクトとプログラミング モデルを拡張したものです。ADOX には、セキュリティのためのオブジェクトに加え、スキーマの作成および修正のためのオブジェクトが用意されています。ADOX では、オブジェクト ベースの手法を使用してスキーマを操作するため、使用される構文の違いにかかわらず、さまざまなデータ ソースで動作するコードを記述できます。

ADOX は、ADO のコア オブジェクトに添付されるライブラリで、テーブルやプロシージャなどのスキーマ オブジェクトを作成、修正、および削除するための追加のオブジェクトを公開します。また、ユーザーとグループを管理したり、オブジェクトに対する権限を付与および削除したりするためのセキュリティ オブジェクトも備えています。

開発ツールで ADOX を使用するには、ADOX タイプ ライブラリへの参照を確立する必要があります。ADOX ライブラリとは、Microsoft ADO Ext. for DDL and Security のことです。ADOX ライブラリのファイル名は Msadox.dll で、プログラム ID (ProgID) は "ADOX" です。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。

Microsoft OLE DB Provider for the Microsoft Jet Database Engine は、ADOX を完全にサポートしています。データ プロバイダーによっては、ADOX の特定の機能がサポートされていない場合があります。Microsoft OLE DB Provider for ODBC、Microsoft OLE DB Provider for Oracle、または Microsoft SQL Server OLE DB Provider でサポートされている機能に関する詳細については、MDAC の Readme ファイルを参照してください。

このドキュメントでは、プログラミング言語に関する Microsoft Visual Basic知識と ADO に関する一般的な知識を前提とします。 ADO の詳細については、「ADO プログラマ ガイド [」を参照してください](ado-programmer-s-guide.md)。

この章では、次のトピックについて説明します。

- [ADOX のプロバイダー サポート](provider-support-for-adox.md)

ADOX に関する概要については、次のトピックを参照してください。

- [ADOX のオブジェクト](adox-objects.md)
- [ADOX のコレクション](adox-collections.md)
- [ADOX のプロパティ](adox-properties.md)
- [ADOX のメソッド](adox-methods.md)
- [ADOX の例](adox-code-examples.md)

