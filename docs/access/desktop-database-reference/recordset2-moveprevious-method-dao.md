---
title: MovePrevious メソッド (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307246"
---
# <a name="recordset2moveprevious-method-dao"></a>MovePrevious メソッド (DAO)


**適用先:** Access 2013、Office 2013

指定された **Recordset** オブジェクトの前のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*。MovePrevious

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合は、 **BOF** プロパティは **True** で、カレント レコードはありません。

最初のレコードがカレント レコードであるときに **MovePrevious** を使用すると、 **BOF** プロパティが **True** となり、カレント レコードがなくなります。 **MovePrevious** を再度使用すると、エラーが発生し、 **BOF** は **True** のままです。

recordset がテーブルタイプの**recordset**を参照している場合 (Microsoft Access ワークスペースのみ)、移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

**MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

