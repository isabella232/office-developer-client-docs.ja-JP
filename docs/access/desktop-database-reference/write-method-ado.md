---
title: メソッド - を作成するには、ActiveX データ オブジェクト (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93336294380ffa207f47adbcad630be3fdd1a8b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950217"
---
# <a name="write-method-ado"></a>Write メソッド (ADO)

**適用されます**Access 2013、Office 2013。

バイナリ データを [Stream](stream-object-ado.md) オブジェクトに書き込みます。

## <a name="syntax"></a>構文

*ストリーム*。*バッファー*の書き込み

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Buffer* |書き込むバイト配列の入ったバリアント型 ( **Variant** ) の値を指定します。|

## <a name="remarks"></a>解説

指定したバイトが、各バイト間にスペースを一切挿入することなく **Stream** オブジェクトに書き込まれます。

カレント [Position](position-property-ado.md) は、書き込まれたデータの次のバイトに設定されます。 **Write** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろのバイトを切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。

現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しいバイトがすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。

> [!NOTE]
> **Write** メソッドは、バイナリ ストリーム ([Type](type-property-ado-stream.md) が **adTypeBinary**) で使用します。テキスト ストリーム (**Type** が **adTypeText**) の場合は、[WriteText](writetext-method-ado.md) を使用してください。

