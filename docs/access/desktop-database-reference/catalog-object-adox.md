---
title: Catalog オブジェクト (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: cd00165cc42897fc8d536965fdfcd271414d556e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618540"
---
# <a name="catalog-object-adox"></a>Catalog オブジェクト (ADOX)


**適用先**: Access 2013、Office 2013

データ ソースのスキーマ カタログを表すコレクションを含みます ([Tables](tables-collection-adox.md)、[Views](views-collection-adox.md)、[Users](users-collection-adox.md)、[Groups](groups-collection-adox.md)、および [Procedures](procedures-collection-adox.md))。

## <a name="remarks"></a>注釈

**Catalog** オブジェクトは、オブジェクトを追加または削除するか、既存のオブジェクトを変更することによって変更できます。すべての **Catalog** オブジェクトをサポートしていないプロバイダーもあり、スキーマ情報の閲覧のみをサポートするプロバイダーもあります。

**Catalog** オブジェクトのプロパティとメソッドを使用すると、次の操作を実行できます。

- [ActiveConnection](activeconnection-property-adox.md) プロパティを ADO [Connection](connection-object-ado.md) オブジェクトまたは有効な接続文字列に設定して、カタログを開きます。

- [Create](create-method-adox.md) メソッドを使用して、新しいカタログを作成します。

- **GetObjectOwner** メソッドと [SetObjectOwner](getobjectowner-method-adox.md) メソッドを使用して、 [Catalog](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox) 内のオブジェクトの所有者を特定します。

