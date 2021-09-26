---
title: LoadFromFile メソッド (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63b8c2541714f432e92d310ce70ebe308db51685
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612037"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile メソッド (ADO)

**適用先**: Access 2013、Office 2013

既存のファイルの内容を [Stream](stream-object-ado.md) に読み込みます。

## <a name="syntax"></a>構文

*Stream*.LoadFromFile *FileName*

## <a name="parameters"></a>パラメーター

|名前 |説明|
|:----|:----------|
|*FileName* |**Stream** に読み込むファイルの名前を含む文字列型 (**String**) の値を指定します。*FileName* には UNC 形式のパスとファイル名を指定できます。指定したファイルが存在しない場合は、実行時エラーが発生します。|

## <a name="remarks"></a>注釈

このメソッドを使用して、ローカル ファイルの内容を **Stream** オブジェクトに読み込むことができます。この方法で、ローカル ファイルの内容をサーバーにアップロードできます。

**Stream** オブジェクトは **LoadFromFile** を呼び出す前に開かれている必要があります。 **Stream** オブジェクトのバインディングはこのメソッドによって変更されず、その **Stream** を開いた URL または **Record** で指定されたオブジェクトにバインドされたままです。

**LoadFromFile** では、 **Stream** オブジェクトの現在の内容を、ファイルから読み込んだデータで上書きします。 **Stream** の既存のすべてのバイトは、ファイルの内容で上書きされます。 [LoadFromFile](eos-property-ado.md) メソッドで作成された **EOS** の後に残っている既存のバイトは、すべて削除されます。

**LoadFromFile** を呼び出した後、現在の位置は **Stream** の先頭に設定され、[Position](position-property-ado.md) プロパティが 0 になります。

ストリームの先頭にエンコード用の 2 バイトを追加できるので、ストリームのサイズは読み込み元のファイルのサイズと完全には一致しない場合があります。

