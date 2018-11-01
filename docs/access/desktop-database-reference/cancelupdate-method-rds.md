---
title: CancelUpdate メソッド (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28216cbeb98a0ebc7dfbc6115ea8bc05fadc057f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887748"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate メソッド (RDS)


**適用されます**Access 2013、Office 2013。



[Recordset](recordset-object-ado.md) オブジェクトの現在の行または新しい行に加えられたすべての変更をキャンセルします。

## <a name="syntax"></a>構文

*DataControl*。CancelUpdate

## <a name="parameters"></a>パラメーター

  - *DataControl*

  - [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。

## <a name="remarks"></a>解説

Cursor Service for OLE DB は、元の値のコピーと変更のキャッシュを両方維持します。 **CancelUpdate** を呼び出すと、変更のキャッシュがリセットされて空になり、すべての連結コントロールが元のデータで更新されます。

