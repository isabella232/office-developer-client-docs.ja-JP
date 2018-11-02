---
title: TableDef.RecordCount プロパティ (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920922"
---
# <a name="tabledefrecordcount-property-dao"></a>TableDef.RecordCount プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**[TableDef](tabledef-object-dao.md)** オブジェクトの全レコード数を取得します。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。RecordCount

*式***テーブル定義**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

レコードを持たない **Recordset** オブジェクトまたは **TableDef** オブジェクトでは、 **RecordCount** プロパティの設定値が 0 となります。

リンクされた **TableDef** オブジェクトを使用する場合、**RecordCount** プロパティの設定値は常に -1 となります。

