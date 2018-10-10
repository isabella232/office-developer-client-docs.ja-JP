---
title: Supports メソッド (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61e6a4f3a5771c4d223380160204e4b0b350f210
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476231"
---
# <a name="supports-method-ado"></a>Supports メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

指定された [Recordset](recordset-object-ado.md) オブジェクトが特定の種類の機能をサポートしているかどうかを調べます。

## <a name="syntax"></a>構文

*ブール値* = *レコード セット*です。(*CursorOptions*) をサポートしています

## <a name="return-value"></a>戻り値

*CursorOptions*引数で識別される機能のすべてが、プロバイダーでサポートされているかどうかを示す**ブール**値を返します。

## <a name="parameters"></a>パラメーター

  - *CursorOptions*

  - 1 つまたは複数の **CursorOptionEnum** 値から成る長整数型 ( [Long](cursoroptionenum.md) ) の式を指定します。

## <a name="remarks"></a>解説

**Supports** メソッドを使用すると、**Recordset** オブジェクトでサポートされている機能の種類を調べることができます。*CursorOptions* で指定した定数に対応する機能が **Recordset** オブジェクトでサポートされていると、**Supports** メソッドは **True** を返します。それ以外の場合は、**False** を返します。


> [!NOTE]
> <P>[!メモ] 指定した機能について <STRONG>Supports</STRONG> メソッドから <STRONG>True</STRONG> が返されても、その機能がどのような状況でもそのプロバイダーで使用できるという保証はありません。 <STRONG>Supports</STRONG> メソッドは、一定の条件が満たされていることを前提にしたうえで、指定された機能をプロバイダーがサポートできるかどうかを判別した結果を単に返すだけです。たとえば、カーソルが複数のテーブルの結合に基づいているために更新不可能な列があったとしても、 <STRONG>Supports</STRONG> は <STRONG>Recordset</STRONG> オブジェクトが更新をサポートしていると判別する場合があります。</P>


