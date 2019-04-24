---
title: Database. Synchronize メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294709"
---
# <a name="databasesynchronize-method-dao"></a>Database. Synchronize メソッド (DAO)


**適用先:** Access 2013、Office 2013

2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*。Synchronize (***dbpathname***, ***ExchangeType***)

*式***Database**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
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
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>2つのデータベース間で変更を同期する方向を示す<strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong>定数です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

You use **Synchronize** to exchange data and design changes between two databases. Design changes always happen first. Both databases must be at the same design level before they can exchange data. たとえば、データ変更がデータベースから dbpathname にのみフローしているにもかかわらず、 **dbRepExportChanges**型を使用すると、レプリカのデザインが変更される可能性があります。

dbpathname で識別されるレプリカは、同じレプリカセットの一部である必要があります。 2 つのレプリカの **ReplicaID** プロパティが同じ値に設定されている場合や、2 つのレプリカが異なるレプリカ セットのデザイン マスターである場合、同期化は失敗します。

2 つのレプリカをインターネット経由で同期させる場合は、定数 **dbRepSyncInternet** を使用する必要があります。 この場合は、ローカルエリアネットワークパスを指定する代わりに、dbpathname 引数に Uniform resource Locator (URL) アドレスを指定します。


> [!NOTE]
> [!メモ] 部分レプリカを他の部分レプリカに同期させることはできません。 詳細については、 [PopulatePartial](database-populatepartial-method-dao.md) メソッドのトピックを参照してください。


