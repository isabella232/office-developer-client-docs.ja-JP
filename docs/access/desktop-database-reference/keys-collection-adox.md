---
title: Keys コレクション (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 82718af6378b13c4b0350dca84a84f06afd682de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626345"
---
# <a name="keys-collection-adox"></a>Keys コレクション (ADOX)


**適用先**: Access 2013、Office 2013

テーブルのすべての [Key](key-object-adox.md) オブジェクトを含みます。

## <a name="remarks"></a>注釈

[Keys](append-method-adox-keys.md) コレクションの **Append** メソッドは、ADOX に対して一意です。次のことができます。

  - **Append** メソッドを使用して、新しいキーをコレクションに追加します。

残りのプロパティとメソッドは、ADO コレクションに標準で装備されています。次のことができます。

  - [Item](item-property-ado.md) プロパティを使用して、コレクションのキーにアクセスします。

  - [Count](count-property-ado.md) プロパティを使用して、コレクションに含まれるキーの数を返します。

  - [Delete](delete-method-adox-collections.md) メソッドを使用して、コレクションからキーを削除します。

  - [Refresh](refresh-method-ado.md) メソッドを使用して、コレクションのオブジェクトを更新し、カレント データベースのスキーマを反映します。

