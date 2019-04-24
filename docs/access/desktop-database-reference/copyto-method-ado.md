---
title: CopyTo メソッド (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295479"
---
# <a name="copyto-method-ado"></a>CopyTo メソッド (ADO)

**適用先:** Access 2013、Office 2013

[Stream](stream-object-ado.md) オブジェクトから、指定した文字数またはバイト数 ([Type](type-property-ado-stream.md) によって決まる) のデータを別の **Stream** オブジェクトにコピーします。

## <a name="syntax"></a>構文

*ストリーム*。CopyTo *deststream*、 *numchars*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*DestStream* |開いている **Stream** オブジェクトへの参照を含むオブジェクト変数の値を指定します。 *DestStream* で指定した **Stream** に現在の **Stream** がコピーされます。 コピー先の **Stream** は既に開かれている必要があります。 開かれていない場合は、実行時エラーが発生します。<br/><br/>**注**: *deststream*パラメーターは、クライアントにリモート接続できない**stream**オブジェクト上のプライベートインターフェイスにアクセスする必要があるため、 **stream**オブジェクトのプロキシではない場合があります。|
|*NumChars* |省略可能です。コピー元 **Stream** の現在の位置からコピー先の **Stream** にコピーするバイト数または文字数を指定する整数型 (**Integer**) の値を指定します。既定値は -1 で、現在の位置から [EOS](eos-property-ado.md) までのすべての文字またはバイトをコピーするよう指定します。|

## <a name="remarks"></a>注釈

このメソッドは、[Position](position-property-ado.md) プロパティで指定された現在の位置から指定数の文字またはバイトをコピーします。指定した数が、現在の位置から **EOS** までのバイト数を超える場合は、現在の位置から **EOS** までの文字またはバイトのみがコピーされます。*NumChars* の値が ?1 の場合、または省略されている場合は、現在の位置から始まるすべての文字またはバイトがコピーされます。

コピー先のストリームに既存の文字またはバイトが存在する場合、コピーの終了ポイント以降の内容はすべてそのまま残り、削除されません。 **Position** は、コピーされた最後のバイトの次のバイトになります。これらのバイトを削除する場合は、 [SetEOS](seteos-method-ado.md) を呼び出してください。

**CopyTo** メソッドは、コピー先の **Stream** とコピー元の **Stream** の種類が同じ場合 (**Type** プロパティの設定値がいずれも **adTypeText** であるか、またはいずれも **adTypeBinary** である場合) のコピーに使用します。**Stream** オブジェクトが文字列型の場合、コピー先の **Stream** の [Charset](charset-property-ado.md) プロパティの設定値を変更すると、文字セットを別の文字セットに変換することができます。また、文字列型の **Stream** オブジェクトをバイナリ型の **Stream** オブジェクトにコピーすることはできますが、バイナリ型の **Stream** オブジェクトを文字列型の **Stream** オブジェクトにコピーすることはできません。

