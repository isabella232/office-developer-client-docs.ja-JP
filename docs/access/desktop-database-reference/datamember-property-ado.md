---
title: DataMember プロパティ (ADO)
TOCTitle: DataMember Property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a67864ab135c59f146a27f997d4b0df63865a50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479595"
---
# <a name="datamember-property-ado"></a>DataMember プロパティ (ADO)

**適用されます**Access 2013 |。Office 2013

[DataSource](datasource-property-ado.md) プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

**String** の値を設定または取得します。名前の大文字と小文字は区別されません。

## <a name="remarks"></a>解説

データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。 *.* の[Recordset](recordset-object-ado.md)オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。

**DataMember** プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。

**DataMember** プロパティは、 **DataSource** プロパティに指定されたどのオブジェクトを **Recordset** オブジェクトとして表すかを指定します。 **Recordset** オブジェクトは、このプロパティを設定する前に閉じておく必要があります。 **DataSource** プロパティの前に **DataMember** プロパティが設定されていない場合、または **DataMember** 名が、 **DataSource** プロパティに指定されているオブジェクトに認識されない場合は、エラーが発生します。

**使用例**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
