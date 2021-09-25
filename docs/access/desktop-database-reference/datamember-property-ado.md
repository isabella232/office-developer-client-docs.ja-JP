---
title: DataMember プロパティ (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: acdfe44352b85644c0c27e624b1dbb07afb235b8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565535"
---
# <a name="datamember-property-ado"></a>DataMember プロパティ (ADO)

**適用先:** Access 2013、Office 2013

[DataSource](datasource-property-ado.md) プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

**String** の値を設定または取得します。名前の大文字と小文字は区別されません。

## <a name="remarks"></a>注釈

This property is used to create data-bound controls with the Data Environment. Data Environment は、Recordset オブジェクトとして表される名前付きオブジェクト *(データ* メンバー) を含むデータ (データ ソース) のコレクション [を保持](recordset-object-ado.md) します *。*

**DataMember** プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。

**DataMember** プロパティは、 **DataSource** プロパティに指定されたどのオブジェクトを **Recordset** オブジェクトとして表すかを指定します。 **Recordset** オブジェクトは、このプロパティを設定する前に閉じておく必要があります。 **DataSource** プロパティの前に **DataMember** プロパティが設定されていない場合、または **DataMember** 名が、 **DataSource** プロパティに指定されているオブジェクトに認識されない場合は、エラーが発生します。

**使用例**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
