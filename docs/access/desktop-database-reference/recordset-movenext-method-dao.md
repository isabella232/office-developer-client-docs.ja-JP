---
title: Recordset.MoveNext メソッド (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef9d90e16ea4c98add8557cdeae22cb85caeeb64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884318"
---
# <a name="recordsetmovenext-method-dao"></a>Recordset.MoveNext メソッド (DAO)


**適用されます**Access 2013、Office 2013。

指定された **Recordset** オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*です。MoveNext

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。

最後のレコードがカレント レコードであるときに **MoveNext** を使用すると、 **EOF** プロパティは **True** となり、カレント レコードはなくなります。 **MoveNext** を再度使用すると、エラーが発生し、 **EOF** は **True** のままとなります。

レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。

