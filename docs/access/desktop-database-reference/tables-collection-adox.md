---
title: Tables コレクション (ADOX)
TOCTitle: Tables collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e53cd4b6d4a61a226103eb443bac7f3b4f92d908
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716173"
---
# <a name="tables-collection-adox"></a>Tables コレクション (ADOX)


**適用されます**Access 2013、Office 2013。

カタログのすべての [Table](table-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>解説

[Tables](append-method-adox-tables.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

  - **Append** メソッドを使用して、新しいテーブルをコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

  - [Item](item-property-ado.md) プロパティを使用して、コレクションのテーブルにアクセスします。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるテーブルの数を返します。

  - [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからテーブルを削除します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。

プロバイダーによっては、Tables コレクションで他のスキーマ オブジェクト (View など) を返すことがあります。したがって、複数の ADOX コレクションに同じオブジェクトへの参照が含まれることになります。1 つのコレクションからオブジェクトを削除すると、削除されたオブジェクトを参照する別のコレクションでは、コレクションで Refresh メソッドを呼び出すまで変更内容が反映されません。たとえば、Microsoft Jet の OLE DB Provider では、View は Tables コレクションで返されます。View を削除した場合は、Tables コレクションにその変更を反映するために、コレクションで Refresh を実行する必要があります。

