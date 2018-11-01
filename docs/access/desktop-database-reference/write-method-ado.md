---
title: ActiveX データ オブジェクト (ADO) メソッドを作成します。
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5987b16c033b13be145e60317cdfdc821851be38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867413"
---
# <a name="write-method-ado"></a>Write メソッド (ADO)


**適用されます**Access 2013、Office 2013。


バイナリ データを [Stream](stream-object-ado.md) オブジェクトに書き込みます。

## <a name="syntax"></a>構文

*ストリーム*。*バッファー*の書き込み

## <a name="parameters"></a>パラメーター

  - *Buffer*

  - 書き込むバイト配列の入ったバリアント型 ( **Variant** ) の値を指定します。

## <a name="remarks"></a>解説

指定したバイトが、各バイト間にスペースを一切挿入することなく **Stream** オブジェクトに書き込まれます。

カレント [Position](position-property-ado.md) は、書き込まれたデータの次のバイトに設定されます。 **Write** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろのバイトを切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。

現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しいバイトがすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。


> [!NOTE]
> <P><STRONG>Write</STRONG> メソッドは、バイナリ ストリーム (<A href="type-property-ado-stream.md">Type</A> が <STRONG>adTypeBinary</STRONG>) で使用します。テキスト ストリーム (<STRONG>Type</STRONG> が <STRONG>adTypeText</STRONG>) の場合は、<A href="writetext-method-ado.md">WriteText</A> を使用してください。</P>


