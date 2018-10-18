---
タイトル: アクセスは、TOCTitle を起動したときにリボンを非表示: Access の起動時にリボンを非表示にする <<<<<<< ヘッド ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 2015/09/18 ===説明: すべての Access 2013 の組み込みタブを非表示にするカスタマイズされたリボンを読み込む方法です。
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: 48548817 ms.date: 2018/10/16
>>>>>>> マスター mtps_version: v=office.15
---

# <a name="hide-the-ribbon-when-access-starts"></a>Access の起動時にリボンを非表示にします。

**に適用されます:** Access 2013 |Office 2013

既定では、Microsoft Access にはリボンを非表示にする方法は用意されていません。このトピックでは、すべての組み込みタブが非表示になっているカスタマイズされたリボンを読み込む方法について説明します。

Access の起動時にカスタマイズされたリボンを読み込むには、その設定を **USysRibbons** という名前のテーブルに保存する必要があります。

<<<<<<< ヘッドを実装するのには、リボンをカスタマイズするために特定の列名を使用して**USysRibbons**テーブルを作成する必要があります。 次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。
=== リボンのカスタマイズの特定の列名を使用して実装することを、 **USysRibbons**テーブルを作成しなければなりません。 

次の表に、 **USysRibbons** テーブルを作成するときに使用する設定を示します。
>>>>>>> master

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<<<<<<< ヘッド
<th><p>列名</p></th>
<th><p>データ型</p></th>
=======
<th><p>列名</p></th>
<th><p>データ型</p></th>
>>>>>>>マスター
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
<<<<<<< ヘッド
<td><p>リボンのカスタマイズを定義するリボン拡張 XML (RibbonX) が含まれます。</p></td>
=======
<td><p>リボン機能拡張 (RibbonX)、リボンのカスタマイズを定義する XML が含まれています。</p></td>
>>>>>>>マスター
</tr>
</tbody>
</table>

<<<<<<< ヘッド

次の表に、 **USysRibbons** テーブルに保存するリボンのカスタマイズ設定を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>列名</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>して HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot。&gt; &lt;リボンの startFromScratch =&quot;真&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Access の起動時にカスタム リボンを適用する
=======
<br/>

次の表に、 **USysRibbons** テーブルに保存するリボンのカスタマイズ設定を示します。

|列名|値|
|:----------|:----|
|**RibbonName**|して HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Access の起動時にカスタム リボンを適用します。
>>>>>>> master

アプリケーションの起動時にカスタム リボン UI を使用できるように適用するには、次の手順を実行します。

1.  前述のプロセスに従って、カスタマイズされたリボンをアプリケーションで使用できるようにします。

2.  アプリケーションを閉じて、再起動します。

<<<<<<< ヘッド
3.  **Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") [ **Access のオプション**] をクリックします。

4.  [ **カレント データベース**] オプションをクリックし、[ **リボンとツール バーのオプション**] セクションで [ **リボン名**] ボックスの一覧をクリックして [ **HideTheRibbon** ] を選択します。
=======
3.  **Microsoft Office ボタン**をクリックして![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")、し、 **[Access のオプション**を選択します。

4.  **カレント データベース**] オプションを選択し、**リボンとツールバーのオプション**] セクションで、[**リボン名**] ボックスの一覧を選択**して HideTheRibbon**を選択します。
>>>>>>> master

5.  アプリケーションを閉じて、再起動します。

> [!NOTE]
> [!メモ] 他の Office アプリケーションのリボン UI の詳細については、「[Office Fluent リボンの概要](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon)」を参照してください。


