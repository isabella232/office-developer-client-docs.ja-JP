---
title: View オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97376361a9ea5dcd71e3f9ef918a8ec7f1ebb0c0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920761"
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

