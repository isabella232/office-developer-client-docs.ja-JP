---
title: Groups コレクション (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7bd2519af3ea3c35d8cc32ef1ec31ea4f9efa1e
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936673"
---
# <a name="groups-collection-adox"></a>Groups コレクション (ADOX)

**適用されます**Access 2013、Office 2013。

カタログまたはユーザーのすべての格納された [Group](group-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>解説

**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

[Groups](append-method-adox-groups.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

- **Append** メソッドを使用して、新しいセキュリティ グループをコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

- [Item](item-property-ado.md) プロパティを使用して、コレクションのグループにアクセスします。

- [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるグループの数を返します。

- [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからグループを削除します。

- [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。

> [!NOTE]
> [!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。


