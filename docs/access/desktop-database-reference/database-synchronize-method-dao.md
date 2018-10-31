---
title: Database.Synchronize メソッド (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b25536c158c248695c9e537a0153922b2518058a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863291"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。(***DbPathName***、 ***ExchangeType***) を同期します。

*式***データベース**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DbPathName</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>データベースを同期させる対象のレプリカへのパスです。</p></td>
</tr>
<tr class="even">
<td><p>ExchangeType</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>2 つのデータベース間で変更を同期させる方向を示す <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> クラスの定数です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

2 つのデータベース間でデータおよびデザインの変更内容を交換するのにには、**同期**を使用します。 デザインの変更は、常に最初に発生します。 両方のデータベースする必要があります同じデザイン レベルで交換するにはデータです。 などの種類が**dbRepExportChanges**の交換可能性があります、レプリカでデザインの変更データのみ、データベースから DbPathName にフローを変更する場合でも。

DbPathName で識別されるレプリカは、同じレプリカ セットの一部である必要があります。 2 つのレプリカの **ReplicaID** プロパティが同じ値に設定されている場合や、2 つのレプリカが異なるレプリカ セットのデザイン マスターである場合、同期化は失敗します。

2 つのレプリカをインターネット経由で同期させる場合は、定数 **dbRepSyncInternet** を使用する必要があります。 この例では、ローカル エリア ネットワーク パスを指定するのではなく引数 DbPathName の統一リソース ロケーター (URL) アドレスを指定します。


> [!NOTE]
> [!メモ] 部分レプリカを他の部分レプリカに同期させることはできません。詳細については、 [PopulatePartial](database-populatepartial-method-dao.md) メソッドのトピックを参照してください。


