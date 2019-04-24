---
title: CacheSize を使用する (Access デスクトップデータベースリファレンス)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312125"
---
# <a name="using-cachesize"></a>CacheSize の使用

**適用先:** Access 2013、Office 2013

**CacheSize** プロパティを使用すると、プロバイダーからローカル メモリに一度に取り込むレコード数を制御できます。たとえば、 **CacheSize** が 10 の場合、 **Recordset** オブジェクトが初めて開かれた後に、最初の 10 のレコードがプロバイダーによってローカル メモリに取り込まれます。 **Recordset** オブジェクト内を移動すると、プロバイダーはローカル メモリのバッファーからデータを返します。キャッシュ内の最後のレコードより後ろのレコードに移動すると、プロバイダーはすぐに次の 10 のレコードをデータ ソースからキャッシュに取り込みます。

> [!NOTE]
> [!メモ] **CacheSize** は、 **Recordset** オブジェクトの **Properties** コレクションに含まれる **Maximum Open Rows** というプロバイダー固有のプロパティを基にしています。 **CacheSize** は、 **Maximum Open Rows** よりも大きい値には設定できません。プロバイダーが開くことのできる行数を変更するには、 **Maximum Open Rows** を設定します。

**CacheSize** の値は、 **Recordset** オブジェクトの存続中に調整できますが、この値を変更しても、データ ソースから次にデータが取り込まれるまで、キャッシュ内のレコード数は変化しません。プロパティ値を変更しただけでは、キャッシュの現在の内容は変更されません。

取り込まれるレコード数が **CacheSize** で指定された数よりも少ない場合は、残りのレコードが返され、エラーは発生しません。

**CacheSize** を 0 に設定することはできません。これを行うとエラーが発生します。

キャッシュから取り込まれたレコードには、他のユーザーがソース データに対して同時に加えた変更が反映されません。キャッシュされたすべてのデータの更新を強制実行するには、[Resync](resync-method-ado.md) メソッドを使用します。

**CacheSize** が 1 よりも大きい値に設定されている場合、レコードの取得後に削除操作が行われると、移動メソッド ([Move](move-method-ado.md)、[MoveFirst、MoveLast、MoveNext、および MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) によって、削除されたレコードに移動してしまう場合があります。最初のフェッチよりも後に実行された削除操作は、削除された行からデータ値にアクセスしようとしない限り、データ キャッシュに反映されません。ただし、**CacheSize** を 1 に設定すると、削除された行はフェッチできないため、この問題は発生しません。

