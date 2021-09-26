---
title: AppendChunk メソッド (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7582a33ea1add92f2c9d678a671cc6129e0f68ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607263"
---
# <a name="appendchunk-method-ado"></a>AppendChunk メソッド (ADO)

**適用先**: Access 2013、Office 2013

大きなサイズのテキストまたはバイナリ データの [Field](field-object-ado.md) オブジェクト、または [Parameter](parameter-object-ado.md) オブジェクトにデータを追加します。

## <a name="syntax"></a>構文

*オブジェクト。* AppendChunk *Data*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*object* |**Field** オブジェクトまたは **Parameter** オブジェクトを指定します。|
|*Data* |オブジェクトに追加するデータを含むバリアント型 ( **Variant** ) の値を指定します。|

## <a name="remarks"></a>注釈

**AppendChunk** メソッドは、長いバイナリ データまたは文字データを格納するために、**Field** オブジェクトまたは **Parameter** オブジェクトに対して使用します。システムのメモリに制限がある場合は、**AppendChunk** メソッドを使用することで、長い値を全体としてではなく、複数の部分に分けて操作できます。

### <a name="field"></a>フィールド

**Field** オブジェクトの [Attributes](attributes-property-ado.md) プロパティの **adFldLong** ビットが True に設定されている場合は、そのフィールドに対して **AppendChunk** メソッドを使用できます。

**Field** オブジェクトに対する **AppendChunk** メソッドの最初の呼び出しでフィールドにデータが書き込まれ、既存のデータが上書きされます。それ以降の **AppendChunk** の呼び出しでは、既存のデータに追加されます。あるフィールドにデータを追加し、その後、カレント レコードの別のフィールド値の設定または読み取りを行うと、最初のフィールドへのデータの追加は終了したものと見なされます。最初のフィールドに対して再度 **AppendChunk** メソッドを呼び出すと、新しい **AppendChunk** 操作と解釈され、既存のデータが上書きされます。最初の [Recordset](recordset-object-ado.md) オブジェクトの複製を除く他の **Recordset** オブジェクトのフィールドにアクセスした場合は、 **AppendChunk** 操作は中断されません。

**Field** オブジェクトで **AppendChunk** を呼び出したときにカレント レコードが存在しないと、エラーが発生します。

> [!NOTE]
> [!メモ] **AppendChunk** メソッドでは、 **Record** オブジェクトの [Field](record-object-ado.md) オブジェクトを操作できません。操作は何も実行されず、実行時エラーが発生します。

### <a name="parameters"></a>パラメーター

**Parameter** オブジェクトの **Attributes** プロパティの **adParamLong** ビットが True に設定されていると、そのパラメーターに対して **AppendChunk** メソッドを使用できます。

**Parameter** オブジェクトに対する **AppendChunk** メソッドの最初の呼び出しではパラメーターにデータが書き込まれ、既存のデータが上書きされます。それ以降の **Parameter** オブジェクトに対する **AppendChunk** の呼び出しでは、既存のパラメーター データに追加されます。 **AppendChunk** メソッドの呼び出しで Null 値を渡すと、すべてのパラメーター データが破棄されます。

