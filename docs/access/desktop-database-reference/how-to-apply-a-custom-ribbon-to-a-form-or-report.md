---
title: フォームまたはレポートにカスタム リボンを適用します。
TOCTitle: Apply a custom ribbon to a form or report
ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15)
ms:contentKeyID: 48545865
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4fb0155b1a1ed36b6fe924f72a4da385197cc21
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478796"
---
# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>フォームまたはレポートにカスタム リボンを適用します。


**適用されます**Access 2013 |。Office 2013

リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、柔軟にリボン ユーザー インターフェイスをカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、フォームまたはレポートを読み込むときにカスタマイズしたリボンを適用する方法について説明します。

## <a name="making-the-ribbon-customization-xml-available"></a>リボンのカスタマイズ XML を使用できるようにする

**リボン機能拡張 XML をテーブルに保管する**

リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。

**USysRibbons** は、ユーザーが作成するシステム テーブルです。リボンのカスタマイズを実装するには、特定の列名を使用してこのテーブルを作成する必要があります。 **USysRibbons** テーブルを作成するときに使用する設定の一覧を次の表に示します。

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
<td><p>テキスト型 (Text)</p></td>
<td><p>このカスタマイズに関連付けられるカスタム リボンの名前が含まれます。</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>メモ型 (Memo)</p></td>
<td><p>リボン、リボンのカスタマイズを定義する機能拡張 XML (RibbonX) が含まれています</p></td>
</tr>
</tbody>
</table>


**プログラムを使用してリボン拡張 XML を読み込む**

**[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。

XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。

プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。

## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>カスタム リボンをフォームまたはレポートに割り当てる

1.  前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。

2.  デザイン ビューでフォームまたはレポートを開きます。

3.  [デザイン] タブの [ **プロパティ シート**] をクリックします。

4.  [プロパティ] ウィンドウの [ **すべて**] タブで、[ **リボン名**] ボックスをクリックし、リボンを選択します。

5.  フォームまたはレポートを保存して閉じ、再度開きます。選択した リボン UI が表示されます。


> [!NOTE]
> [!メモ] リボン UI に表示されるタブは付加的なものです。 具体的には、タブを非表示にするか、*最初から*属性を**True**に設定、しない限り、フォームのタブが表示されますか、レポートのリボンのユーザー インターフェイスは、既存のタブに追加します。

> [!NOTE]
> [!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。


