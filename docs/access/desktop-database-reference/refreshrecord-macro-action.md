---
title: RefreshRecord マクロ アクション
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 1f1592282635cc27486562ca26c31bcea4f3b4e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611694"
---
# <a name="refreshrecord-macro-action"></a>RefreshRecord マクロ アクション


**適用先**: Access 2013、Office 2013

You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.

## <a name="remarks"></a>注釈

the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.

このマクロ アクションの動作は、このマクロ アクションをクライアント データベースで呼び出しているか、または Web データベースで呼び出しているかによって異なります。

## <a name="client-database"></a>クライアント データベースの場合

In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.

The **RefreshRecord** macro action does the following in a client database:

1.  アクティブ フォームまたはアクティブ データシートのレコード ソースを更新し、現在のレコード セットの行に対する変更を反映します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。

2.  現在のレコード セットを更新し、変更を反映します。 レコード ソース内の行が削除されている場合は、[削除済み] を表示するために \# 変更されます。

3.  アクティブまたはデータシートを更新して、変更されたレコードと削除済みレコードを現在のセット \# に表示します。

4.  アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。

## <a name="web-database"></a>Web データベースの場合

In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.

The **RefreshRecord** macro action does the following in a web database:

1.  現在のレコード セットのベース テーブルに対する変更を、サーバーから取得します。ODBC リンク テーブルについては、現在のレコード セットに対する変更をデータ ソースから取得します。

2.  現在のレコード セットを更新し、変更を反映します。 現在のセット内の行が削除されている場合は、[削除済み] を表示するために \# 変更されます。

3.  アクティブなフォームまたはデータシートを更新して、変更されたレコードと削除済みレコードを現在のセット \# に表示します。

4.  アクティブ フォームまたはアクティブ データシートのサブフォームおよびサブレポートに再クエリを行います。

