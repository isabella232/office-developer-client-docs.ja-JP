---
title: Microsoft Exchange データソースドライバーの初期化
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291408"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Microsoft Exchange データソースドライバーの初期化

**適用先:** Access 2013、Office 2013

microsoft Exchange データソースドライバーをインストールすると、セットアッププログラムによって、エンジンおよび ISAM 形式のサブキーに、microsoft Windows レジストリに既定値のセットが書き込まれます。 これらの設定は直接変更しないでください。アプリケーションのセットアッププログラムを使用して、これらの設定を追加、削除、または変更します。 次のセクションでは、Microsoft Exchange データソースドライバーの初期化および ISAM 形式の設定について説明します。

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Microsoft Exchange データソースの初期設定

**access Connectivity Engine Engine\\\\Exchange**フォルダーには、microsoft Outlook および microsoft Exchange フォルダーへの外部アクセスに使用される Aceexch ドライバーの初期化設定が含まれています。 このキーのエントリは 1 つだけで、その設定は次のようになっています。

`win32=<path>\ACEEXCH.DLL`

Microsoft Access データベース エンジンは、この設定を使用して Aceexch.dll の格納場所を示します。 このフル パスはインストール時に決まります。 値の型は REG\_SZ です。

Microsoft Outlook の ISAM 形式の使用結果と Microsoft Exchange クライアントの ISAM 形式の使用結果は似ています。唯一の違いは、異なる 2 つのクライアントが、同じ列に異なる名前を使用することです。2 つの ISAM 形式は、Microsoft Access データベース エンジンがユーザーの望む特定のスタイルで列名を返すことができるように作られています。

## <a name="microsoft-outlook-client-isam-formats"></a>Microsoft Outlook クライアントの ISAM 形式

**Access Connectivity Engine\\ISAM 形式\\Outlook 9.0**フォルダーには、次のエントリが含まれています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>importfilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook ()</p></td>
</tr>
<tr class="odd">
<td><p>canlink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
<tr class="even">
<td><p>onetableperfile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1/3</p></td>
</tr>
<tr class="even">
<td><p>indexdialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>createdbonexport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>supportslongnames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。



## <a name="microsoft-exchange-client-isam-formats"></a>Microsoft Exchange クライアントの ISAM 形式

**Access Connectivity Engine\\ISAM 形式\\の Exchange 4.0**フォルダーには、次のエントリが含まれています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>importfilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange ()</p></td>
</tr>
<tr class="odd">
<td><p>canlink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
<tr class="even">
<td><p>onetableperfile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>isamtype</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1/3</p></td>
</tr>
<tr class="even">
<td><p>indexdialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="odd">
<td><p>createdbonexport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>supportslongnames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>atl-fs-01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Outlook および Exchange データ用の schema.ini ファイルのカスタマイズ

Schema.ini ファイルは、テキストの ISAM で使用されるのと同様の方法で、Microsoft Outlook と Microsoft Exchange の ISAM でも使用されます。Schema.ini には、データの書式化方法、アクセスされる列名など、データ ソースの仕様が記述されています。

Outlook や Exchange で、データの読み込み、インポート、またはエクスポートを行う前に、Schema.ini ファイルを変更する必要はありません。Outlook と Exchange のための Schema.ini ファイル内の設定の多くは、MAPI が必要とする内部タグに特有のものです。これらのタグの値は変更しないでください。

