---
title: Recordset.MoveNext メソッド (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 1b0ebe0edcfcbfac5942fc83a3ff1f99eddfea7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300344"
---
# <a name="recordsetmovenext-method-dao"></a>Recordset.MoveNext メソッド (DAO)


**適用先**: Access 2013、Office 2013

指定された **Recordset** オブジェクトの次のレコードに移動し、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式* .MoveNext

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈


            **Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。


            **Recordset** を開いた時点では、最初のレコードがカレント レコードで、**BOF** プロパティは **False** です。**Recordset** にレコードが含まれていない場合、**BOF** プロパティは **True** で、カレント レコードはありません。

最後のレコードがカレント レコードであるときに **MoveNext** を使用すると、 **EOF** プロパティが **True** となり、カレント レコードがなくなります。 **MoveNext** を再度使用すると、エラーが発生し、 **EOF** プロパティは **True** のままです。

recordset がテーブル タイプの **Recordset** である場合 (Microsoft Access ワークスペースのみ)、現在のインデックスに従って移動が行われます。 現在のインデックスを設定するには、 **Index** プロパティを使用します。 現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。


            **MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。


            **Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

