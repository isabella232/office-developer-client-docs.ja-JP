---
title: Access の起動時にリボンを非表示にする
TOCTitle: Hide the ribbon when Access starts
description: Access 2013 のすべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537830"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Access の起動時にリボンを非表示にする

**適用先**: Access 2013 | Office 2013

既定では、Microsoft Access にはリボンを非表示にする方法は用意されていません。このトピックでは、すべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。

Access の起動時にカスタマイズされたリボンを読み込むには、その設定を **USysRibbons** という名前のテーブルに保存する必要があります。

リボンのカスタマイズを実装するには、特定の列名を使用して **USysRibbons** テーブルを作成する必要があります。 

次のテーブルは、**USysRibbons** テーブルを作成するときに使用する設定を示しています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>列名</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>テキスト</p></td>
<td><p>このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>メモ</p></td>
<td><p>リボンのカスタマイズを定義するリボン機能拡張 XML (RibbonX) が含まれます。</p></td>
</tr>
</tbody>
</table>

<br/>

次のテーブルは、**USysRibbons** テーブルに格納するリボンのカスタマイズ設定の一覧です。

|列名|値|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Access の起動時にカスタム リボンを適用する

アプリケーションの起動時にカスタム リボン UI を使用できるように適用するには、次の手順を実行します。

1.  前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。

2.  アプリケーションを閉じて、再起動します。

3.  [**Microsoft Office ボタン**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")] を選択し、[**Access のオプション**] を選択します。

4.  [**カレント データベース**] オプションを選択し、[**リボンとツール バーのオプション**] セクションで [**リボン名**] 一覧を選択して [**HideTheRibbon** ] を選択します。

5.  アプリケーションを閉じて、再起動します。

> [!NOTE]
> [!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。


