---
title: サポートされている内容を確認する
TOCTitle: Determining What is Supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6114dd0fa56a87b6c2e07770795ea5889ae3c44
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883632"
---
# <a name="determining-what-is-supported"></a>サポートされている内容を確認する


**適用されます**Access 2013、Office 2013。

**Supports** メソッドは、指定された **Recordset** オブジェクトが、特定の種類の機能をサポートしているかどうかを確認するために使用します。構文は次のとおりです。

`boolean = recordset.Supports( CursorOptions )`

**Supports** は、*CursorOptions* 引数で指定されているすべての機能が、プロバイダーによってサポートされているかどうかを示すブール値を返します。**Supports** メソッドを使用すると、**Recordset** オブジェクトがどのような種類の機能をサポートしているのかを確認できます。*CursorOptions* で対応する定数が指定されている機能を、**Recordset** オブジェクトがサポートしている場合、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。

**Supports** メソッドを使用すると、 **Recordset** オブジェクトが、新しいレコードの追加、ブックマークの使用、 **Find** メソッドの使用、スクロールの使用、 **Index** プロパティの使用、およびバッチ更新の実行に対応できるかどうかを確認できます。定数とその意味をすべて記載した一覧については、「 [CursorOptionEnum](cursoroptionenum.md)」を参照してください。

**Supports** メソッドが特定の機能について **True** を返す場合でも、プロバイダーがすべての状況でその機能を実現できるとは限りません。 **Supports** メソッドは、特定の条件が満たされているという仮定の下で、プロバイダーが指定された機能をサポートできるかどうかを返すに過ぎません。たとえば、カーソルで複数テーブルの結合が想定されている場合は一部の列を更新できませんが、 **Supports** メソッドでは **Recordset** オブジェクトが更新をサポートしていると示される場合があります。

