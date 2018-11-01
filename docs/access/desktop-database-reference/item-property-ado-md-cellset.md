---
title: Item プロパティ (ADO MD Cellset)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4f2f67daf4bf072037fac07ecdc3cd163904818
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883800"
---
# <a name="item-property-ado-md-cellset"></a>Item プロパティ (ADO MD Cellset)

**適用されます**Access 2013、Office 2013。

座標を使用して、セルセットからセルを取得します。

## <a name="syntax"></a>構文

*セル*の設定 = *セルセット*。項目 (*位置*)

## <a name="parameters"></a>パラメーター

- *Positions*

- セルを一意に指定するための値のバリアント型配列 ( **Variant** **Array** )。 *位置*には、次のいずれかを指定できます。
    
  - 位置番号の配列
    
  - メンバー名の配列
    
  - 位置を表す序数

## <a name="remarks"></a>解説

**Item** プロパティを使用して、 [Cellset](cell-object-ado-md.md) オブジェクト内の [Cell](cellset-object-ado-md.md) オブジェクトを返します。 *位置*引数に対応するセルが見つからない場合、 **Item**プロパティの場合は、エラーが発生します。

**Item** プロパティは **Cellset** オブジェクトの既定プロパティです。次のいずれの構文形式でも同じ結果が得られます。

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

*位置*の引数を返すセルを指定します。 セルは、位置を表す序数または各軸に沿った位置によって指定できます。 各軸に沿った位置によってセルを指定する場合は、位置の数値またはメンバーの名前を指定できます。

位置を表す序数は、**Cellset** 内のセルを一意に識別する数です。概念的には、**Cellset** 内のセルは **Cellset** が *p* 次元の配列であるかのように番号が付けられます。ここで、*p* は軸の数です。セルは行優先でアドレス指定されます。

**Item** にメンバー名を文字列として渡す場合、メンバーの軸の数値識別子は昇順で記載する必要があります。軸内では、次元のネストの昇順で記載する必要があります。つまり、最も外側の次元のメンバーを最初に記載し、その後に内側の次元のメンバーを記載します。各次元は個別の文字列で表し、メンバーの文字列の一覧はコンマで区切る必要があります。


> [!NOTE]
> [!メモ] データ プロバイダーによっては、メンバー名によるセルの取得がサポートされていない場合があります。詳細については、各自のプロバイダーのドキュメントを参照してください。


