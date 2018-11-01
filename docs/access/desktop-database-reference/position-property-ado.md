---
title: Position プロパティ (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1111cdbc0e5a319f1f3431477854c6d38eff20
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875407"
---
# <a name="position-property-ado"></a>Position プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Stream](stream-object-ado.md) オブジェクト内の現在の位置を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

ストリームの先頭から現在位置までのオフセットをバイト単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 で、ストリームの最初のバイトを表します。

## <a name="remarks"></a>解説

現在位置はストリームの末尾よりも後ろに移動できます。ストリームの末尾を越えて現在位置を指定すると、 [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) オブジェクトの **Size** も拡張されます。この方法で追加された新しいバイトはすべて Null になります。


> [!NOTE]
> <P>[!メモ] <STRONG>Position</STRONG> は常にバイト単位です。マルチバイト文字セットを使用するテキスト ストリームでは、位置と文字サイズを乗算することによって文字数がわかります。たとえば、2 バイト文字セットの場合、最初の文字の位置は 0、2 番目の文字の位置は 2、3 番目の文字の位置は 4 のようになります。</P>



負の値を使用して **Stream** 内の現在位置を変更することはできません。 **Position** で使用できるのは正の値だけです。

読み取り専用の **Stream** オブジェクトの場合、 **Position** が **Stream** の **Size** よりも大きい値に設定されていても ADO はエラーを返しません。これによって、 **Stream** のサイズや、 **Stream** の内容が変更されることはありません。ただし、 **Position** の値が意味のない値になるので、このような操作はしないでください。

