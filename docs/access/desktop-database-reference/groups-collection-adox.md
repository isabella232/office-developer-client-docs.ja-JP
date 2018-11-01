---
title: Groups コレクション (ADOX)
TOCTitle: Groups Collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 099b9b4034d64f768513cfa5c9a28b89bef89ef8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880993"
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
> <P>[!メモ] <STRONG>Group</STRONG> オブジェクトを <STRONG>User</STRONG> オブジェクトの <STRONG>Groups</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">Group</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Groups</STRONG> コレクションに存在している必要があります。</P>


