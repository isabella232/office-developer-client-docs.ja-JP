---
title: SetLocalVar マクロ アクション
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b257473d2acd3d17f30a3fdd579d213dcd39487b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996903"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar マクロ アクション

**適用されます**Access 2013、Office 2013。

" **SetLocalVar/ローカル変数の設定** " アクションは、一時変数を作成し、それを特定の値に設定します。

## <a name="setting"></a>設定

" **SetLocalVar/ローカル変数の設定** " アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>はい</p></td>
<td><p>変数の名前を指定する文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>はい</p></td>
<td><p>この一時変数の値を設定に使用する式を指定します。 式の前に等号 (=) を付けないでください。 この引数を設定するのには、<strong>式ビルダー</strong>を使用するのには [<strong>ビルド</strong>] ボタンをクリックすることができます。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>備考

**予約**によって作成された変数は、定義されているマクロでのみ使用できます。 **[SetTempVar](settempvar-macro-action.md)** アクションを使用して、別のマクロ、イベント プロシージャ、またはフォームまたはレポートで使用できる変数を定義します。

一時変数を作成すると、それを式で参照できます。たとえば、TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロール ソースとして使用できます。

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> [!メモ] データ マクロでは、変数を参照するために LocalVals コレクションを使用する必要はありません。 などの TotalAmount を名前付きデータ マクロで一時変数を作成する場合可能性があります変数を使用するコントロールのソースとしてテキスト ボックスの次の構文を使用して: `=[TotalAmount]`。

