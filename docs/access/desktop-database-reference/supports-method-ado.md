---
title: サポート メソッド (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9551120657b2284959f1f7c69d8a11324ea9e5e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585257"
---
# <a name="supports-method-ado"></a>サポート メソッド (ADO)

**適用先**: Access 2013、Office 2013

指定された [Recordset](recordset-object-ado.md) オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。

## <a name="syntax"></a>構文

*boolean*  = *recordset*.サポート (*CursorOptions*)

## <a name="return-value"></a>戻り値

プロバイダーが *CursorOptions* 引数で指定されたすべての機能をサポートしているかどうかを示すブール型 (**Boolean**) の値を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*CursorOptions* |1 つまたは複数の **CursorOptionEnum** 値から成る長整数型 ( [Long](cursoroptionenum.md) ) の式を指定します。|

## <a name="remarks"></a>注釈

**Supports** メソッドを使用すると、**Recordset** オブジェクトでサポートされている機能の種類を調べることができます。*CursorOptions* で指定した定数に対応する機能が **Recordset** オブジェクトでサポートされていると、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。


> [!NOTE]
> [!メモ] 指定した機能について **Supports** メソッドから **True** が返されても、その機能がどのような状況でもそのプロバイダーで使用できるという保証はありません。 **Supports** メソッドは、一定の条件が満たされていることを前提にしたうえで、指定された機能をプロバイダーがサポートできるかどうかを判別した結果を単に返すだけです。たとえば、カーソルが複数のテーブルの結合に基づいているために更新不可能な列があったとしても、 **Supports** は **Recordset** オブジェクトが更新をサポートしていると判別する場合があります。


