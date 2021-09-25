---
title: SubmitChanges メソッド (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f1464bce8cbaed5e33c40d90a246c6302e5d85e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562189"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges メソッド (RDS)

**適用先:** Access 2013、Office 2013

ローカルにキャッシュされていて更新可能な [Recordset](recordset-object-ado.md) の保留中の変更を、[Connect](connect-property-rds.md) プロパティまたは [URL](url-property-rds.md) プロパティで指定されているデータ ソースに送信します。

## <a name="syntax"></a>構文

*DataControl*.SubmitChanges

*DataFactory*.SubmitChanges *Connection*, *Recordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。|
|*DataFactory* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数。|
|*Connection* |**RDS.DataControl** オブジェクトの **Connect** プロパティで作成された接続を表す文字列型 ( **String** ) の値。|
|*Recordset* |**Recordset** オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

**RDS.DataControl** オブジェクトで **SubmitChanges** メソッドを使用するには、その前に [Connect](connect-property-rds.md) プロパティ、[Server](server-property-rds.md) プロパティ、および [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) プロパティを設定しておく必要があります。

[SubmitChanges](cancelupdate-method-rds.md) を呼び出した後に同じ **Recordset** オブジェクトに対して **CancelUpdate** メソッドを呼び出しても、既に変更がコミットされているため、その **CancelUpdate** 呼び出しは失敗します。

変更を加えられたレコードだけが変更を反映させるために送信され、すべての変更が成功するか、またはすべてまとめて失敗します。

**SubmitChanges は、既定** の **RDSServer.DataFactory オブジェクトでのみ使用** できます。 カスタム ビジネス オブジェクトには、このメソッドは使用できません。

**URL** プロパティが設定されている場合、 **SubmitChanges** は、その URL で指定された場所に変更内容を送信します。

