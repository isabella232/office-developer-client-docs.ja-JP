---
title: Recordset.MovePrevious メソッド (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 22832abd8a573c4e7dc45b5f7827019e5e577964
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477399"
---
# <a name="recordsetmoveprevious-method-dao"></a>Recordset.MovePrevious メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

指定された **Recordset** オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*です。MovePrevious

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合、 **BOF** プロパティは **True** で、カレント レコードはありません。

最初のレコードがカレント レコードであるときに **MovePrevious** を使用すると、 **BOF** プロパティは **True** となり、カレント レコードはなくなります。 **MovePrevious** を再度使用すると、エラーが発生し、 **BOF** は **True** のままとなります。

レコード セットは、テーブル タイプ**のレコード セット**(Microsoft Access ワークスペースのみ) を参照している場合の移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

前方のみタイプの**Recordset**オブジェクトでは、 **MoveFirst**、 **MoveLast**、および**MovePrevious**メソッドを使うことはできません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、 **Move** メソッドを使用します。

