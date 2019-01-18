---
title: Supports メソッド (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703385"
---
# <a name="supports-method-ado"></a>Supports メソッド (ADO)

**適用されます**Access 2013、Office 2013。

指定された [Recordset](recordset-object-ado.md) オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。

## <a name="syntax"></a>構文

*ブール値* = *レコード セット*です。(*CursorOptions*) をサポートしています

## <a name="return-value"></a>戻り値

*CursorOptions*引数で識別される機能のすべてが、プロバイダーでサポートされているかどうかを示す**ブール**値を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*CursorOptions* |1 つまたは複数の **CursorOptionEnum** 値から成る長整数型 ( [Long](cursoroptionenum.md) ) の式を指定します。|

## <a name="remarks"></a>解説

**Supports** メソッドを使用すると、**Recordset** オブジェクトでサポートされている機能の種類を調べることができます。*CursorOptions* で指定した定数に対応する機能が **Recordset** オブジェクトでサポートされていると、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。


> [!NOTE]
> [!メモ] 指定した機能について **Supports** メソッドから **True** が返されても、その機能がどのような状況でもそのプロバイダーで使用できるという保証はありません。 **Supports** メソッドは、一定の条件が満たされていることを前提にしたうえで、指定された機能をプロバイダーがサポートできるかどうかを判別した結果を単に返すだけです。たとえば、カーソルが複数のテーブルの結合に基づいているために更新不可能な列があったとしても、 **Supports** は **Recordset** オブジェクトが更新をサポートしていると判別する場合があります。


