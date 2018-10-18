---
<<<<<<< ヘッド タイトル: を使用して ActiveX データ オブジェクトの TOCTitle: ActiveX データ オブジェクトを使用する ms:assetid: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: 48545279 ms.date: 2015/09/18 === タイトル: ActiveX を使用データ オブジェクト TOCTitle: ActiveX データ オブジェクトの使用の説明: Microsoft Access が保守、および Visual Basic を使用して Access データベースとその関連データを管理する 3 つのオブジェクトの作成に使用するモデルを提供します。
ms:assetid: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: 48545279 ms.date: 2018/10/16
>>>>>>> マスター mtps_version: v=office.15 f1_keywords:
- vbaac10.chm5285627 f1_categories。
- Office.Version=v15
---

<<<<<<< ヘッド
# <a name="using-activex-data-objects"></a>ActiveX データ オブジェクトを使用する


**適用されます**Access 2013 |。Office 2013

<a name="microsoft-access-provides-three-object-models-to-use-in-the-creation-maintaining-and-managing-of-your-access-databases-and-their-related-data-by-using-visual-basic"></a>Microsoft Access では、Visual Basic を使って Access データベースとその関連データを作成、保守、および管理するための 3 つの新しいオブジェクト モデルが提供されています。
=======
# <a name="use-activex-data-objects"></a>ActiveX データ オブジェクトを使用します。

**適用されます**Access 2013 |。Office 2013

Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。
>>>>>>> master

## <a name="microsoft-activex-data-objects-ado"></a>ADO (ActiveX データ オブジェクト)

ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。

<<<<<<< ヘッド
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>ADOX (ADO Ext. for DDL and Security)

ADOX では、セキュリティ管理に必要なオブジェクトのほか、新しいデータベースに必要な DDL (データ定義言語) オブジェクト、およびそれに含まれるオブジェクトが提供されています。

**JRO (Jet and Replication Objects 2.5 Library)**

<a name="since-ado-objects-were-designed-to-work-with-many-databases-in-addition-to-microsoft-jet-databases-functionality-specific-to-jet-was-broken-out-into-the-jro-library"></a>ADO オブジェクトは、Jet データベースだけでなく、数多くのデータベースと共に動作するよう設計されています。JRO ライブラリには Jet 特有の機能を集めています。
=======
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>DDL とセキュリティ (ADOX) の ADO の拡張

ADOX には、新しいデータベースを作成するために必要なデータ定義言語 (DDL) オブジェクト、およびセキュリティを管理するために必要なオブジェクトだけでなく内にあるオブジェクトが用意されています。

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet とレプリケーション オブジェクト 2.5 ライブラリ (JRO)

ADO オブジェクトは、Microsoft Jet データベースの他の多くのデータベースを操作するに設計されて、ため jet 固有の機能に分かれています。
>>>>>>> master

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
<<<<<<< ヘッド (MDB ののみ)</p></th>
=== (Mdb のみ)</p></th>
>>>>>>> master
</tr>
</thead>
<tbody>
<tr class="odd">
<<<<<<< ヘッド
<td><p>レコードセットの作成</p></td>
=======
<td><p>レコード セットを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>起動時の設定関連のプロパティの編集</p></td>
=======
<td><p>スタートアップ プロパティを編集します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>ANSI92 SQL のサポート ***</p></td>
=======
<td><p>ANSI92 のサポート * * sql.* パッケージ</p></td>
>>>>>>>マスター
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>テーブルの作成</p></td>
=======
<td><p>テーブルを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>新しいデータベース</p></td>
=======
<td><p>新しいデータベースを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>既存のテーブルのプロパティの編集</p></td>
=======
<td><p>既存のテーブルのプロパティを編集します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>テーブルのリレーションシップの作成</p></td>
=======
<td><p>テーブル間のリレーションシップを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>セキュリティ設定値の編集</p></td>
=======
<td><p>セキュリティの設定を編集します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>列データの圧縮属性のサポート</p></td>
=======
<td><p>列のデータの圧縮の属性をサポートします。</p></td>
>>>>>>>マスター
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>格納された基本 SQL クエリまたはビューの編集</p></td>
=======
<td><p>格納された基本 SQL クエリまたはビューを編集します。</p></td>
>>>>>>>マスター
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
<<<<<<< ヘッド
<td><p>データベースの最適化/エンコード</p></td>
=======
<td><p>データベースの最適化/エンコードします。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>キャッシュの更新</p></td>
=======
<td><p>キャッシュを更新します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>データベースをレプリケート可能にする</p></td>
=======
<td><p>データベースをレプリケート可能にします。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>データベース レプリカの作成</p></td>
=======
<td><p>データベースのレプリカを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>レプリカの同期をとる</p></td>
=======
<td><p>レプリカを同期します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>データベース プロパティの編集</p></td>
=======
<td><p>データベースのプロパティを編集します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< ヘッド
<td><p>カスタム データベース プロパティの作成</p></td>
=======
<td><p>カスタム データベース プロパティを作成します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< ヘッド
<td><p>列のプロパティの編集</p></td>
=======
<td><p>テーブルの列のプロパティを編集します。</p></td>
>>>>>>>マスター
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。

\*\* Access プロジェクトを操作するときのみ使用できます。

<<<<<<< ヘッド\* \* \* Access データベース エンジンは、いくつかの ANSI 92 SQL をサポートしていてはまだ完全に ANSI92 に準拠します。

1データベースの参照には、 **Connection** オブジェクトを使用します。

2データベースの参照には、 **Catalog** オブジェクトを使用します。

3データベースの参照には、 **Replica** オブジェクトを使用します。

4データベースの参照には、 **JetEngine** オブジェクトを使用します。


> [!NOTE]
> <a name="punlike-dao-ado-and-adox-objects-can-perform-the-marked-actions-in-databases-other-then-jet-as-long-as-the-provider-for-those-databases-supports-that-actionp"></a><P>DAO とは異なり、ADO および ADOX オブジェクトは、上記の印がついている動作を Jet ではなく、データベースで実行できます。ただし、使用するデータベースのプロバイダーが、それらの動作をサポートしている場合に限ります。</P>
=======
\*\*\*Access データベース エンジンは、いくつかの ANSI 92 SQL をサポートして、その準拠ではありませんまだ完全に ANSI92 です。

リファレンス ・ データベースを使用して**接続**オブジェクトを 1 です。

2 は**カタログ**データベースにオブジェクトを参照します。

3 使用**レプリカ**データベースにオブジェクトを参照します。

4 使用**JetEngine**データベースにオブジェクトを参照します。


> [!NOTE]
> DAO とは異なり ADO および ADOX オブジェクトはこれらのデータベース用のプロバイダーは、そのアクションをサポートしている限り、Jet 以外のデータベースにマークされたアクションを実行できます。
>>>>>>> master


