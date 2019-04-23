---
title: Position プロパティ (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287525"
---
# <a name="position-property-ado"></a>Position プロパティ (ADO)

**適用先:** Access 2013、Office 2013

[Stream](stream-object-ado.md) オブジェクト内の現在の位置を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

ストリームの先頭から現在位置までのオフセットをバイト単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 で、ストリームの最初のバイトを表します。

## <a name="remarks"></a>注釈

現在位置はストリームの末尾よりも後ろに移動できます。ストリームの末尾を越えて現在位置を指定すると、 [Stream](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) オブジェクトの **Size** も拡張されます。この方法で追加された新しいバイトはすべて Null になります。

> [!NOTE]
> [!メモ] **Position** は常にバイト単位です。マルチバイト文字セットを使用するテキスト ストリームでは、位置と文字サイズを乗算することによって文字数がわかります。たとえば、2 バイト文字セットの場合、最初の文字の位置は 0、2 番目の文字の位置は 2、3 番目の文字の位置は 4 のようになります。

負の値を使用して **Stream** 内の現在位置を変更することはできません。 **Position** で使用できるのは正の値だけです。

読み取り専用の **Stream** オブジェクトの場合、 **Position** が **Stream** の **Size** よりも大きい値に設定されていても ADO はエラーを返しません。これによって、 **Stream** のサイズや、 **Stream** の内容が変更されることはありません。ただし、 **Position** の値が意味のない値になるので、このような操作はしないでください。

