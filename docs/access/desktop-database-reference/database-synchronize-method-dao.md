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
ms.localizationpriority: medium
ms.openlocfilehash: 8c12d87cd9d5730c8e64add44254bc429256e741
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589765"
---
# <a name="databasesynchronize-method-dao"></a>Database.Synchronize メソッド (DAO)


**適用先**: Access 2013、Office 2013

2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .Synchronize(***DbPathName** _, _*_ExchangeType_**)

*式* **Database** オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>データベースを同期させる対象のレプリカへのパスです。</p></td>
</tr>
<tr class="even">
<td><p><em>ExchangeType</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>2 つのデータベース間の変更を同期する方向を示す <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> 定数。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

You use **Synchronize** to exchange data and design changes between two databases. Design changes always happen first. Both databases must be at the same design level before they can exchange data. たとえば **、dbRepExportChanges** 型の交換によって、データベースから DbPathName へのデータ変更フローのみである場合でも、レプリカで設計変更が発生する可能性があります。

DbPathName で識別されるレプリカは、同じレプリカ セットの一部である必要があります。 2 つのレプリカの **ReplicaID** プロパティが同じ値に設定されている場合や、2 つのレプリカが異なるレプリカ セットのデザイン マスターである場合、同期化は失敗します。

2 つのレプリカをインターネット経由で同期させる場合は、定数 **dbRepSyncInternet** を使用する必要があります。 この場合、ローカル エリア ネットワーク パスを指定する代わりに、DbPathName 引数に Uniform Resource Locator (URL) アドレスを指定します。


> [!NOTE]
> [!メモ] 部分レプリカを他の部分レプリカに同期させることはできません。詳細については、 [PopulatePartial](database-populatepartial-method-dao.md) メソッドのトピックを参照してください。


