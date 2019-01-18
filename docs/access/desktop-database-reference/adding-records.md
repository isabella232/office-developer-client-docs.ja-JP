---
title: (デスクトップ データベース参照のアクセス) のレコードを追加します。
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698842"
---
# <a name="adding-records"></a>レコードの追加

**適用されます**Access 2013、Office 2013。

既存の **Recordset** 内に新しいレコードを作成し、これを初期化するには、 **AddNew** メソッドを使用します。 **Supports** メソッドで **CursorOptionEnum** 値の **adAddNew** を指定すると、現在の **Recordset** オブジェクトにレコードを追加できるかどうかを確認できます。

**AddNew** メソッドを呼び出した後は、新しいレコードが現在のレコードとなり、 **Update** メソッドを呼び出した後もそのままの状態です。 **Recordset** オブジェクトがブックマークをサポートしていない場合は、他のレコードに移動すると新しいレコードにアクセスできなくなる可能性があります。このため、カーソルの種類によっては、新しいレコードにアクセスできるようにするために、 **Requery** メソッドを呼び出す必要があります。

現在のレコードの編集中、または新しいレコードの追加中に **AddNew** を呼び出すと、 **Update** メソッドが自動的に呼び出され、変更を保存してから新しいレコードが作成されます。

このセクションには、次のトピックが含まれています。

- [複数のフィールドの追加](adding-multiple-fields.md)
- [編集モードを決定します。](determining-edit-mode.md)
- [イミディ エイトとバッチ モードで AddNew を使用します。](using-addnew-in-immediate-and-batch-modes.md)

