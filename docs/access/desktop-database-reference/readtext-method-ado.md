---
title: ReadText メソッド (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a46a62505f3234dc552db1ed39d38383524cda9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593804"
---
# <a name="readtext-method-ado"></a>ReadText メソッド (ADO)

**適用先**: Access 2013、Office 2013

文字列型の [Stream](stream-object-ado.md) オブジェクトから、指定された文字数を読み取ります。

## <a name="syntax"></a>構文

*文字列*  = *Stream*.ReadText (*NumChars*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*NumChars* |省略可能です。ファイルから読み取る文字の数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値を指定します。既定値は **adReadAll** です。|

## <a name="return-value"></a>戻り値

**ReadText** メソッドは、指定した文字数、行全体、またはストリーム全体を **Stream** オブジェクトから読み取り、結果の文字列を返します。

## <a name="remarks"></a>注釈

*NumChar* がストリームに残っている文字の数よりも大きい場合、残っている文字のみが返されます。読み取った文字列に、*NumChar* で指定した長さに合うようにスペースが補充されることはありません。読み取る文字が残っていない場合は、値が Null のバリアント型が返されます。**ReadText** は、逆方向の読み取りに使用することはできません。

> [!NOTE]
> **ReadText** メソッドは、文字列型ストリーム ([Type](type-property-ado-stream.md) が **adTypeText**) で使用します。バイナリ型のストリーム (**Type** が **adTypeBinary**) の場合は、[Read](read-method-ado.md) を使用してください。

