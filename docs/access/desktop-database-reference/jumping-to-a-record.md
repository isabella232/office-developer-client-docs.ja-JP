---
title: 任意のレコードにジャンプする
TOCTitle: Jumping to a Record
ms:assetid: 27177bbe-066c-aeb0-6dfd-45d8c2a87487
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249033(v=office.15)
ms:contentKeyID: 48543829
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88c7c5643559dabf3304863417c526a9fd15354
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873272"
---
# <a name="jumping-to-a-record"></a>任意のレコードにジャンプする


**適用されます**Access 2013、Office 2013。

次の構文で [Move](move-method-ado.md) メソッドを使用すると、 **Recordset** 内を指定した数の分だけ前後に移動できます。

```vb 
 
oRs.Move NumRecords, Start
```

**Move** メソッドは、すべての **Recordset** オブジェクトでサポートされています。

*NumRecords* 引数がゼロより大きい場合、現在のレコードの位置は前方 (**Recordset** の末尾方向) に移動します。*NumRecords* がゼロより小さい場合、現在のレコードの位置は後方 (**Recordset** の先頭方向) に移動します。

**Move** の呼び出しにより、現在のレコードの位置が先頭のレコードよりも前に移動した場合、現在のレコードの位置は、**Recordset** 内の先頭のレコードの前に設定されます (**BOF** が **True** になる)。**BOF** プロパティが既に **True** の場合、後方に移動しようとするとエラーが発生します。

**Move** の呼び出しにより、現在のレコードの位置が最後のレコードよりも後に移動した場合、現在のレコードの位置は、**Recordset** 内の最後のレコードの後に設定されます (**EOF** が **True** になる)。**EOF** プロパティが既に **True** の場合、前方に移動しようとするとエラーが発生します。

空の **Recordset** オブジェクトから **Move** メソッドを呼び出すと、エラーが発生します。

引数*Start*でブックマークを指定した場合、移動は、 **Recordset**オブジェクトがブックマークをサポートするいると仮定して、このブックマークを持つレコードを基準にしてが。 ブックマークは、 [Bookmark](bookmark-property-ado.md) プロパティを使用して取得します。 引数を指定しない場合は、現在のレコードを基準にして移動します。

*NumRecords*引数を現在のレコード位置が現在キャッシュされているレコード グループの範囲外に移動する、プロバイダーからのレコードをローカルにキャッシュ、 **CacheSize**プロパティを使用する場合、レコードの新しいグループを取得するために ADO を強制的に移動先のレコードから開始しています。 **CacheSize** プロパティが、新規に取得されるグループのサイズを決定し、移動先のレコードが最初に取得されるレコードになります。

