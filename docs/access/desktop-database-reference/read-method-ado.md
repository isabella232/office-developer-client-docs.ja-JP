---
title: メソッドを ActiveX データ オブジェクト (ADO) を読む
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477376"
---
# <a name="read-method-ado"></a>Read メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。

## <a name="syntax"></a>構文

*バリアント* = *ストリーム*。読み取り (*NumBytes* )

## <a name="parameters"></a>パラメーター

  - *NumBytes*

  - 省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。

## <a name="return-value"></a>戻り値

**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 ( **Variant** ) として返します。

## <a name="remarks"></a>解説

*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。


> [!NOTE]
> <P><EM>NumBytes</EM> は常にバイトを表します。テキストの <STRONG>Stream</STRONG> オブジェクト (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeText</STRONG>) の場合は、<A href="readtext-method-ado.md">ReadText</A> を使用してください。</P>


