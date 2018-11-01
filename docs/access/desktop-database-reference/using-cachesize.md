---
title: CacheSize (デスクトップ データベース参照のアクセス) を使用します。
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa624c545d17ef0d56a076b3d30326bacd2c6edf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871963"
---
# <a name="using-cachesize"></a>CacheSize の使用


**適用されます**Access 2013、Office 2013。

**CacheSize** プロパティを使用すると、プロバイダーからローカル メモリに一度に取り込むレコード数を制御できます。たとえば、 **CacheSize** が 10 の場合、 **Recordset** オブジェクトが初めて開かれた後に、最初の 10 のレコードがプロバイダーによってローカル メモリに取り込まれます。 **Recordset** オブジェクト内を移動すると、プロバイダーはローカル メモリのバッファーからデータを返します。キャッシュ内の最後のレコードより後ろのレコードに移動すると、プロバイダーはすぐに次の 10 のレコードをデータ ソースからキャッシュに取り込みます。


> [!NOTE]
> <P>[!メモ] <STRONG>CacheSize</STRONG> は、 <STRONG>Recordset</STRONG> オブジェクトの <STRONG>Properties</STRONG> コレクションに含まれる <STRONG>Maximum Open Rows</STRONG> というプロバイダー固有のプロパティを基にしています。 <STRONG>CacheSize</STRONG> は、 <STRONG>Maximum Open Rows</STRONG> よりも大きい値には設定できません。プロバイダーが開くことのできる行数を変更するには、 <STRONG>Maximum Open Rows</STRONG> を設定します。</P>



**CacheSize** の値は、 **Recordset** オブジェクトの存続中に調整できますが、この値を変更しても、データ ソースから次にデータが取り込まれるまで、キャッシュ内のレコード数は変化しません。プロパティ値を変更しただけでは、キャッシュの現在の内容は変更されません。

取り込まれるレコード数が **CacheSize** で指定された数よりも少ない場合は、残りのレコードが返され、エラーは発生しません。

**CacheSize** を 0 に設定することはできません。これを行うとエラーが発生します。

キャッシュから取り込まれたレコードには、他のユーザーがソース データに対して同時に加えた変更が反映されません。キャッシュされたすべてのデータの更新を強制実行するには、[Resync](resync-method-ado.md) メソッドを使用します。

**CacheSize** が 1 よりも大きい値に設定されている場合、レコードの取得後に削除操作が行われると、移動メソッド ([Move](move-method-ado.md)、[MoveFirst、MoveLast、MoveNext、および MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) によって、削除されたレコードに移動してしまう場合があります。最初のフェッチよりも後に実行された削除操作は、削除された行からデータ値にアクセスしようとしない限り、データ キャッシュに反映されません。ただし、**CacheSize** を 1 に設定すると、削除された行はフェッチできないため、この問題は発生しません。

