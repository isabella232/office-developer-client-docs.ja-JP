---
title: アクセスを開始するときにカスタム リボンを適用します。
TOCTitle: Apply a custom ribbon when starting Access
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 575834f818386a7ba536e826fff2b7da00b324d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479719"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>アクセスを開始するときにカスタム リボンを適用します。

**に適用されます:** Access 2013 |Office 2013

リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、非常に柔軟にリボン UI をカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、データベースを開くときにカスタマイズしたリボンを適用する方法について説明します。

## <a name="making-the-ribbon-customization-xml-available"></a>リボンのカスタマイズ XML を使用できるようにする

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a>リボン機能拡張 XML をテーブルに保管する

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
<td><p>リボンのカスタマイズを定義するリボン拡張 XML (RibbonX) が含まれます。</p></td>
</tr>
</tbody>
</table>


### <a name="loading-ribbon-extensibility-xml-programmatically"></a>プログラムを使用してリボン拡張 XML を読み込む

**[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。

XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。

プロシージャが完了したら、"RunCode/プロシージャの実行" アクションを使用してプロシージャを呼び出す AutoExec マクロを作成します。これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。

## <a name="applying-customized-ribbons-when-access-starts"></a>Access の起動時にカスタマイズされたリボンを適用する

アプリケーションの起動時にカスタム UI を使用できるように適用するには、次の手順を実行します。

1.  前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。

2.  アプリケーションを閉じて、再起動します。

3.  **Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") [ **Access のオプション**] をクリックします。

4.  [ **カレント データベース**] オプションをクリックし、[ **リボンとツール バーのオプション**] セクションで [ **リボン名**] ボックスをクリックして、リボンを選択します。

5.  アプリケーションを閉じて、再起動します。選択した UI が表示されます。

> [!NOTE]
> [!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。


