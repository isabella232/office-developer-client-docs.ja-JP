---
title: Access の起動時にカスタム リボンを適用する
TOCTitle: Apply a custom ribbon when starting Access
description: Access 2013 でデータベースを開くときにカスタマイズされたリボンを適用する方法。
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291958"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Access の起動時にカスタム リボンを適用する

**適用先**: Access 2013 | Office 2013

リボンでは、リボン XML の作成およびカスタマイズを簡素化するテキストベースの宣言型 XML マークアップが使用されています。XML を数行記述するだけで、ユーザーに最適なインターフェイスを作成できます。Access では、非常に柔軟にリボン UI をカスタマイズできます。たとえば、カスタマイズしたマークアップをテーブルまたは別の Access データベースに格納する、VBA プロシージャに埋め込む、Excel のワークシートと関連付けるなどの操作ができます。このトピックでは、データベースを開くときにカスタマイズしたリボンを適用する方法について説明します。

## <a name="make-the-ribbon-customization-xml-available"></a>リボン カスタマイズ XML を利用可能にする

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>リボン機能拡張 XML をテーブルに格納する

リボンのカスタマイズを使用できるようにするための 1 つの方法は、リボンのカスタマイズをテーブルに保管することです。カスタマイズを " **USysRibbons** " という名前のテーブルに保管した場合、マクロまたは VBA コードを使用せずにカスタマイズを実装できます。

**USysRibbons** はユーザーが作成したシステム テーブルです。 リボンのカスタマイズを実装するには、特定の列名を使用してテーブルを作成する必要があります。 

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


### <a name="load-ribbon-extensibility-xml-programmatically"></a>プログラムでリボン機能拡張 XML を読み込む

**[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** メソッドを使用してリボンのカスタマイズをプログラムで読み込むことができます。通常、リボンを作成し、そのリボンをアプリケーションで使用できるようにするには、まず、リボンの名前と XML カスタマイズ マークアップを渡して **LoadCustomUI** メソッドを呼び出すプロシージャを使用して、データベースにモジュールを作成します。

XML マークアップには、テーブルから作成される **Recordset** オブジェクト、データベース外部のソース (文字列に解析する XML ファイルなど)、またはプロシージャの内部に直接埋め込まれた XML マークアップを指定できます。各リボンの名前およびリボンを構成するタブの **id** 属性が一意である限り、 **LoadCustomUI** メソッドへの呼び出しを複数回使用し、それぞれに異なる XML マークアップを渡すことで、異なるリボンを作成することができます。

プロシージャが完了したら、RunCode アクションを使用して、プロシージャを呼び出す AutoExec マクロを次に作成します。 これにより、アプリケーションが開始されたときに **LoadCustomUI** メソッドが自動的に実行され、すべてのカスタム リボンをアプリケーションで使用できるようになります。

## <a name="apply-customized-ribbons-when-access-starts"></a>Access の起動時にカスタマイズされたリボンを適用する

アプリケーションの起動時にカスタム UI を使用できるように適用するには、次の手順を実行します。

1.  前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。

2.  アプリケーションを閉じて、再起動します。

3.  [**Microsoft Office Button**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")] を選択し、[**ACCESS のオプション**] を選択します。

4.  [**カレント データベース**] オプションを選択し、[**リボンとツール バーのオプション**] セクションで [**リボン名**]  一覧を選択して、リボンを選択します。

5.  アプリケーションを閉じて、再起動します。選択した UI が表示されます。

> [!NOTE]
> [!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。


