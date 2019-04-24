---
title: Recordset2 メソッド (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0eeb917e-f76a-03ec-9e1e-aa8d501db031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845265(v=office.15)
ms:contentKeyID: 48543254
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6f500578182aac74b608117ee4105a6b657057df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309556"
---
# <a name="recordset2movenext-method-dao"></a>Recordset2 メソッド (DAO)


**適用先:** Access 2013、Office 2013

指定された **Recordset** オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式*。MoveNext

*式***Recordset2**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

**Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。

**Recordset** を開いた時点では、最初のレコードがカレント レコードで、 **BOF** プロパティは **False** です。 **Recordset** にレコードが含まれていない場合は、 **BOF** プロパティは **True** で、カレント レコードはありません。

最後のレコードがカレント レコードであるときに **MoveNext** を使用すると、 **EOF** プロパティが **True** となり、カレント レコードがなくなります。 **MoveNext** を再度使用すると、エラーが発生し、 **EOF** プロパティは **True** のままです。

recordset がテーブルタイプの**recordset**を参照している場合 (Microsoft Access ワークスペースのみ)、移動は現在のインデックスに従います。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。

**MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。

**Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

