---
title: '15 章:  ADOX に関する基本事項'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3869f23b93df78fd207812a85f91dd3272bd255f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479267"
---
# <a name="chapter-15-adox-fundamentals"></a>15 章: ADOX に関する基本事項


**適用されます**Access 2013 |。Office 2013

Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO オブジェクトおよびプログラミング モデルの拡張機能です。ADOX には、セキュリティに加え、スキーマの作成および変更のためのオブジェクトが含まれます。オブジェクト ベースでスキーマ操作が行われるため、さまざまなデータ ソースに対してそれぞれの文法の違いに関係なく動作するコードを記述することができます。

ADOX は、コア ADO オブジェクトに付随するライブラリです。これにより、テーブルやプロシージャなどのスキーマ オブジェクトの作成、修正、および削除のための追加オブジェクトが提供されます。これにはまた、ユーザーおよびグループを管理し、オブジェクトに対する権限を与えたり取り消すためのセキュリティ オブジェクトも含まれます。

開発ツールで ADOX を使用するには、ADOX タイプ ライブラリへの参照を確立する必要があります。ADOX ライブラリとは、Microsoft ADO Ext. for DDL and Security のことです。ADOX ライブラリのファイル名は Msadox.dll で、プログラム ID (ProgID) は "ADOX" です。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。

Microsoft OLE DB Provider for the Microsoft Jet Database Engine は、ADOX を完全にサポートしています。データ プロバイダーによっては、ADOX の特定の機能がサポートされていない場合があります。Microsoft OLE DB Provider for ODBC、Microsoft OLE DB Provider for Oracle、または Microsoft SQL Server OLE DB Provider でサポートされている機能に関する詳細については、MDAC の Readme ファイルを参照してください。

このドキュメントは、Microsoft® Visual Basic® のプログラミング言語を使用できる知識および ADO に関する一般的な知識を持っていることを前提としています。ADO の詳細については、「[ADO プログラマ ガイド](ado-programmer-s-guide.md)」を参照してください。ADOX に関する概要については、次のトピックを参照してください。

  - [ADOX オブジェクト](adox-objects.md)

  - [ADOX コレクション](adox-collections.md)

  - [ADOX のプロパティ](adox-properties.md)

  - [ADOX メソッド](adox-methods.md)

  - [ADOX コードの例](adox-code-examples.md)

