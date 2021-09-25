---
title: Read メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2588df93b014d4e5ca85b0b545b0a18bfa751174
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593811"
---
# <a name="read-method-ado"></a>Read メソッド (ADO)

**適用先**: Access 2013、Office 2013

バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。

## <a name="syntax"></a>構文

*バリアント型 (Variant)*  = *Stream*.読み取り (*NumBytes* )

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*NumBytes* |省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。|

## <a name="return-value"></a>戻り値

**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 (**Variant**) として返します。

## <a name="remarks"></a>注釈

*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。

> [!NOTE]
> *NumBytes* は常にバイトを表します。テキストの **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) の場合は、[ReadText](readtext-method-ado.md) を使用してください。


