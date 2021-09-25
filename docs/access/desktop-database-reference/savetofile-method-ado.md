---
title: SaveToFile メソッド (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49ef7e94d0e196436500d0180a05a2e475660cfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589177"
---
# <a name="savetofile-method-ado"></a>SaveToFile メソッド (ADO)

**適用先**: Access 2013、Office 2013

[Stream](stream-object-ado.md) のバイナリの内容をファイルに保存します。

## <a name="syntax"></a>構文

*Stream*.SaveToFile *FileName*, *SaveOptions*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*FileName* |**Stream** の内容の保存先であるファイルの完全修飾名を含む文字列型 ( **String** ) の値を指定します。有効なローカルの場所、または UNC 値を介してアクセスできる場所への保存が可能です。|
|*SaveOptions* |保存するファイルがまだ存在しない場合に、 [SaveToFile](saveoptionsenum.md) メソッドで新しいファイルを作成するかどうかを **SaveOptionsEnum** 値で指定します。既定値は **adSaveCreateNotExists** です。これらのオプションでは、指定したファイルが存在しない場合にエラーが発生するように指定できます。また、 **SaveToFile** メソッドで既存ファイルの現在の内容を上書きするように指定することもできます。|

> [!NOTE]
> [!メモ] **adSaveCreateOverwrite** を設定して既存ファイルを上書きすると、 **SaveToFile** メソッドによって、元の既存ファイルから、新しい [EOS](eos-property-ado.md) 以降のバイトがすべて削除されます。

## <a name="remarks"></a>注釈

**SaveToFile** メソッドを使用すると、 **Stream** オブジェクトの内容をローカル ファイルにコピーできます。 **Stream** オブジェクトの内容やプロパティは変更されません。 **SaveToFile** メソッドを呼び出す前に、 **Stream** オブジェクトが開かれている必要があります。

このメソッドでは、 **Stream** オブジェクトと基になるソースの関連付けは変更されません。 **Stream** オブジェクトは、開かれたときのソースである元の URL または **Record** に関連付けられたままになります。

**SaveToFile** メソッドの操作後、ストリーム内の現在の位置 ([Position](position-property-ado.md)) は、ストリームの先頭 (0) に設定されます。

