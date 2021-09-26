---
title: レコードへのジャンプ
TOCTitle: Jumping to a record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bc76b4d9efffbebe99a71bb1948b2cc7e12b73f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617987"
---
# <a name="jumping-to-a-record"></a>レコードへのジャンプ


**適用先**: Access 2013、Office 2013

次の構文で [Move](move-method-ado.md) メソッドを使用すると、 **Recordset** 内を指定した数の分だけ前後に移動できます。

```vb 
 
oRs.Move NumRecords, Start
```

**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。

*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。

**Move** の呼び出しにより、現在のレコードの位置が先頭のレコードよりも前に移動した場合、現在のレコードの位置は、**Recordset** 内の先頭のレコードの前に設定されます (**BOF** が **True** になる)。**BOF** プロパティが既に **True** の場合、後方に移動しようとするとエラーが発生します。

**Move** の呼び出しにより、現在のレコードの位置が最後のレコードよりも後に移動した場合、現在のレコードの位置は、**Recordset** 内の最後のレコードの後に設定されます (**EOF** が **True** になる)。**EOF** プロパティが既に **True** の場合、前方に移動しようとするとエラーが発生します。

空の **Recordset** オブジェクトで **Move** メソッドを呼び出すと、エラーが発生します。

**Recordset** オブジェクトでブックマークがサポートされている場合、*Start* 引数でブックマークを指定すると、このブックマークが指すレコードを基準にして移動します。ブックマークは、[Bookmark](bookmark-property-ado.md) プロパティを使用して取得します。引数を指定しない場合は、現在のレコードを基準にして移動します。

**CacheSize** プロパティを使用してプロバイダーからのレコードをローカルにキャッシュしている場合、*NumRecords* 引数を渡して、現在キャッシュされているレコード グループの範囲外に現在のレコード位置を移動すると、移動先のレコードから始まる新規レコード グループが強制的に取得されます。**CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。

