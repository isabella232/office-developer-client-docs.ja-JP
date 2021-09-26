---
title: BrowseTo マクロ アクション
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 53cc7fd0b085efee9b52d53371b08e338ccd4665
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607081"
---
# <a name="browseto-macro-action"></a>BrowseTo マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.

## <a name="setting"></a>設定

"BrowseTo/参照先" アクションの引数は次のとおりです。

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
<td><p>Object Type/オブジェクトの種類</p></td>
<td><p>参照先のオブジェクトの種類。</p></td>
</tr>
<tr class="even">
<td><p>オブジェクト名</p></td>
<td><p>"Path to Subform Control/サブフォーム コントロールへのパス" 引数で参照するサブフォーム コントロール内に読み込まれるオブジェクト。</p></td>
</tr>
<tr class="odd">
<td><p>Path to Subform Control/サブフォーム コントロールへのパス</p></td>
<td><p>指定した場合、アプリケーションのメイン フォームから Object Name 引数で指定されたオブジェクトを読み込むターゲット サブフォーム コントロールへのパス。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>指定した場合は、オブジェクト レコード ソースの Where 条件を置き換えます。</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>指定した場合は、現在のページになる帳票フォームのページを設定します。 この引数は Web のみです。</p></td>
</tr>
<tr class="even">
<td><p>Data Mode/データ モード</p></td>
<td><p>指定した場合は、フォームのデータ入力モードを設定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

PathToSubFormControl 引数は、次のコード例に示す構文で指定します。

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

この例では、Main Form が Access クライアント アプリケーションでの最上位フォームになります。"Path to Subform Control/サブフォーム コントロールへのパス" 引数では、メイン フォームから、"Object Name/オブジェクト名" 引数で指定したオブジェクトのコンテナーであるサブフォーム コントロールまで、フォームとサブフォーム コントロールの名前を交互に指定する必要があります。指定する各サブフォーム コントロールは、その前のフォーム上のコントロールである必要があります。このパスは、サブフォーム コントロールで終わる必要があります。

## <a name="example"></a>例

次の例は、BrowseTo アクションを使用して、サブフォーム コントロールまたはナビゲーション コントロール内でレポートを開く方法を示しています。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

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



