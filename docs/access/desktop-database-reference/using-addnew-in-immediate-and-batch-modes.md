---
title: イミディエイト モードとバッチ モードで AddNew を使用する
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79bd4ed656da49e61ea70ace3b11f09c19382b03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943641"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>イミディ エイトとバッチ モードで AddNew を使用します。


**適用されます**Access 2013、Office 2013。

**AddNew**メソッドの動作は、**レコード セット**オブジェクトと、 *FieldList*と*値*の引数を渡すかどうかの更新モードに依存します。

**Update** メソッドを呼び出すとプロバイダーによって基になるデータ ソースに変更が書き込まれるイミディエイト更新モードでは、引数を指定せずに **AddNew** メソッドを呼び出すと、**EditMode** プロパティが **adEditAdd** に設定されます。プロバイダーは、フィールドの値に変更があった場合、それをローカルにキャッシュします。**Update** メソッドを呼び出すと、新しいレコードがデータベースに保存され、**EditMode** プロパティが **adEditNone** にリセットされます。*FieldList* 引数と *Values* 引数を指定した場合は、直ちに新しいレコードが自動的にデータベースに保存されます (**Update** を呼び出す必要はありません)。この場合、**EditMode** プロパティの値は **adEditNone** のまま変化しません。

バッチ更新モードでは、引数を指定しないで**AddNew**メソッドを呼び出すと、 **EditMode**プロパティ**adEditAdd**に設定します。 プロバイダーは、ローカルでのフィールド値の変更をキャッシュします。 **UpdateBatch が呼び出されるまで、プロバイダーは基になるデータベースへの変更 post しないですが、現在の**レコード セット**に新しいレコードを追加します。 **Update**メソッドを呼び出すと、 **EditMode**プロパティが**adEditNone**にリセット**メソッドです。 ADO がプロバイダーをキャッシュに格納するために新しいレコードを送信する、 *FieldList*と*値*の引数を渡す場合**UpdateBatch**メソッドを呼び出して基になるデータベースに新しいレコードを転記する必要があります。 **および**UpdateBatch**** の詳細についてを参照してください[第 5 章: データを更新し保存する](chapter-5-updating-and-persisting-data.md)です。

