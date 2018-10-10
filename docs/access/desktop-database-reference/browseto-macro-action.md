---
title: "'BrowseTo/参照先' マクロ アクション"
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 09e2b8238555a0d1b718f04c69f733039c1d8477
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479619"
---
# <a name="browseto-macro-action"></a>"BrowseTo/参照先" マクロ アクション

**適用されます**Access 2013 |。Office 2013

**参照**アクションを使用するには保存されているオブジェクト間を移動します。 サブフォーム コントロールの引数へのパスを指定することで、サブフォーム コントロールのソース オブジェクトを変更することもできます。 **参照**を使用して、新しいウィンドウを開かずに、form2 を form1 から移動します。

## <a name="setting"></a>設定

**参照**操作では、次の引数があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>オブジェクトの種類</p></td>
<td><p>参照先のオブジェクトの種類。</p></td>
</tr>
<tr class="even">
<td><p>オブジェクト名</p></td>
<td><p>"Path to Subform Control/サブフォーム コントロールへのパス" 引数で参照するサブフォーム コントロール内に読み込まれるオブジェクト。</p></td>
</tr>
<tr class="odd">
<td><p>Path to Subform Control/サブフォーム コントロールへのパス</p></td>
<td><p>指定されている場合に、ターゲット アプリケーションのメイン フォームからのパスは、[オブジェクト名] 引数で指定されたオブジェクトその荷重を制御します。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>指定した場合は、オブジェクト レコード ソースの Where 条件を置き換えます。</p></td>
</tr>
<tr class="odd">
<td><p>Page オブジェクト</p></td>
<td><p>指定した場合は、現在のページになる帳票フォームのページを設定します。この引数は Web のみです。</p></td>
</tr>
<tr class="even">
<td><p>Data Mode/データ モード</p></td>
<td><p>指定した場合は、フォームのデータ入力モードを設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

PathToSubFormControl 引数は、次のコード例に示す構文で指定します。

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

この例では、Main Form が Access クライアント アプリケーションでの最上位フォームになります。"Path to Subform Control/サブフォーム コントロールへのパス" 引数では、メイン フォームから、"Object Name/オブジェクト名" 引数で指定したオブジェクトのコンテナーであるサブフォーム コントロールまで、フォームとサブフォーム コントロールの名前を交互に指定する必要があります。指定する各サブフォーム コントロールは、その前のフォーム上のコントロールである必要があります。このパスは、サブフォーム コントロールで終わる必要があります。

## <a name="example"></a>例

次の例では、参照操作を使用して、サブフォームのコントロールやナビゲーション コントロールは、レポートを開くにする方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



