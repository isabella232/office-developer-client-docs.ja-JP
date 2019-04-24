---
title: CancelUpdate メソッド (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296669"
---
# <a name="cancelupdate-method-rds"></a>CancelUpdate メソッド (RDS)

**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトの現在の行または新しい行に加えられたすべての変更をキャンセルします。

## <a name="syntax"></a>構文

*DataControl*。CancelUpdate

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DataControl* |[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数。|

## <a name="remarks"></a>注釈

Cursor Service for OLE DB は、元の値のコピーと変更のキャッシュを両方維持します。**CancelUpdate** を呼び出すと、変更のキャッシュがリセットされて空になり、すべての連結コントロールが元のデータで更新されます。

