---
title: RecordCount プロパティ (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5ab01c419f703c1c17b1bf2b2cca2fb3844655d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712737"
---
# <a name="recordcount-property-ado"></a>RecordCount プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクト内のレコード数を示します。

## <a name="return-value"></a>戻り値

**Recordset** のレコード数を示す長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**Recordset** オブジェクトに存在するレコード数を調べるには、 **RecordCount** プロパティを使用します。ADO でレコード数を特定できない場合や、プロバイダーやカーソルのタイプが **RecordCount** をサポートしていない場合、このプロパティは -1 を返します。閉じている **Recordset** オブジェクトの **RecordCount** プロパティを取得しようとすると、エラーが発生します。

**Recordset** オブジェクトがおよその位置付けまたはブックマークをサポートしている場合、つまり、 **Supports (adApproxPosition)** または **Supports (adBookmark)** がそれぞれ **True** を返す場合、 **Recordset** の値がすべて設定されているかどうかに関係なく、正確なレコード数が返されます。 **Recordset** オブジェクトがおよその位置付けをサポートしていない場合、正確な **RecordCount** の値を返すにはすべてのレコードを取得してカウントする必要があるので、このプロパティが大量のリソースを消費する可能性があります。

レコード数を特定できるかどうかは、 **Recordset** オブジェクトのカーソルのタイプによって異なります。 **RecordCount** プロパティは、前方スクロールのみのカーソルの場合は -1 を返します。静的カーソルまたはキーセット カーソルの場合は実際の数を返します。動的カーソルの場合はデータ ソースに応じて -1 または実際の数を返します。

