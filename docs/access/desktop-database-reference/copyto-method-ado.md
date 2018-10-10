---
title: CopyTo メソッド (ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bd949b92068619b76ac78d5e62cde0e247ed7b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477626"
---
# <a name="copyto-method-ado"></a>CopyTo メソッド (ADO)


**適用されます**Access 2013 |。Office 2013


[Stream](type-property-ado-stream.md) オブジェクトから、指定した文字数またはバイト数 ( [Type](stream-object-ado.md) によって決まる) のデータを別の **Stream** オブジェクトにコピーします。

## <a name="syntax"></a>構文

*ストリーム*。CopyTo *DestStream*、 *NumChars*

## <a name="parameters"></a>パラメーター

  - *DestStream*

  - 開いている **Stream** オブジェクトへの参照を含むオブジェクト変数の値を指定します。*DestStream* で指定した **Stream** に現在の **Stream** がコピーされます。コピー先の **Stream** は既に開かれている必要があります。開かれていない場合は、実行時エラーが発生します。


    

    > [!NOTE]
    > <P><EM>DestStream</EM>パラメーターはありません<STRONG>ストリーム</STRONG>オブジェクトのプロキシ クライアントをリモート化不可能な<STRONG>ストリーム</STRONG>オブジェクトのプライベート インターフェイスへのアクセスが必要です。</P>



  - *NumChars*

  - 省略可能です。 コピー元 **Stream** の現在の位置からコピー先の **Stream** にコピーするバイト数または文字数を指定する整数型 ( **Integer** ) の値を指定します。 既定値は、-1 で、すべての文字またはバイトを[eos](eos-property-ado.md)の現在の位置からコピーされるように指定します。

## <a name="remarks"></a>解説

このメソッドは、[Position](position-property-ado.md) プロパティで指定された現在の位置から指定数の文字またはバイトをコピーします。 指定した数が、現在の位置から **EOS** までのバイト数を超える場合は、現在の位置から **EOS** までの文字またはバイトのみがコピーされます。 *NumChars*の値は-1、または省略すると、すべての文字または現在の位置から始まるバイトがコピーされます。

コピー先のストリームに既存の文字またはバイトが存在する場合、コピーの終了ポイント以降の内容はすべてそのまま残り、削除されません。 **Position** は、コピーされた最後のバイトの次のバイトになります。これらのバイトを削除する場合は、 [SetEOS](seteos-method-ado.md) を呼び出してください。

**CopyTo** メソッドは、コピー先の **Stream** とコピー元の **Stream** の種類が同じ場合 (**Type** プロパティの設定値がいずれも **adTypeText** であるか、またはいずれも **adTypeBinary** である場合) のコピーに使用します。**Stream** オブジェクトが文字列型の場合、コピー先の **Stream** の [Charset](charset-property-ado.md) プロパティの設定値を変更すると、文字セットを別の文字セットに変換することができます。また、文字列型の **Stream** オブジェクトをバイナリ型の **Stream** オブジェクトにコピーすることはできますが、バイナリ型の **Stream** オブジェクトを文字列型の **Stream** オブジェクトにコピーすることはできません。

