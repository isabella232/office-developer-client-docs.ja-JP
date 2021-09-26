---
title: Recordset.MoveFirst メソッド (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b09723b816525ac538de54c3a85df53260496959
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585453"
---
# <a name="recordsetmovefirst-method-dao"></a>Recordset.MoveFirst メソッド (DAO)


**適用先**: Access 2013、Office 2013

指定した **Recordset** オブジェクトの最初のレコードに移動して、そのレコードをカレント レコードにします。

## <a name="syntax"></a>構文

*式* .MoveFirst

*式* **Recordset** オブジェクトを表す変数。

## <a name="remarks"></a>注釈


            **Move** メソッドは、条件を適用せずにレコード間を移動するために使用します。

カレント レコードを編集した場合は、他のレコードに移動する前に、必ず **Update** メソッドを使用して変更を保存してください。更新を実行せずに他のレコードに移動すると、変更は警告なしで取り消されます。


            **Recordset** を開いた時点では、最初のレコードがカレント レコードで、**BOF** プロパティは **False** です。**Recordset** にレコードが含まれていない場合、**BOF** プロパティは **True** で、カレント レコードはありません。


            **MoveFirst** または **MoveLast** を使用したときに、最初のレコードまたは最後のレコードが既にカレント レコードである場合、カレント レコードは変更されません。

recordset がテーブル タイプの **Recordset** である場合 (Microsoft Access ワークスペースのみ)、現在のインデックスに従って移動が行われます。現在のインデックスを設定するには、 **Index** プロパティを使用します。現在のインデックスを設定しない場合、返されるレコードの順序は未定義となります。


            **MoveFirst**、**MoveLast**、および **MovePrevious** の各メソッドは、前方スクロール タイプの **Recordset** オブジェクトでは使用できません。


            **Recordset** オブジェクト内のカレント レコードを、指定されたレコード数だけ前方または後方に移動するには、**Move** メソッドを使用します。

