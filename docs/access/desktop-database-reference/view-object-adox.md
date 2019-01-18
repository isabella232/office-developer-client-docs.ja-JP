---
title: View オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722474"
---
# <a name="view-object-adox"></a>View オブジェクト (ADOX)


**適用されます**Access 2013、Office 2013。

抽出されたレコードのセットまたは仮想テーブルを表します。ADO [Command](command-object-ado.md) オブジェクトと共に使用する場合、 **View** オブジェクトを使用してビューを追加、削除、または変更できます。

## <a name="remarks"></a>解説

ビューは、他のデータベースまたはビューから作成された仮想テーブルです。 **View** オブジェクトを使用すると、プロバイダーの "CREATE VIEW" の構文を使用せずにストアド プロシージャを作成できます。

**View** オブジェクトのプロパティを使用すると、次の操作を実行できます。

  - [Name](name-property-adox.md) プロパティを使用して、ビューを識別します。

  - **Command** プロパティを使用して、ビューの追加、削除、または変更に使用できる ADO [Command](command-property-adox.md) オブジェクトを指定します。

  - [DateCreated](datecreated-property-adox.md) プロパティと [DateModified](datemodified-property-adox.md) プロパティを使用して、日付情報を返します。

