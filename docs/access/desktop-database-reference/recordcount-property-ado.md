---
title: RecordCount プロパティ (ADO)
TOCTitle: RecordCount property (ADO)
ms:assetid: e3072d10-5bf7-02a8-027e-a9d9a34e3f27
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250155(v=office.15)
ms:contentKeyID: 48548304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: eea0d6fb59dae74304bb03fbb670c973f49262e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568559"
---
# <a name="recordcount-property-ado"></a>RecordCount プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクト内のレコード数を示します。

## <a name="return-value"></a>戻り値

**Recordset** のレコード数を示す長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**Recordset** オブジェクトに存在するレコード数を調べるには、 **RecordCount** プロパティを使用します。ADO でレコード数を特定できない場合や、プロバイダーやカーソルのタイプが **RecordCount** をサポートしていない場合、このプロパティは -1 を返します。閉じている **Recordset** オブジェクトの **RecordCount** プロパティを取得しようとすると、エラーが発生します。

**Recordset** オブジェクトがおよその位置付けまたはブックマークをサポートしている場合、つまり、 **Supports (adApproxPosition)** または **Supports (adBookmark)** がそれぞれ **True** を返す場合、 **Recordset** の値がすべて設定されているかどうかに関係なく、正確なレコード数が返されます。 **Recordset** オブジェクトがおよその位置付けをサポートしていない場合、正確な **RecordCount** の値を返すにはすべてのレコードを取得してカウントする必要があるので、このプロパティが大量のリソースを消費する可能性があります。

レコード数を特定できるかどうかは、 **Recordset** オブジェクトのカーソルのタイプによって異なります。 **RecordCount** プロパティは、前方スクロールのみのカーソルの場合は -1 を返します。静的カーソルまたはキーセット カーソルの場合は実際の数を返します。動的カーソルの場合はデータ ソースに応じて -1 または実際の数を返します。

