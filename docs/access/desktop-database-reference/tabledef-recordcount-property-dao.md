---
title: TableDef プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314288"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef プロパティ (DAO)


**適用先:** Access 2013、Office 2013

**[TableDef](tabledef-object-dao.md)** オブジェクトのレコードの合計数を返します。 取得のみ可能な **Long** 値です。

## <a name="syntax"></a>構文

*式*。RecordCount

*式***TableDef**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

レコードを持たない **Recordset** オブジェクトまたは **TableDef** オブジェクトでは、 **RecordCount** プロパティの設定値が 0 となります。

リンクされた **TableDef** オブジェクトを使用する場合、**RecordCount** プロパティの設定値は常に -1 となります。

