---
title: イミディエイト モードとバッチ モードで AddNew を使用する
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: caa9a0137e4fbfb636fd2d876fb9f72eed9c6509
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585089"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>イミディエイト モードとバッチ モードでの AddNew の使用


**適用先:** Access 2013、Office 2013

**AddNew** メソッドの動作は、**Recordset** の更新モードと、*FieldList* 引数および *Values* 引数を渡すかどうかによって異なります。

**Update** メソッドを呼び出すとプロバイダーによって基になるデータ ソースに変更が書き込まれるイミディエイト更新モードでは、引数を指定せずに **AddNew** メソッドを呼び出すと、**EditMode** プロパティが **adEditAdd** に設定されます。プロバイダーは、フィールドの値に変更があった場合、それをローカルにキャッシュします。**Update** メソッドを呼び出すと、新しいレコードがデータベースに保存され、**EditMode** プロパティが **adEditNone** にリセットされます。*FieldList* 引数と *Values* 引数を指定した場合は、直ちに新しいレコードが自動的にデータベースに保存されます (**Update** を呼び出す必要はありません)。この場合、**EditMode** プロパティの値は **adEditNone** のまま変化しません。

バッチ更新モードでは、引数を指定せずに **AddNew** メソッドを呼び出すと、**EditMode** プロパティが **adEditAdd** に設定されます。プロバイダーは、フィールドの値に変更があった場合、それをローカルにキャッシュします。**Update** メソッドを呼び出すと、新しいレコードが現在の **Recordset** に追加され、**EditMode** プロパティが **adEditNone** にリセットされます。ただし、**UpdateBatch** メソッドを呼び出さない限り、プロバイダーは基になるデータベースに変更を保存しません。*FieldList* 引数と *Values* 引数を指定した場合は、新しいレコードが自動的にプロバイダーに送られ、キャッシュに保存されます。この場合、新しいレコードを基になるデータベースに保存するには、**UpdateBatch** メソッドを呼び出す必要があります。**Update** および **UpdateBatch** の詳細については、「[5 章: データを更新し、保存する](chapter-5-updating-and-persisting-data.md)」を参照してください。

