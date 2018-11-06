---
title: LoadFromFile メソッド (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7b8492da87d0443d7992a1b9443501885ade3a0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998582"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile メソッド (ADO)

**適用されます**Access 2013、Office 2013。

既存のファイルの内容を [Stream](stream-object-ado.md) に読み込みます。

## <a name="syntax"></a>構文

*ストリーム*。LoadFromFile*ファイル名*

## <a name="parameters"></a>パラメーター

|名前 |説明|
|:----|:----------|
|*Filename* |**Stream** に読み込むファイルの名前を含む文字列型 ( **String** ) の値を指定します。 *ファイル名*には、任意の有効なパスと UNC 形式の名前を含めることができます。 指定したファイルが存在しない場合は、実行時エラーが発生します。|

## <a name="remarks"></a>解説

このメソッドを使用して、ローカル ファイルの内容を **Stream** オブジェクトに読み込むことができます。この方法で、ローカル ファイルの内容をサーバーにアップロードできます。

**Stream** オブジェクトは **LoadFromFile** を呼び出す前に開かれている必要があります。 **Stream** オブジェクトのバインディングはこのメソッドによって変更されず、その **Stream** を開いた URL または **Record** で指定されたオブジェクトにバインドされたままです。

**LoadFromFile** では、 **Stream** オブジェクトの現在の内容を、ファイルから読み込んだデータで上書きします。 **Stream** の既存のすべてのバイトは、ファイルの内容で上書きされます。 [LoadFromFile](eos-property-ado.md) メソッドで作成された **EOS** の後に残っている既存のバイトは、すべて削除されます。

**LoadFromFile** を呼び出した後、現在の位置は **Stream** の先頭に設定され、[Position](position-property-ado.md) プロパティが 0 になります。

ストリームの先頭にエンコード用の 2 バイトを追加できるので、ストリームのサイズは読み込み元のファイルのサイズと完全には一致しない場合があります。

