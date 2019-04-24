---
title: GetChunk メソッド (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292287"
---
# <a name="getchunk-method-ado"></a>GetChunk メソッド (ADO)

**適用先:** Access 2013、Office 2013

サイズの大きいテキスト データやバイナリ データの [Field](field-object-ado.md) オブジェクトから、内容の全体または一部を返します。

## <a name="syntax"></a>構文

*変数* = *フィールド*GetChunk (*サイズ*)

## <a name="return-value"></a>戻り値

バリアント型 (**Variant**) の値を返します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Size* |取得するバイト数または文字数と等しい長整数型 ( **Long** ) の式を指定します。|

## <a name="remarks"></a>注釈

**Field** オブジェクトで **GetChunk** メソッドを使用すると、オブジェクトから長いバイナリ データや文字データの一部または全体を取得できます。システム メモリに制限がある場合、**GetChunk** メソッドを使用すると、長い値をセグメントに分けて操作できます。

**GetChunk** への呼び出しによって返される値は、*variable* に格納されます。*Size* が残りのデータよりも大きい場合、**GetChunk** メソッドは、*variable* の余った部分を空白で埋めることはなく、残りのデータのみを返します。フィールドが空の場合、**GetChunk** メソッドは Null 値を返します。

**GetChunk** を連続して呼び出すと、直前の **GetChunk** の呼び出しで取得されたデータの直後からデータが取得されます。ただし、あるフィールドのデータを取得しているときに、カレント レコードの別のフィールド値の設定または読み取りを行うと、最初のフィールドからのデータ取得は終了したと見なされます。最初のフィールドでもう一度 **GetChunk** メソッドを呼び出すと、新規の **GetChunk** 操作と解釈され、データ先頭から読み取りが開始されます。最初の [Recordset](recordset-object-ado.md) オブジェクトの複製を除く別の **Recordset** オブジェクトのフィールドにアクセスした場合、 **GetChunk** の操作は中断されません。

**Field** オブジェクトの [Attributes](attributes-property-ado.md) プロパティで **adFldLong** ビットが **True** に設定されていると、そのフィールドで **GetChunk** メソッドを使用できます。

**Field** オブジェクトで **GetChunk** メソッドを使用する際にカレント レコードがないと、エラー 3021 (カレント レコードがありません) が発生します。


> [!NOTE]
> [!メモ] **GetChunk** メソッドでは、 **Record** オブジェクトの [Field](record-object-ado.md) オブジェクトを操作できません。操作は何も実行されず、実行時エラーが発生します。


