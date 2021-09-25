---
title: WriteText メソッド (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b61687a933ff7a9b52ebd10958aa080aa383723b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593216"
---
# <a name="writetext-method-ado"></a>WriteText メソッド (ADO)

**適用先**: Access 2013、Office 2013

指定されたテキスト文字列を [Stream](stream-object-ado.md) オブジェクトに書き込みます。

## <a name="syntax"></a>構文

*Stream*.WriteText *Data*, *Options*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Data* |書き込むテキストが格納された文字列型 ( **String** ) の値を指定します。|
|*Options* |省略可能です。指定された文字列の末尾に行区切り文字を書き込むかどうかを指定する [StreamWriteEnum](streamwriteenum.md) 値を指定します。|

## <a name="remarks"></a>注釈

指定した文字列が、各文字列間にスペースや文字を挿入することなく **Stream** オブジェクトに書き込まれます。

カレント [Position](position-property-ado.md) は、書き込まれたデータの次の文字に設定されます。 **WriteText** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろの文字を切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。

現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しい文字がすべて格納できるように [Stream](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。

> [!NOTE]
> **WriteText** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText**) で使用します。バイナリ ストリーム (**Type** が **adTypeBinary**) の場合は、[Write](write-method-ado.md) を使用してください。


