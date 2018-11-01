---
title: ActiveX データ オブジェクトを使用します。
TOCTitle: Use ActiveX Data Objects
description: Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887510"
---
# <a name="use-activex-data-objects"></a>ActiveX データ オブジェクトを使用します。

**適用されます**Access 2013、Office 2013。

Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。

## <a name="microsoft-activex-data-objects-ado"></a>ADO (ActiveX データ オブジェクト)

ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>DDL とセキュリティ (ADOX) の ADO の拡張

ADOX には、新しいデータベースを作成するために必要なデータ定義言語 (DDL) オブジェクト、およびセキュリティを管理するために必要なオブジェクトだけでなく内にあるオブジェクトが用意されています。

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet とレプリケーション オブジェクト 2.5 ライブラリ (JRO)

ADO オブジェクトは、Microsoft Jet データベースの他の多くのデータベースを操作するに設計されて、ため jet 固有の機能に分かれています。

次の表は、各機能を DAO と比較したものです。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>機能</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(Mdb のみ)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>レコード セットを作成します。</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>スタートアップ プロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ANSI92 のサポート * * sql.* パッケージ</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブルを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>新しいデータベースを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>既存のテーブルのプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>テーブル間のリレーションシップを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>セキュリティの設定を編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>列のデータの圧縮の属性をサポートします。</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>格納された基本 SQL クエリまたはビューを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>コードでのみアクセス可能なパーマネント クエリの作成</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>コンテナー/UI およびコードでアクセス可能なクエリの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>データベースの最適化/エンコードします。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>キャッシュを更新します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>データベースをレプリケート可能にします。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベースのレプリカを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>レプリカを同期します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベースのプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>カスタム データベース プロパティを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブルの列のプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。

\*\* Access プロジェクトを操作するときのみ使用できます。

\*\*\*Access データベース エンジンは、いくつかの ANSI 92 SQL をサポートして、その準拠ではありませんまだ完全に ANSI92 です。

リファレンス ・ データベースを使用して**接続**オブジェクトを 1 です。

2 は**カタログ**データベースにオブジェクトを参照します。

3 使用**レプリカ**データベースにオブジェクトを参照します。

4 使用**JetEngine**データベースにオブジェクトを参照します。


> [!NOTE]
> DAO とは異なり ADO および ADOX オブジェクトはこれらのデータベース用のプロバイダーは、そのアクションをサポートしている限り、Jet 以外のデータベースにマークされたアクションを実行できます。


