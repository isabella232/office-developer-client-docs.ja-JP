---
title: Catalog オブジェクト (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8bb6024043655c2529ce8309e5a6bead08cb4225
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947057"
---
# <a name="catalog-object-adox"></a>Catalog オブジェクト (ADOX)


**適用されます**Access 2013、Office 2013。

データ ソースのスキーマ カタログを表すコレクションを含みます ([Tables](tables-collection-adox.md)、[Views](views-collection-adox.md)、[Users](users-collection-adox.md)、[Groups](groups-collection-adox.md)、および [Procedures](procedures-collection-adox.md))。

## <a name="remarks"></a>解説

**Catalog** オブジェクトは、オブジェクトを追加または削除するか、既存のオブジェクトを変更することによって変更できます。すべての **Catalog** オブジェクトをサポートしていないプロバイダーもあり、スキーマ情報の閲覧のみをサポートするプロバイダーもあります。

**Catalog** オブジェクトのプロパティとメソッドを使用すると、次の操作を実行できます。

- [ActiveConnection](activeconnection-property-adox.md) プロパティを ADO [Connection](connection-object-ado.md) オブジェクトまたは有効な接続文字列に設定して、カタログを開きます。

- [Create](create-method-adox.md) メソッドを使用して、新しいカタログを作成します。

- **GetObjectOwner** メソッドと [SetObjectOwner](getobjectowner-method-adox.md) メソッドを使用して、 [Catalog](https://msdn.microsoft.com/library/jj249006\(v=office.15\)) 内のオブジェクトの所有者を特定します。

